---
description: Pruebe automáticamente una página web para detectar problemas de accesibilidad mediante la sección Accesibilidad de la herramienta Problemas.
title: Probar automáticamente una página web para problemas de accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 1cba9db1744235dfbfd2a007e33d1101452aab31
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624741"
---
# <a name="automatically-test-a-webpage-for-accessibility-issues"></a><span data-ttu-id="48993-104">Probar automáticamente una página web para problemas de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="48993-104">Automatically test a webpage for accessibility issues</span></span>

<span data-ttu-id="48993-105">La **herramienta Problemas** incluye una sección **Accesibilidad** que notifica automáticamente problemas como la falta de texto alternativo en las imágenes, la falta de etiquetas en los campos de formulario y el contraste insuficiente de los colores del texto.</span><span class="sxs-lookup"><span data-stu-id="48993-105">The **Issues** tool includes an **Accessibility** section that automatically reports issues such as missing alternative text on images, missing labels on form fields, and insufficient contrast of text colors.</span></span>  <span data-ttu-id="48993-106">La **herramienta** Problemas se encuentra en el **cajón** en la parte inferior de DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-106">The **Issues** tool is within the **Drawer** at the bottom of DevTools.</span></span>  <span data-ttu-id="48993-107">En este artículo se usa la página web de demostración de pruebas de accesibilidad para realizar un paso adelante con la sección **Accesibilidad** de la **herramienta** Problemas.</span><span class="sxs-lookup"><span data-stu-id="48993-107">This article uses the accessibility-testing demo webpage to step through using the **Accessibility** section of the **Issues** tool.</span></span>

<span data-ttu-id="48993-108">Hay varias maneras de abrir la **herramienta Problemas,** como:</span><span class="sxs-lookup"><span data-stu-id="48993-108">There are several ways to open the **Issues** tool, such as:</span></span>
*  <span data-ttu-id="48993-109">Seleccione el **contador de problemas** \( Contador de problemas ![ ](../media/issues-counter-icon.msft.png) \) en la parte superior derecha de DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-109">Select the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\) in the upper right of DevTools.</span></span>
*  <span data-ttu-id="48993-110">En la **herramienta Elementos,** en el árbol DOM, **pulse Mayús y** haga clic en un subrayado ondulado en un elemento.</span><span class="sxs-lookup"><span data-stu-id="48993-110">In the **Elements** tool, in the DOM tree, **Shift+click** a wavy underline on an element.</span></span>
*  <span data-ttu-id="48993-111">En el **menú comando**, escriba `issues` y, a continuación, **seleccione Mostrar problemas**.</span><span class="sxs-lookup"><span data-stu-id="48993-111">In the **Command Menu**, type `issues`, and then select **Show Issues**.</span></span>


## <a name="view-the-accessibility-section-of-the-issues-tool"></a><span data-ttu-id="48993-112">Ver la sección Accesibilidad de la herramienta Problemas</span><span class="sxs-lookup"><span data-stu-id="48993-112">View the Accessibility section of the Issues tool</span></span>

1.  <span data-ttu-id="48993-113">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-113">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>  <span data-ttu-id="48993-114">En la parte superior derecha, **aparece** el contador de problemas \( Contador de problemas \), como un icono de burbuja de voz junto con el número de problemas ![ ](../media/issues-counter-icon.msft.png) detectados automáticamente.</span><span class="sxs-lookup"><span data-stu-id="48993-114">In the upper right, the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\) appears, as a speech-bubble icon along with the number of automatically detected issues.</span></span>  <span data-ttu-id="48993-115">Es posible que aparezca un número diferente en el explorador y que el número se actualice a medida que use DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-115">A different number might appear in your browser, and the number might update as you use DevTools.</span></span>

    :::image type="complex" source="../media/a11y-testing-issues-tracker.msft.png" alt-text="El contador Problemas de DevTools, que indica cuántos problemas hay en el documento actual" lightbox="../media/a11y-testing-issues-tracker.msft.png":::
        <span data-ttu-id="48993-117">El **contador Problemas** de DevTools, que indica cuántos problemas hay en el documento actual</span><span class="sxs-lookup"><span data-stu-id="48993-117">The **Issues counter** in DevTools, indicating how many problems there are in the current document</span></span>
    :::image-end:::

1.  <span data-ttu-id="48993-118">Seleccione el **contador Problemas**.</span><span class="sxs-lookup"><span data-stu-id="48993-118">Select the **Issues counter**.</span></span>  <span data-ttu-id="48993-119">Se **abre** la herramienta Problemas, en el **cajón** situado en la parte inferior de DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-119">The **Issues** tool opens, in the **Drawer** at the bottom of DevTools.</span></span>

    :::image type="complex" source="../media/a11y-testing-accessibility-issues.msft.png" alt-text="Advertencias de accesibilidad mostradas en la herramienta Problemas" lightbox="../media/a11y-testing-accessibility-issues.msft.png":::
        <span data-ttu-id="48993-121">Advertencias de accesibilidad mostradas en la herramienta Problemas</span><span class="sxs-lookup"><span data-stu-id="48993-121">Accessibility warnings displayed in the Issues tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="48993-122">En la **pestaña Problemas,** expanda la **sección Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="48993-122">On the **Issues** tab, expand the **Accessibility** section.</span></span>


## <a name="verify-that-input-fields-have-labels"></a><span data-ttu-id="48993-123">Comprobar que los campos de entrada tienen etiquetas</span><span class="sxs-lookup"><span data-stu-id="48993-123">Verify that input fields have labels</span></span>

<span data-ttu-id="48993-124">Para comprobar si los campos de entrada \*\*\*\* tienen etiquetas conectadas, use la herramienta Problemas, que comprueba automáticamente toda la página web e informa de este problema en la **sección Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="48993-124">To check whether input fields have labels connected to them, use the **Issues** tool, which automatically checks the entire webpage and reports this issue in the **Accessibility** section.</span></span>

1.  <span data-ttu-id="48993-125">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-125">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="48993-126">En la parte superior derecha, seleccione el **contador de problemas** \( Contador de problemas ![ ](../media/issues-counter-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="48993-126">In the upper right, select the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\).</span></span>  <span data-ttu-id="48993-127">Se **abre** la herramienta Problemas, en el **cajón** situado en la parte inferior de DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-127">The **Issues** tool opens, in the **Drawer** at the bottom of DevTools.</span></span>

1.  <span data-ttu-id="48993-128">En la **pestaña Problemas,** expanda la **sección Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="48993-128">On the **Issues** tab, expand the **Accessibility** section.</span></span>

1.  <span data-ttu-id="48993-129">Expanda la **advertencia** `Form elements must have labels: Element has no title attribute Element has no placeholder attribute` .</span><span class="sxs-lookup"><span data-stu-id="48993-129">Expand the **Warning** `Form elements must have labels: Element has no title attribute Element has no placeholder attribute`.</span></span>

1. <span data-ttu-id="48993-130">Seleccione el **vínculo Abrir en elementos.**</span><span class="sxs-lookup"><span data-stu-id="48993-130">Select the **Open in Elements** link.</span></span>

    :::image type="complex" source="../media/a11y-testing-inspect-problematic-element.msft.png" alt-text="Herramienta Elementos que muestra el HTML problemático después de seleccionar el vínculo en la herramienta Problemas" lightbox="../media/a11y-testing-inspect-problematic-element.msft.png":::
        <span data-ttu-id="48993-132">Herramienta Elementos que muestra el HTML problemático después de seleccionar el vínculo en la **herramienta** Problemas</span><span class="sxs-lookup"><span data-stu-id="48993-132">Elements tool showing the problematic HTML after selecting the link in the **Issues** tool</span></span> :::image-end:::

    <span data-ttu-id="48993-133">Se **abre** la herramienta Elementos, con el elemento resaltado en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="48993-133">The **Elements** tool opens, with the element highlighted in the DOM tree.</span></span>  <span data-ttu-id="48993-134">El **panel Estilos** muestra las reglas CSS aplicadas para el elemento.</span><span class="sxs-lookup"><span data-stu-id="48993-134">The **Styles** pane displays the applied CSS rules for the element.</span></span>  <span data-ttu-id="48993-135">Ahora se muestra el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="48993-135">The following code is now displayed.</span></span>

    ```html
    <label>Search</label>
    <input type="search">
    <input type="submit" value="go">
    ```

    <span data-ttu-id="48993-136">En el código anterior, el elemento se usa incorrectamente, ya que no hay conexión `label` entre el elemento y un elemento `label` `input` determinado.</span><span class="sxs-lookup"><span data-stu-id="48993-136">In the above code, the `label` element is used incorrectly, because there is no connection between the `label` element and a particular `input` element.</span></span>  <span data-ttu-id="48993-137">Para conectar el `label` elemento a un elemento `input` específico, use cualquiera de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="48993-137">To connect the `label` element to a specific `input` element, use any of the following options.</span></span>
    *   <span data-ttu-id="48993-138">Anide `input` el elemento dentro del `label` elemento.</span><span class="sxs-lookup"><span data-stu-id="48993-138">Nest the `input` element within the `label` element.</span></span>
    *   <span data-ttu-id="48993-139">En el `label` elemento, agregue un `for` atributo que coincida con un atributo del `id` `input` elemento.</span><span class="sxs-lookup"><span data-stu-id="48993-139">In the `label` element, add a `for` attribute that matches an `id` attribute of the `input` element.</span></span>

    <span data-ttu-id="48993-140">También hay otra forma de probar la falta de conexiones entre elementos.</span><span class="sxs-lookup"><span data-stu-id="48993-140">There's also another way to test for lack of connections between elements.</span></span> <span data-ttu-id="48993-141">En la **herramienta Elementos,** seleccione el `<label>Search</label>` elemento en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="48993-141">In the **Elements** tool, select the `<label>Search</label>` element in the DOM tree.</span></span>  <span data-ttu-id="48993-142">En la página web, observe que el foco solo aparece en la **etiqueta de** búsqueda y no en el cuadro de texto de entrada.</span><span class="sxs-lookup"><span data-stu-id="48993-142">On the webpage, notice that focus only appears on the **Search** label, and not the input textbox.</span></span>  <span data-ttu-id="48993-143">La implementación correcta se centraría en el `search` cuadro de texto de entrada y la **etiqueta** de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="48993-143">The correct implementation would put focus on the `search` input textbox and the **Search** label.</span></span>

1.  <span data-ttu-id="48993-144">Como ejemplo de una conexión correcta, seleccione la **etiqueta Otro** en el formulario de donación.</span><span class="sxs-lookup"><span data-stu-id="48993-144">As an example of a correct connection, select the **Other** label on the donation form.</span></span>  <span data-ttu-id="48993-145">Un cuadro de indicador de foco aparece correctamente \*\*\*\* en el cuadro de texto de entrada junto a la etiqueta Otros, ya que hay valores de atributo `for` y `id` coincidencia.</span><span class="sxs-lookup"><span data-stu-id="48993-145">A focus-indicator box correctly appears on the input textbox next to the **Other** label, because there are matching `for` and `id` attribute values.</span></span>

1.  <span data-ttu-id="48993-146">En la **herramienta Problemas,** seleccione **Más lectura** para obtener más información sobre el problema.</span><span class="sxs-lookup"><span data-stu-id="48993-146">In the **Issues tool**, select **Further reading** to learn more about the issue.</span></span>  <span data-ttu-id="48993-147">Para abrir el vínculo en una nueva pestaña, **haga**clic en el vínculo en Windows/Linux o comando haga clic en + \*\*\*\* el vínculo en \*\*\*\* + \*\*\*\* macOS.</span><span class="sxs-lookup"><span data-stu-id="48993-147">To open the link in a new tab, **Ctrl**+**click** the link on Windows/Linux, or **Command**+**click** the link on macOS.</span></span>

    :::image type="complex" source="../media/a11y-testing-more-information-links.msft.png" alt-text="Vínculo en la pestaña Problemas que apunta a información más detallada sobre el problema" lightbox="../media/a11y-testing-more-information-links.msft.png":::
        <span data-ttu-id="48993-149">Vínculo en la **pestaña Problemas** que apunta a información más detallada sobre el problema</span><span class="sxs-lookup"><span data-stu-id="48993-149">Link on the **Issues** tab pointing to more in-depth information about the issue</span></span>
    :::image-end:::


## <a name="verify-that-images-have-alt-text"></a><span data-ttu-id="48993-150">Comprobar que las imágenes tienen texto alternativo</span><span class="sxs-lookup"><span data-stu-id="48993-150">Verify that images have alt text</span></span>

<span data-ttu-id="48993-151">Las pruebas básicas de accesibilidad requieren asegurarse de que se proporciona texto alternativo (también denominado _texto_alternativo) para las imágenes.</span><span class="sxs-lookup"><span data-stu-id="48993-151">Basic accessibility testing requires making sure alternative text (also called _alt text_) is provided for images.</span></span>

<span data-ttu-id="48993-152">Para comprobar automáticamente si se proporciona texto alternativo para imágenes, use la herramienta **Problemas,** que tiene una sección **Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="48993-152">To automatically check whether alt text is provided for images, use the **Issues** tool, which has an **Accessibility** section.</span></span>  <span data-ttu-id="48993-153">La **herramienta** Problemas se encuentra en el **cajón** en la parte inferior de DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-153">The **Issues** tool is located in the **Drawer** at the bottom of DevTools.</span></span>

1.  <span data-ttu-id="48993-154">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-154">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="48993-155">Para abrir la **herramienta Problemas,** seleccione el contador **Problemas** en la esquina superior derecha de DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-155">To open the **Issues** tool, select the **Issues** counter in the upper right of DevTools.</span></span>

1.  <span data-ttu-id="48993-156">En la **pestaña Problemas,** expanda la advertencia `Images must have alternate text: Element has no title attribute` .</span><span class="sxs-lookup"><span data-stu-id="48993-156">On the **Issues** tab, expand the warning `Images must have alternate text: Element has no title attribute`.</span></span>  <span data-ttu-id="48993-157">Hay cuatro instancias de imágenes que carecen de texto alternativo.</span><span class="sxs-lookup"><span data-stu-id="48993-157">There are four instances of images that lack alt text.</span></span>

    :::image type="complex" source="../media/a11y-testing-images-without-alt.msft.png" alt-text="Las imágenes de informes de la herramienta Problemas a las que les falta texto alternativo" lightbox="../media/a11y-testing-images-without-alt.msft.png":::
        <span data-ttu-id="48993-159">Las imágenes de informes de la herramienta Problemas a las que les falta texto alternativo</span><span class="sxs-lookup"><span data-stu-id="48993-159">The Issues tool reporting images that are missing alternative text</span></span>
    :::image-end:::

<span data-ttu-id="48993-160">Para obtener más información, vaya [a Imágenes debe tener texto alternativo.](https://dequeuniversity.com/rules/axe/4.1/image-alt)</span><span class="sxs-lookup"><span data-stu-id="48993-160">For more information, navigate to [Images must have alternate text](https://dequeuniversity.com/rules/axe/4.1/image-alt).</span></span>


## <a name="verify-that-text-colors-have-enough-contrast"></a><span data-ttu-id="48993-161">Comprobar que los colores de texto tienen suficiente contraste</span><span class="sxs-lookup"><span data-stu-id="48993-161">Verify that text colors have enough contrast</span></span>

<span data-ttu-id="48993-162">Para comprobar automáticamente si los colores de texto tienen suficiente contraste, use la **herramienta Problemas,** que tiene una sección **Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="48993-162">To automatically check whether text colors have enough contrast, use the **Issues** tool, which has an **Accessibility** section.</span></span>  <span data-ttu-id="48993-163">La **herramienta** Problemas se encuentra en el **cajón** en la parte inferior de DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-163">The **Issues** tool is located in the **Drawer** at the bottom of DevTools.</span></span>

1.  <span data-ttu-id="48993-164">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-164">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="48993-165">Para abrir la **herramienta Problemas,** seleccione el contador **Problemas** en la esquina superior derecha de DevTools.</span><span class="sxs-lookup"><span data-stu-id="48993-165">To open the **Issues** tool, select the **Issues** counter in the upper right of DevTools.</span></span>  <span data-ttu-id="48993-166">Es posible que recibas advertencias de que dos elementos de la página web de demostración no tienen suficiente contraste.</span><span class="sxs-lookup"><span data-stu-id="48993-166">You may receive warnings that two elements on the demo webpage don't have enough contrast.</span></span>

    :::image type="complex" source="../media/a11y-testing-contrast-issues.msft.png" alt-text="Problemas de contraste notificados en la herramienta Problemas" lightbox="../media/a11y-testing-contrast-issues.msft.png":::
        <span data-ttu-id="48993-168">Problemas de contraste notificados en la herramienta Problemas</span><span class="sxs-lookup"><span data-stu-id="48993-168">Contrast problems reported in the Issues tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="48993-169">Según la configuración, la pestaña **Problemas** puede tener una advertencia como que los usuarios pueden tener dificultades para leer contenido de texto debido a un contraste de **color insuficiente.**</span><span class="sxs-lookup"><span data-stu-id="48993-169">Depending on your settings, the **Issues** tab might have a warning like **Users may have difficulties reading text content due to insufficient color contrast**.</span></span>   <span data-ttu-id="48993-170">Puede expandir esa advertencia y, a continuación, expandir **Recursos afectados**.</span><span class="sxs-lookup"><span data-stu-id="48993-170">You can expand that warning, and then expand **Affected resources**.</span></span>  <span data-ttu-id="48993-171">Aparece una lista de elementos con una lista de elementos que no tienen suficiente contraste.</span><span class="sxs-lookup"><span data-stu-id="48993-171">A list of elements appears with a list of elements that don't have enough contrast.</span></span>


1.  <span data-ttu-id="48993-172">Seleccione el `li.high` elemento.</span><span class="sxs-lookup"><span data-stu-id="48993-172">Select the `li.high` element.</span></span>  <span data-ttu-id="48993-173">En la página web que se representa, se resalta el vínculo **Perros** de la sección **Donar,** que muestra una pequeña superposición de información.</span><span class="sxs-lookup"><span data-stu-id="48993-173">In the rendered webpage, the **Dogs** link in the **Donate** section is highlighted, displaying a small information overlay.</span></span>  <span data-ttu-id="48993-174">Esta es la misma superposición que aparece al pasar el puntero sobre un elemento del árbol DOM de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="48993-174">This is the same overlay that appears when you hover over an element in the DOM tree in the **Elements** tool.</span></span>

    :::image type="complex" source="../media/a11y-testing-element-with-contrast-issues.msft.png" alt-text="Elemento de la página web resaltado después de seleccionar un vínculo en la sección Recursos afectados" lightbox="../media/a11y-testing-element-with-contrast-issues.msft.png":::
        <span data-ttu-id="48993-176">Elemento de la página web resaltado después de seleccionar un vínculo en la **sección Recursos afectados**</span><span class="sxs-lookup"><span data-stu-id="48993-176">Element in the webpage highlighted after selecting a link in the **Affected Resources** section</span></span>
    :::image-end:::


### <a name="wavy-underlines-in-the-dom-tree-indicate-automatically-detected-issues"></a><span data-ttu-id="48993-177">Los subrayados ondulados en el árbol DOM indican problemas detectados automáticamente</span><span class="sxs-lookup"><span data-stu-id="48993-177">Wavy underlines in the DOM tree indicate automatically detected issues</span></span> 

<span data-ttu-id="48993-178">El árbol DOM de la **herramienta Elementos** marca los problemas directamente en el HTML con subrayados ondulados.</span><span class="sxs-lookup"><span data-stu-id="48993-178">The DOM tree in the **Elements** tool flags issues directly in the HTML with wavy underlines.</span></span>  <span data-ttu-id="48993-179">La herramienta **Problemas** notifica estos problemas.</span><span class="sxs-lookup"><span data-stu-id="48993-179">These issues are reported by the **Issues** tool.</span></span>  <span data-ttu-id="48993-180">Al **mayús+clic en** cualquier elemento con un subrayado ondulado, se muestra **la herramienta** Problemas.</span><span class="sxs-lookup"><span data-stu-id="48993-180">When you **Shift+click** any element with a wavy underline, the **Issues tool** is displayed.</span></span>

1.  <span data-ttu-id="48993-181">En la **herramienta Elementos,** en el árbol DOM, **pulse Mayús y** haga clic en el elemento , que tiene una línea `<input type="search">` ondulada debajo `input` de .</span><span class="sxs-lookup"><span data-stu-id="48993-181">In the **Elements** tool, in the DOM tree, **Shift+click** the element `<input type="search">`, which has a wavy line under `input`.</span></span>  <span data-ttu-id="48993-182">Se **muestra la herramienta** Problemas y se muestra el problema de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="48993-182">The **Issues tool** is displayed, and shows the issue for that element.</span></span>

    :::image type="complex" source="../media/a11y-testing-wavy-underlines.msft.png" alt-text="Un elemento que tiene un subrayado ondulado en la vista DOM tiene un problema" lightbox="../media/a11y-testing-wavy-underlines.msft.png":::
        <span data-ttu-id="48993-184">Un elemento que tiene un subrayado ondulado en la vista DOM tiene un problema</span><span class="sxs-lookup"><span data-stu-id="48993-184">An element that has a wavy underline in the DOM view has an issue</span></span>
    :::image-end:::


## <a name="see-also"></a><span data-ttu-id="48993-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="48993-185">See also</span></span>

*  [<span data-ttu-id="48993-186">Buscar y corregir problemas con la herramienta Problemas</span><span class="sxs-lookup"><span data-stu-id="48993-186">Find and fix problems using the Issues tool</span></span>][DevToolsIssuesTool]
*  [<span data-ttu-id="48993-187">Información general sobre las pruebas de accesibilidad con DevTools</span><span class="sxs-lookup"><span data-stu-id="48993-187">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="48993-188">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="48993-188">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsIssuesTool]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

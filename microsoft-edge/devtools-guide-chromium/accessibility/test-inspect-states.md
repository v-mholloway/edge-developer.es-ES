---
description: Inspeccione la accesibilidad de todos los estados de los elementos, como el contraste de texto durante el estado de desplazamiento, en el panel Estilos mediante El estado del elemento Toggle.
title: Comprobar la accesibilidad de todos los estados de elementos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 129a89f94925de24a4e649bd91f513de031d6b4a
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597686"
---
# <a name="verify-accessibility-of-all-states-of-elements"></a><span data-ttu-id="eaf07-104">Comprobar la accesibilidad de todos los estados de elementos</span><span class="sxs-lookup"><span data-stu-id="eaf07-104">Verify accessibility of all states of elements</span></span>

<!-- 5. STYLES: TOGGLE STATE -->

<span data-ttu-id="eaf07-105">Compruebe la accesibilidad de todos los estados de los elementos, como el contraste de color del texto durante el `hover` estado.</span><span class="sxs-lookup"><span data-stu-id="eaf07-105">Check the accessibility of all states of elements, such as text color contrast during the `hover` state.</span></span>  <span data-ttu-id="eaf07-106">La **herramienta Inspeccionar** informa de problemas de accesibilidad de un estado a la vez.</span><span class="sxs-lookup"><span data-stu-id="eaf07-106">The **Inspect** tool reports accessibility issues for one state at a time.</span></span>  <span data-ttu-id="eaf07-107">Para comprobar la accesibilidad de los \*\*\*\* distintos estados de los elementos, en la pestaña Estilos, seleccione **\:hov** (**Toggle Element State**), tal como se describe en este artículo.</span><span class="sxs-lookup"><span data-stu-id="eaf07-107">To check accessibility of the various states of elements, in the **Styles** tab, select **\:hov** (**Toggle Element State**), as described in this article.</span></span> <span data-ttu-id="eaf07-108">Primero se muestra por qué es necesaria la simulación de estado con la herramienta **Inspeccionar** y, a continuación, se muestra cómo usar la simulación de estado.</span><span class="sxs-lookup"><span data-stu-id="eaf07-108">We first show why state simulation is necessary using the **Inspect** tool, and then we show how to use state simulation.</span></span>


## <a name="checking-text-color-contrast-in-the-default-state"></a><span data-ttu-id="eaf07-109">Comprobar el contraste de color del texto en el estado predeterminado</span><span class="sxs-lookup"><span data-stu-id="eaf07-109">Checking text color contrast in the default state</span></span>

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

<span data-ttu-id="eaf07-110">Además de las pruebas automáticas de contraste de color en la herramienta **Problemas,** también puede usar la herramienta **Inspeccionar** para comprobar si los elementos de página individuales tienen suficiente contraste.</span><span class="sxs-lookup"><span data-stu-id="eaf07-110">In addition to the automatic color-contrast tests in the **Issues** tool, you can also use the **Inspect** tool to check whether individual page elements have enough contrast.</span></span>  <span data-ttu-id="eaf07-111">Si la información de contraste está disponible, la superposición **Inspeccionar** muestra la relación de contraste y un elemento de casilla.</span><span class="sxs-lookup"><span data-stu-id="eaf07-111">If contrast information is available, the **Inspect** overlay shows the contrast ratio and a checkbox item.</span></span>  <span data-ttu-id="eaf07-112">Un icono de marca de verificación verde indica que hay suficiente contraste y un icono de alerta amarilla indica que no hay suficiente contraste.</span><span class="sxs-lookup"><span data-stu-id="eaf07-112">A green check mark icon indicates there's enough contrast, and a yellow alert icon indicates that there's not enough contrast.</span></span>

<span data-ttu-id="eaf07-113">Por ejemplo, los vínculos del menú de navegación de la barra lateral tienen suficiente contraste.</span><span class="sxs-lookup"><span data-stu-id="eaf07-113">For example, the links in the sidebar navigation menu have enough contrast.</span></span>  <span data-ttu-id="eaf07-114">Pero el elemento **verde de** la lista Perros de la sección **Estado** de donación no tiene suficiente contraste, por lo que se marca mediante una advertencia en la superposición **Inspeccionar.**</span><span class="sxs-lookup"><span data-stu-id="eaf07-114">But the green **Dogs** list item in the **Donation status** section doesn't have enough contrast, and so is flagged by a warning in the **Inspect** overlay.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Los vínculos del menú de navegación de la barra lateral tienen suficiente contraste, como se muestra en la superposición Inspeccionar" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
            <span data-ttu-id="eaf07-116">Los vínculos del menú de navegación de la barra lateral tienen suficiente contraste, como se muestra en **la superposición Inspeccionar**</span><span class="sxs-lookup"><span data-stu-id="eaf07-116">The links in the sidebar navigation menu have enough contrast, as shown in the **Inspect** overlay</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Un elemento que no tiene suficiente contraste se marca mediante una advertencia en la superposición Inspeccionar" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
            <span data-ttu-id="eaf07-118">Un elemento que no tiene suficiente contraste se marca mediante una advertencia en la **superposición Inspeccionar**</span><span class="sxs-lookup"><span data-stu-id="eaf07-118">An element that doesn't have enough contrast is flagged by a warning in the **Inspect** overlay</span></span> :::image-end:::
    :::column-end:::
:::row-end:::
        

## <a name="hovering-when-the-inspect-tool-is-active-doesnt-show-the-text-color-contrast-for-the-hover-state"></a><span data-ttu-id="eaf07-119">Si se activa la herramienta Inspeccionar, no se muestra el contraste de color de texto para el estado de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="eaf07-119">Hovering when the Inspect tool is active doesn't show the text-color contrast for the hover state</span></span>

<span data-ttu-id="eaf07-120">La **superposición** de información de la herramienta Inspeccionar solo representa un solo estado.</span><span class="sxs-lookup"><span data-stu-id="eaf07-120">The **Inspect** tool's information overlay only represents a single state.</span></span>  <span data-ttu-id="eaf07-121">Los elementos de la página pueden tener estados diferentes, todos los cuales deben probarse.</span><span class="sxs-lookup"><span data-stu-id="eaf07-121">Elements on the page can have different states, all of which need to be tested.</span></span>  <span data-ttu-id="eaf07-122">Por ejemplo, al pasar el puntero del mouse sobre el menú de la página de demostración de pruebas de accesibilidad, se obtiene una animación que cambia los colores.</span><span class="sxs-lookup"><span data-stu-id="eaf07-122">For example, when you hover the mouse pointer over the menu of the accessibility-testing demo page, you get an animation that changes the colors.</span></span> <span data-ttu-id="eaf07-123">Realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="eaf07-123">Perform the following steps.</span></span>

1.  <span data-ttu-id="eaf07-124">Abra la [página web de demostración de pruebas de][DevToolsA11yErrorsDemopage] accesibilidad en una pestaña nueva.</span><span class="sxs-lookup"><span data-stu-id="eaf07-124">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.</span></span>

1.  <span data-ttu-id="eaf07-125">Mantenga el mouse sobre los elementos de menú azul del menú de navegación de la barra lateral.</span><span class="sxs-lookup"><span data-stu-id="eaf07-125">Hover over the blue menu items in the sidebar navigation menu.</span></span>  <span data-ttu-id="eaf07-126">Observe que cada elemento tiene una animación.</span><span class="sxs-lookup"><span data-stu-id="eaf07-126">Notice that each item has an animation.</span></span>

    :::image type="complex" source="../media/a11y-testing-hover.msft.png" alt-text="Elemento de menú que muestra diferentes colores cuando el puntero del mouse está sobre él" lightbox="../media/a11y-testing-hover.msft.png":::
        <span data-ttu-id="eaf07-128">Elemento de menú que muestra diferentes colores cuando el puntero del mouse está sobre él</span><span class="sxs-lookup"><span data-stu-id="eaf07-128">The menu item showing different colors when the mouse pointer is over it</span></span>
    :::image-end:::
    
<span data-ttu-id="eaf07-129">Ahora, use la herramienta Inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="eaf07-129">Now, use the Inspect tool.</span></span> <span data-ttu-id="eaf07-130">Cuando se usa la herramienta Inspeccionar, las animaciones de los elementos del menú no se ejecutarán al pasar el puntero sobre ellos.</span><span class="sxs-lookup"><span data-stu-id="eaf07-130">When the Inspect tool is used, animations on the menu items won't run when you hover over them.</span></span>  <span data-ttu-id="eaf07-131">Al usar la herramienta Inspeccionar, no puede alcanzar el estado de los elementos de menú para probar la relación de contraste, ya que el estado de los estilos no `hover` `hover` se desencadena.</span><span class="sxs-lookup"><span data-stu-id="eaf07-131">When using the Inspect tool, you can't reach the `hover` state on menu items to test the contrast ratio, because the `hover` state in your styles isn't triggered.</span></span>  
    
<span data-ttu-id="eaf07-132">Para confirmar que las animaciones no se ejecutan, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="eaf07-132">To confirm that your animations don't run, perform the following steps.</span></span>
    
1.  <span data-ttu-id="eaf07-133">Seleccione el **botón Inspeccionar** \( el botón Inspeccionar \) en la esquina superior izquierda de DevTools para que el icono esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="eaf07-133">Select the **Inspect** \(![the Inspect button](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="eaf07-134">Mantenga el mouse sobre los vínculos azules del menú de navegación de la barra lateral.</span><span class="sxs-lookup"><span data-stu-id="eaf07-134">Hover over the blue links on the sidebar navigation menu.</span></span>  <span data-ttu-id="eaf07-135">Las animaciones de los elementos de menú no se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="eaf07-135">The animations for the menu items don't run.</span></span> <span data-ttu-id="eaf07-136">En su lugar, los elementos de menú se muestran con colores y resaltados para la superposición de flexbox.</span><span class="sxs-lookup"><span data-stu-id="eaf07-136">Instead, the menu items are displayed using colors and highlights for the flexbox overlay.</span></span>

<span data-ttu-id="eaf07-137">Comprobar el contraste de texto suficiente de esta manera no es suficiente, ya que los elementos de la página podrían tener estados diferentes.</span><span class="sxs-lookup"><span data-stu-id="eaf07-137">Checking for sufficient text contrast this way isn't enough, because the elements on the page could have different states.</span></span>


## <a name="use-state-simulation-to-simulate-the-hover-state-of-an-animated-menu-item"></a><span data-ttu-id="eaf07-138">Usar la simulación de estado para simular el estado de desplazamiento de un elemento de menú animado</span><span class="sxs-lookup"><span data-stu-id="eaf07-138">Use state simulation to simulate the hover state of an animated menu item</span></span> 

<!-- Elements tool: Styles pane: Toggle Element State -->

<span data-ttu-id="eaf07-139">Cuando la **herramienta Inspeccionar** está activa, en lugar de pasar el mouse sobre un elemento animado, debe simular el estado del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="eaf07-139">When the **Inspect** tool is active, instead of hovering over an animated element, you need to simulate the state of the menu item.</span></span>  <span data-ttu-id="eaf07-140">Para simular el estado de un elemento de menú, use la simulación de estado en el **panel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="eaf07-140">To simulate the state of a menu item, use the state simulation in the **Styles** pane.</span></span>  <span data-ttu-id="eaf07-141">El **panel Estilos** tiene un botón **\:hov** (**Toggle Element State**), que muestra un grupo de casillas con la etiqueta Force **element state**.</span><span class="sxs-lookup"><span data-stu-id="eaf07-141">The **Styles** pane has a **\:hov** (**Toggle Element State**) button, which displays a group of checkboxes labeled **Force element state**.</span></span>

<span data-ttu-id="eaf07-142">Para activar el estado del mouse mientras se usa la herramienta Inspeccionar:</span><span class="sxs-lookup"><span data-stu-id="eaf07-142">To turn on the hover state while using the Inspect tool:</span></span>

1.  <span data-ttu-id="eaf07-143">Si aún no está abierto, abra la página web de demostración [de][DevToolsA11yErrorsDemopage] pruebas de accesibilidad en una nueva pestaña.  A **continuación, seleccione F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="eaf07-143">If it's not open already, open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="eaf07-144">Seleccione el **botón Inspeccionar** \( Inspeccionar botón de herramienta \) en la esquina superior izquierda de DevTools para que el icono esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="eaf07-144">Select the **Inspect** \(![Inspect tool button](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="eaf07-145">En la página web representada, seleccione el vínculo **azul Gatos** en el menú de navegación de la barra lateral.</span><span class="sxs-lookup"><span data-stu-id="eaf07-145">In the rendered webpage, select the blue **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="eaf07-146">Se **abre** la herramienta Elementos, con el elemento `<a href="#cats">Cats</a>` seleccionado.</span><span class="sxs-lookup"><span data-stu-id="eaf07-146">The **Elements** tool opens, with the element `<a href="#cats">Cats</a>` selected.</span></span>

    :::image type="complex" source="../media/a11y-testing-inspecting-link-to-hover.msft.png" alt-text="Inspeccionar el elemento que tiene un estado de puntero en la herramienta Elementos" lightbox="../media/a11y-testing-inspecting-link-to-hover.msft.png":::
        <span data-ttu-id="eaf07-148">Inspeccionar el elemento que tiene un estado de puntero en la herramienta Elementos</span><span class="sxs-lookup"><span data-stu-id="eaf07-148">Inspecting the element that has a hover state in the Elements tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="eaf07-149">Seleccione la **pestaña Estilos.**  El elemento seleccionado tiene un estado en el CSS que se aplica a él, pero que no `a` está visible en el panel `hover` **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="eaf07-149">Select the **Styles** tab.  The selected `a` element has a `hover` state in the CSS that is applied to it, but that's not visible in the **Styles** pane.</span></span> 

1.  <span data-ttu-id="eaf07-150">En el **panel Estilos,** a la derecha de la regla de `#sidebar nav li a` estilo, seleccione el `styles.css` vínculo.</span><span class="sxs-lookup"><span data-stu-id="eaf07-150">In the **Styles** pane, to the right of the style rule `#sidebar nav li a`, select the `styles.css` link.</span></span>  <span data-ttu-id="eaf07-151">Se **abre la herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="eaf07-151">The **Sources** tool opens.</span></span>  <span data-ttu-id="eaf07-152">A continuación, busque la regla de pseudo-clase CSS `#sidebar nav li a:hover` .</span><span class="sxs-lookup"><span data-stu-id="eaf07-152">Then find the CSS pseudo-class rule `#sidebar nav li a:hover`.</span></span>  <span data-ttu-id="eaf07-153">Esta regla no se ejecuta cuando la **herramienta Inspeccionar** está activa.</span><span class="sxs-lookup"><span data-stu-id="eaf07-153">This rule doesn't run when the **Inspect** tool is active.</span></span>  <span data-ttu-id="eaf07-154">Simularemos la ejecución de esta regla de estado en los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="eaf07-154">We'll simulate running this state rule in the next steps.</span></span>

1.  <span data-ttu-id="eaf07-155">Seleccione la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="eaf07-155">Select the **Elements** tool.</span></span>  <span data-ttu-id="eaf07-156">A continuación, en el panel **Estilos,** seleccione **el botón :hov** (**Toggle Element State**).</span><span class="sxs-lookup"><span data-stu-id="eaf07-156">Then in the **Styles** pane, select the **:hov** (**Toggle Element State**) button.</span></span>  <span data-ttu-id="eaf07-157">Se **muestra el grupo de** casillas De estado del elemento Force.</span><span class="sxs-lookup"><span data-stu-id="eaf07-157">The **Force element state** group of checkboxes is displayed.</span></span>

    :::image type="complex" source="../media/a11y-testing-state-simulation.msft.png" alt-text="La herramienta de simulación de estado que muestra todas las opciones" lightbox="../media/a11y-testing-state-simulation.msft.png":::
        <span data-ttu-id="eaf07-159">La herramienta de simulación de estado que muestra todas las opciones</span><span class="sxs-lookup"><span data-stu-id="eaf07-159">The state simulation tool showing all the options</span></span>
    :::image-end:::

1.  <span data-ttu-id="eaf07-160">Active la **casilla :hover.**</span><span class="sxs-lookup"><span data-stu-id="eaf07-160">Select the **:hover** checkbox.</span></span>  <span data-ttu-id="eaf07-161">En el DOM, a la izquierda del elemento, aparece un punto amarillo que indica que el `<a href="#cats">Cats</a>` elemento tiene un estado simulado.</span><span class="sxs-lookup"><span data-stu-id="eaf07-161">In the DOM, to the left of the element `<a href="#cats">Cats</a>`, a yellow dot appears, indicating that the element has a simulated state.</span></span>  <span data-ttu-id="eaf07-162">El **elemento de** menú Gatos ahora aparece en la página web como si el puntero estuviera sobre él.</span><span class="sxs-lookup"><span data-stu-id="eaf07-162">The **Cats** menu item now appears in the webpage as if the pointer were hovering over it.</span></span>  <span data-ttu-id="eaf07-163">Es posible que se ejecute la animación en el elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="eaf07-163">The animation on the menu item might run.</span></span>

    :::image type="complex" source="../media/a11y-testing-hover-simulated.msft.png" alt-text="DevTools simulando un estado de puntero" lightbox="../media/a11y-testing-hover-simulated.msft.png":::
        <span data-ttu-id="eaf07-165">DevTools simulando un estado de puntero</span><span class="sxs-lookup"><span data-stu-id="eaf07-165">DevTools simulating a hover state</span></span>
    :::image-end:::

    <span data-ttu-id="eaf07-166">Después de aplicar el estado simulado, puede volver a usar la herramienta **Inspeccionar** para comprobar el contraste del elemento cuando el usuario mantiene el mouse sobre él, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="eaf07-166">After the simulated state is applied, you can use the **Inspect** tool again to check the contrast of the element when the user hovers over it, as follows.</span></span>

1.  <span data-ttu-id="eaf07-167">Seleccione el **botón Inspeccionar** \( Icono inspector \) en la esquina superior izquierda de DevTools para que el icono esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="eaf07-167">Select the **Inspect** \(![Inspector icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="eaf07-168">Mantenga el mouse sobre el vínculo **azul Gatos** en el menú de navegación de la barra lateral.</span><span class="sxs-lookup"><span data-stu-id="eaf07-168">Hover over the blue **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="eaf07-169">El vínculo ahora es azul claro, debido a la animación de desplazamiento simulada.</span><span class="sxs-lookup"><span data-stu-id="eaf07-169">The link is now light blue, because of the simulated hover animation.</span></span>  <span data-ttu-id="eaf07-170">Aparece **la** superposición de información de la herramienta \*\*\*\* Inspeccionar, que muestra un signo de exclamación naranja en la fila Contraste, lo que indica que el contraste no es lo suficientemente alto.</span><span class="sxs-lookup"><span data-stu-id="eaf07-170">The **Inspect** tool's information overlay appears, showing an orange exclamation point in the **Contrast** row, indicating that the contrast isn't high enough.</span></span>

    :::image type="complex" source="../media/a11y-testing-hover-contrast-testing.msft.png" alt-text="Probar el contraste de un elemento en un estado de puntero simulado" lightbox="../media/a11y-testing-hover-contrast-testing.msft.png":::
        <span data-ttu-id="eaf07-172">Probar el contraste de un elemento en un estado de puntero simulado</span><span class="sxs-lookup"><span data-stu-id="eaf07-172">Testing the contrast of an element in a simulated hover state</span></span>
    :::image-end:::

<span data-ttu-id="eaf07-173">La simulación de estado también es una buena forma de comprobar si se han considerado diferentes necesidades de usuario, como las necesidades de los usuarios de teclado.</span><span class="sxs-lookup"><span data-stu-id="eaf07-173">State simulation is also a good way to check whether you considered different user needs, such as the needs of keyboard users.</span></span>  <span data-ttu-id="eaf07-174">Al usar las casillas De estado **del** elemento Force, puedes simular el estado para detectar que la interfaz de usuario permanece sin cambios `:focus` cuando tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="eaf07-174">By using the **Force element state** checkboxes, you can simulate the `:focus` state to discover that the UI remains unchanged when it has focus.</span></span> <span data-ttu-id="eaf07-175">Esta falta de un indicador cuando un elemento tiene el foco es un problema.</span><span class="sxs-lookup"><span data-stu-id="eaf07-175">This lack of an indicator when an element has focus is a problem.</span></span>


## <a name="see-also"></a><span data-ttu-id="eaf07-176">Consulta también</span><span class="sxs-lookup"><span data-stu-id="eaf07-176">See also</span></span>

*  [<span data-ttu-id="eaf07-177">Información general sobre las pruebas de accesibilidad con DevTools</span><span class="sxs-lookup"><span data-stu-id="eaf07-177">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="eaf07-178">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="eaf07-178">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

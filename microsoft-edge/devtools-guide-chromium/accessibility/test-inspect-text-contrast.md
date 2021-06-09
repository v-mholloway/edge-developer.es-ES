---
description: Compruebe el contraste de color de texto en el estado predeterminado mediante la superposición de información de la herramienta Inspeccionar en la página, que tiene una sección Accesibilidad que incluye información de contraste.
title: Comprobar el contraste de color de texto en el estado predeterminado con la herramienta Inspeccionar
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ade9fd6d685f6f7cea6311b1645a527ece352a38
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597656"
---
# <a name="check-text-color-contrast-in-the-default-state-using-the-inspect-tool"></a><span data-ttu-id="37e4f-104">Comprobar el contraste de color de texto en el estado predeterminado con la herramienta Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="37e4f-104">Check text-color contrast in the default state using the Inspect tool</span></span>

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

<span data-ttu-id="37e4f-105">Compruebe el contraste de color del texto en el estado predeterminado mediante la **herramienta Inspeccionar.**</span><span class="sxs-lookup"><span data-stu-id="37e4f-105">Check text color contrast in the default state by using the **Inspect** tool.</span></span>  <span data-ttu-id="37e4f-106">La **superposición** de información de la herramienta Inspeccionar en la página web tiene una sección **Accesibilidad** que incluye información **de** contraste.</span><span class="sxs-lookup"><span data-stu-id="37e4f-106">The **Inspect** tool's information overlay on the webpage has an **Accessibility** section that includes **Contrast** information.</span></span>

<span data-ttu-id="37e4f-107">Para comprobar el contraste de color de texto en el estado predeterminado mediante la superposición de información de la herramienta Inspeccionar, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="37e4f-107">To check text-color contrast in the default state using the Inspect tool's information overlay, perform the following steps.</span></span>

<!-- Inspect tool -->
<span data-ttu-id="37e4f-108">Para los elementos que tienen texto, **la superposición de** información de la herramienta Inspeccionar muestra lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="37e4f-108">For elements that have text, the **Inspect** tool's information overlay shows the following:</span></span>
*  <span data-ttu-id="37e4f-109">Relación de contraste de texto frente a colores de fondo.</span><span class="sxs-lookup"><span data-stu-id="37e4f-109">The contrast ratio of text versus background colors.</span></span>
*  <span data-ttu-id="37e4f-110">Icono de marca de verificación verde para elementos con contraste suficiente.</span><span class="sxs-lookup"><span data-stu-id="37e4f-110">A green check mark icon for elements with enough contrast.</span></span>
*  <span data-ttu-id="37e4f-111">Icono de alerta amarilla para elementos que no tienen suficiente contraste.</span><span class="sxs-lookup"><span data-stu-id="37e4f-111">A yellow alert icon for elements that don't have enough contrast.</span></span>

<span data-ttu-id="37e4f-112">En algunos casos, el contraste se ve afectado al establecer el explorador en tema claro u tema oscuro.</span><span class="sxs-lookup"><span data-stu-id="37e4f-112">In some cases, contrast is affected by setting the browser to light theme or dark theme.</span></span>

<span data-ttu-id="37e4f-113">Por ejemplo, en la página de demostración, los vínculos azules \*\*\*\* del menú \*\*\*\* de navegación de la barra lateral tienen suficiente contraste, pero el vínculo verde Perros de la sección Estado de la donación no tiene suficiente contraste.</span><span class="sxs-lookup"><span data-stu-id="37e4f-113">As an example, on the demo page, the blue links of the sidebar navigation menu have enough contrast, but the green **Dogs** link in the **Donation status** section does not have enough contrast.</span></span>  <span data-ttu-id="37e4f-114">Revise esos elementos con **la herramienta Inspeccionar,** como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="37e4f-114">Review those elements using the **Inspect** tool, as follows:</span></span>

1.  <span data-ttu-id="37e4f-115">Abra la [página web de demostración de pruebas de][DevToolsA11yErrorsDemopage] accesibilidad en una pestaña nueva.  A **continuación, seleccione F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="37e4f-115">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="37e4f-116">Seleccione el **botón Inspeccionar** \( Botón Inspeccionar \) en la esquina superior izquierda de DevTools para que el icono esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="37e4f-116">Select the **Inspect** \(![Inspect button](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="37e4f-117">En la página web que se representa, mantenga el mouse sobre el vínculo **azul Gatos** del menú de navegación de la barra lateral.</span><span class="sxs-lookup"><span data-stu-id="37e4f-117">In the rendered webpage, hover over the blue **Cats** link of the sidebar navigation menu.</span></span>  <span data-ttu-id="37e4f-118">Aparece **la superposición** de información de la herramienta Inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="37e4f-118">The **Inspect** tool's information overlay appears.</span></span>  <span data-ttu-id="37e4f-119">En la **sección Accesibilidad** de la superposición de \*\*\*\* información, aparece una marca de verificación verde en la fila Contraste, que indica que este elemento tiene suficiente contraste de color de texto frente al color de fondo.</span><span class="sxs-lookup"><span data-stu-id="37e4f-119">In the **Accessibility** section of the information overlay, a green checkmark appears on the **Contrast** row, indicating that this element has enough contrast of text color versus background color.</span></span>

    :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Los elementos de menú tienen suficiente contraste, como se muestra en la herramienta Inspeccionar" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
        <span data-ttu-id="37e4f-121">Los elementos de menú tienen suficiente contraste, como se muestra en la herramienta Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="37e4f-121">The menu items have enough contrast, as shown in the Inspect tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="37e4f-122">En la página web que se representa, en la sección **Estado de** la donación, mantenga el mouse sobre el **vínculo** Perros.</span><span class="sxs-lookup"><span data-stu-id="37e4f-122">In the rendered webpage, in the **Donation Status** section, hover over the **Dogs** link.</span></span>  <span data-ttu-id="37e4f-123">La **superposición** de información de la herramienta Inspeccionar muestra un signo de exclamación naranja en la fila **Contraste,** lo que indica que este elemento no tiene suficiente contraste de texto frente a los colores de fondo.</span><span class="sxs-lookup"><span data-stu-id="37e4f-123">The **Inspect** tool's information overlay shows an orange exclamation point on the **Contrast** row, indicating that this element doesn't have enough contrast of text versus background colors.</span></span>

    :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Un elemento que no tiene suficiente contraste, como se muestra en la advertencia de la herramienta Inspeccionar" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
        <span data-ttu-id="37e4f-125">Un elemento que no tiene suficiente contraste, como se muestra en la advertencia de la herramienta Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="37e4f-125">An element that doesn't have enough contrast, as shown by the warning in the Inspect tool</span></span>
    :::image-end:::


## <a name="different-options-to-inspect-text-color-contrast-in-devtools"></a><span data-ttu-id="37e4f-126">Diferentes opciones para inspeccionar el contraste de color de texto en DevTools</span><span class="sxs-lookup"><span data-stu-id="37e4f-126">Different options to inspect text-color contrast in DevTools</span></span>

<span data-ttu-id="37e4f-127">Use las siguientes características de DevTools para inspeccionar el contraste de color de texto.</span><span class="sxs-lookup"><span data-stu-id="37e4f-127">Use the following DevTools features to inspect text-color contrast.</span></span>

*  <span data-ttu-id="37e4f-128">Use la **herramienta Inspeccionar** (como superposición de información en la página web) para comprobar si un elemento de página individual tiene suficiente contraste de color de texto.</span><span class="sxs-lookup"><span data-stu-id="37e4f-128">Use the **Inspect** tool (as an information overlay on the webpage) to check whether an individual page element has enough text-color contrast.</span></span>  <span data-ttu-id="37e4f-129">La **superposición** de información de la herramienta Inspeccionar incluye una sección **Accesibilidad** que tiene una fila **información** de contraste.</span><span class="sxs-lookup"><span data-stu-id="37e4f-129">The **Inspect** tool's information overlay includes an **Accessibility** section that has a **Contrast** information row.</span></span>  <span data-ttu-id="37e4f-130">La **herramienta Inspeccionar** solo muestra información de contraste de texto para el estado actual.</span><span class="sxs-lookup"><span data-stu-id="37e4f-130">The **Inspect** tool only shows text-contrast information for the current state.</span></span>  <span data-ttu-id="37e4f-131">Este enfoque se describe en el artículo actual.</span><span class="sxs-lookup"><span data-stu-id="37e4f-131">This approach is described in the current article.</span></span>

*  <span data-ttu-id="37e4f-132">La **herramienta Problemas** notifica automáticamente cualquier problema de contraste de color para toda la página web, cuando el texto y el color de fondo no contrastan lo suficiente.</span><span class="sxs-lookup"><span data-stu-id="37e4f-132">The **Issues** tool automatically reports any color-contrast issues for the entire webpage, when text and background color don't contrast enough.</span></span>  <span data-ttu-id="37e4f-133">Este enfoque se describe en [Verify that text colors have enough contrast](test-issues-tool.md#verify-that-text-colors-have-enough-contrast).</span><span class="sxs-lookup"><span data-stu-id="37e4f-133">This approach is described in [Verify that text colors have enough contrast](test-issues-tool.md#verify-that-text-colors-have-enough-contrast).</span></span>

*  <span data-ttu-id="37e4f-134">Emular un estado no predeterminado, como el estado, mediante el uso del estado de elemento Toggle en el panel Estilos, descrito en `hover` [Verify accessibility of all states of elements](test-inspect-states.md). \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="37e4f-134">Emulate a non-default state, such as the `hover` state, by using **Toggle Element State** in the **Styles** pane, described in [Verify accessibility of all states of elements](test-inspect-states.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="37e4f-135">Consulta también</span><span class="sxs-lookup"><span data-stu-id="37e4f-135">See also</span></span>

*  [<span data-ttu-id="37e4f-136">Comprobar la accesibilidad de todos los estados de elementos</span><span class="sxs-lookup"><span data-stu-id="37e4f-136">Verify accessibility of all states of elements</span></span>][DevtoolsAccessibilityTestInspectStates]
*  [<span data-ttu-id="37e4f-137">Usar la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar el puntero sobre la página web</span><span class="sxs-lookup"><span data-stu-id="37e4f-137">Use the Inspect tool to detect accessibility issues by hovering over the webpage</span></span>](test-inspect-tool.md)
*  [<span data-ttu-id="37e4f-138">Información general sobre las pruebas de accesibilidad con DevTools</span><span class="sxs-lookup"><span data-stu-id="37e4f-138">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="37e4f-139">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="37e4f-139">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityTestInspectStates]: test-inspect-states.md "Comprobar la accesibilidad de todos los estados de elementos | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

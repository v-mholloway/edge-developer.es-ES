---
description: Compruebe si hay problemas de contraste con el tema oscuro y el tema claro (para el modo oscuro y el modo claro) mediante la lista desplegable \"Emular la característica multimedia CSS prefers-color-scheme\" en la herramienta de representación.
title: Comprobar si hay problemas de contraste con el tema oscuro y el tema claro
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 052c75b610ec872329f387e46819867f299a8ca9
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597690"
---
# <a name="check-for-contrast-issues-with-dark-theme-and-light-theme"></a><span data-ttu-id="d55f2-104">Comprobar si hay problemas de contraste con el tema oscuro y el tema claro</span><span class="sxs-lookup"><span data-stu-id="d55f2-104">Check for contrast issues with dark theme and light theme</span></span>

<!-- Rendering tool: Emulate CSS media feature prefers-color-scheme -->

<span data-ttu-id="d55f2-105">Al probar la accesibilidad de color, puede haber diferentes temas de color para mostrar que necesita probar para problemas de contraste.</span><span class="sxs-lookup"><span data-stu-id="d55f2-105">When testing color accessibility, there could be different display color themes that you need to test for contrast issues.</span></span>

<span data-ttu-id="d55f2-106">La mayoría de los sistemas operativos vienen con un modo oscuro y un modo claro.</span><span class="sxs-lookup"><span data-stu-id="d55f2-106">Most operating systems come with a dark mode and a light mode.</span></span>  <span data-ttu-id="d55f2-107">La página web puede reaccionar a esta configuración del sistema operativo mediante una consulta multimedia CSS.</span><span class="sxs-lookup"><span data-stu-id="d55f2-107">Your webpage can react to this operating system setting, by using a CSS media query.</span></span>  <span data-ttu-id="d55f2-108">Puede probar estos temas y probar la consulta multimedia CSS sin tener que cambiar la configuración del sistema operativo mediante las opciones `prefers-color-scheme` CSS de la herramienta **de** representación.</span><span class="sxs-lookup"><span data-stu-id="d55f2-108">You can test these themes and test your CSS media query without having to change your operating system setting, by using the `prefers-color-scheme` CSS options in the **Rendering** tool.</span></span>

<span data-ttu-id="d55f2-109">Por ejemplo, la página de demostración de pruebas de accesibilidad incluye un tema claro y un tema oscuro.</span><span class="sxs-lookup"><span data-stu-id="d55f2-109">As an example, the accessibility-testing demo page includes a light theme and a dark theme.</span></span>  <span data-ttu-id="d55f2-110">La página de demostración hereda la configuración del tema oscuro o claro del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d55f2-110">The demo page inherits the dark or light theme setting from the operating system.</span></span>  <span data-ttu-id="d55f2-111">Si usamos DevTools para simular el sistema operativo que se va \*\*\*\* a establecer en un esquema de luz y, a continuación, actualizar la página web de demostración, la herramienta Problemas muestra seis problemas de contraste de color en lugar de dos.</span><span class="sxs-lookup"><span data-stu-id="d55f2-111">If we use DevTools to simulate the operating system being set to a light scheme and then refresh the demo webpage, the **Issues** tool shows six color-contrast problems instead of two.</span></span>  <span data-ttu-id="d55f2-112">(Es posible que vea números diferentes).</span><span class="sxs-lookup"><span data-stu-id="d55f2-112">(You might see different numbers.)</span></span>


<span data-ttu-id="d55f2-113">Para emular la selección de un usuario del tema de color preferido:</span><span class="sxs-lookup"><span data-stu-id="d55f2-113">To emulate a user's selection of preferred color theme:</span></span>

1.  <span data-ttu-id="d55f2-114">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="d55f2-114">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="d55f2-115">Seleccione **Esc** para abrir el cajón en la parte inferior de DevTools.</span><span class="sxs-lookup"><span data-stu-id="d55f2-115">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="d55f2-116">Seleccione el icono en la parte superior del cajón para ver la lista de herramientas y, a **+** continuación, seleccione **Representación**.</span><span class="sxs-lookup"><span data-stu-id="d55f2-116">Select the **+** icon at the top of the Drawer to see the list of tools, and then select **Rendering**.</span></span>  <span data-ttu-id="d55f2-117">Aparece la herramienta de representación.</span><span class="sxs-lookup"><span data-stu-id="d55f2-117">The Rendering tool appears.</span></span>

1.  <span data-ttu-id="d55f2-118">En la lista desplegable Emular elementos **multimedia CSS prefers-color-scheme,** seleccione **prefers-color-scheme: light**.</span><span class="sxs-lookup"><span data-stu-id="d55f2-118">In the **Emulate CSS media feature prefers-color-scheme** dropdown list, select **prefers-color-scheme: light**.</span></span>      <span data-ttu-id="d55f2-119">La página web se vuelve a representar mediante `light-theme.css` .</span><span class="sxs-lookup"><span data-stu-id="d55f2-119">The webpage is re-rendered using `light-theme.css`.</span></span>


    :::image type="complex" source="../media/a11y-testing-simulating-light-mode.msft.png" alt-text="Uso de la herramienta de representación para simular un modo de luz y desencadenar el otro tema del documento" lightbox="../media/a11y-testing-simulating-light-mode.msft.png":::
        <span data-ttu-id="d55f2-121">Uso de la herramienta de representación para simular un modo de luz y desencadenar el otro tema del documento</span><span class="sxs-lookup"><span data-stu-id="d55f2-121">Using the Rendering tool to simulate a light mode and triggering the other theme of the document</span></span>
    :::image-end:::


1.  <span data-ttu-id="d55f2-122">Seleccione la **herramienta Problemas** y, a continuación, expanda la **sección Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="d55f2-122">Select the **Issues** tool, and then expand the **Accessibility** section.</span></span>  <span data-ttu-id="d55f2-123">Dependiendo de varios factores, es posible que reciba `Insufficient color contrast` advertencias.</span><span class="sxs-lookup"><span data-stu-id="d55f2-123">Depending on various factors, you might get `Insufficient color contrast` warnings.</span></span> <span data-ttu-id="d55f2-124">Observe que **en RECURSOS AFECTADOS** hay 6 elementos con contraste de color insuficiente.</span><span class="sxs-lookup"><span data-stu-id="d55f2-124">Notice in **AFFECTED RESOURCES** there are 6 elements with insufficient color contrast.</span></span>
    
    :::image type="complex" source="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png" alt-text="Nuevos problemas de contraste detectados debido al cambio al tema claro" lightbox="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png":::
        <span data-ttu-id="d55f2-126">Nuevos problemas de contraste detectados debido al cambio al tema claro</span><span class="sxs-lookup"><span data-stu-id="d55f2-126">New contrast issues detected because of the change to light theme</span></span>
    :::image-end:::
    
    <span data-ttu-id="d55f2-127">En nuestra página de demostración, la sección **Estado de** donación de la página es ilegible en modo claro y debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="d55f2-127">On our demo page, the **Donation status** section of the page is unreadable in light mode, and needs to change.</span></span> 
    
    :::image type="complex" source="../media/a11y-testing-donation-state-light-contrast.msft.png" alt-text="La sección Estado de donación tiene problemas de contraste en modo claro" lightbox="../media/a11y-testing-donation-state-light-contrast.msft.png":::
        <span data-ttu-id="d55f2-129">La **sección Estado de donación** tiene problemas de contraste en modo claro</span><span class="sxs-lookup"><span data-stu-id="d55f2-129">The **Donation Status** section has contrast issues in light mode</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="d55f2-130">En DevTools, seleccione la **herramienta Elementos** y, a continuación, **seleccione Ctrl+F** en Windows/Linux o **Command+F** en macOS.</span><span class="sxs-lookup"><span data-stu-id="d55f2-130">In DevTools, select the **Elements** tool, and then select **Ctrl+F** on Windows/Linux or **Command+F** on macOS.</span></span>  <span data-ttu-id="d55f2-131">Aparece **el cuadro** de texto Buscar, para buscar en el árbol DOM HTML.</span><span class="sxs-lookup"><span data-stu-id="d55f2-131">The **Find** textbox appears, to search within the HTML DOM tree.</span></span>
 
1.  <span data-ttu-id="d55f2-132">Escriba `scheme` .</span><span class="sxs-lookup"><span data-stu-id="d55f2-132">Enter `scheme`.</span></span>  <span data-ttu-id="d55f2-133">Se encuentran las siguientes consultas multimedia CSS y ahora se pueden actualizar los archivos CSS correspondientes.</span><span class="sxs-lookup"><span data-stu-id="d55f2-133">The following CSS media queries are found, and the corresponding CSS files can now be updated.</span></span>

    ```html
    <link rel="stylesheet" href="css/light-theme.css" media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)">
    <link rel="stylesheet" href="css/dark-theme.css" media="(prefers-color-scheme: dark)">
    ```


## <a name="see-also"></a><span data-ttu-id="d55f2-134">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d55f2-134">See also</span></span>

*  [<span data-ttu-id="d55f2-135">Simulación de combinación de colores claros o oscuros</span><span class="sxs-lookup"><span data-stu-id="d55f2-135">Dark or light color scheme simulation</span></span>][DevToolsColorSchemeSimulation]
*  [<span data-ttu-id="d55f2-136">Información general sobre las pruebas de accesibilidad con DevTools</span><span class="sxs-lookup"><span data-stu-id="d55f2-136">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="d55f2-137">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d55f2-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsColorSchemeSimulation]: ./preferred-color-scheme-simulation.md "Simulación de combinación de colores claros o | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

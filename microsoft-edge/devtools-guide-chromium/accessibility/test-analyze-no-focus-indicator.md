---
description: Analizar la falta de indicación del foco del teclado en un menú de barra lateral, debido a la falta de una regla de pseudo-clase CSS para el estado de foco en un vínculo, combinado con el vínculo sin configuración de esquema.
title: Analizar la falta de indicación del foco del teclado en un menú lateral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 3626de9bdc2cce266efafe4b1b2e8fff501a74f7
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597704"
---
# <a name="analyze-the-lack-of-indication-of-keyboard-focus-in-a-sidebar-menu"></a><span data-ttu-id="85660-104">Analizar la falta de indicación del foco del teclado en un menú lateral</span><span class="sxs-lookup"><span data-stu-id="85660-104">Analyze the lack of indication of keyboard focus in a sidebar menu</span></span>

<!-- Inspect tool, and CSS rules: pseudo-classes for states -->

<span data-ttu-id="85660-105">En la página de demostración de pruebas de accesibilidad, el menú de navegación de la barra lateral con vínculos azules no indica visualmente qué vínculo tiene el foco al usar un teclado.</span><span class="sxs-lookup"><span data-stu-id="85660-105">In the accessibility-testing demo page, the sidebar navigation menu with blue links doesn't visually indicate which link has focus, when using a keyboard.</span></span>  <span data-ttu-id="85660-106">Para averiguar por qué el menú de la barra lateral es confuso para los usuarios de teclado, buscaremos reglas de pseudo-clase CSS para los estados y, junto con la propiedad CSS, para los esquemas `hover` `focus` de vínculo.</span><span class="sxs-lookup"><span data-stu-id="85660-106">To find out why the sidebar menu is confusing to keyboard users, we'll look for CSS pseudo-class rules for the `hover` and `focus` states, along with the CSS property for link outlines.</span></span>  

<span data-ttu-id="85660-107">Este análisis encuentra que la falta de indicación del foco del teclado en los vínculos del menú de navegación de la barra lateral se debe a:</span><span class="sxs-lookup"><span data-stu-id="85660-107">This analysis finds that the lack of indication of keyboard focus in the links of the sidebar navigation menu is because:</span></span>
*  <span data-ttu-id="85660-108">Los `a` vínculos tienen una configuración de propiedad CSS de `outline: none` .</span><span class="sxs-lookup"><span data-stu-id="85660-108">The `a` links have a CSS property setting of `outline: none`.</span></span>
*  <span data-ttu-id="85660-109">Los `a` vínculos carecen de una regla de pseudo-clase CSS para el `:focus` estado.</span><span class="sxs-lookup"><span data-stu-id="85660-109">The `a` links lack a CSS pseudo-class rule for the `:focus` state.</span></span>

<span data-ttu-id="85660-110">Para navegar al CSS, usaremos la herramienta **Inspeccionar** para resaltar un vínculo azul en el menú de navegación de la barra lateral y, a continuación, veremos el árbol DOM y CSS para el elemento que define ese `a` vínculo.</span><span class="sxs-lookup"><span data-stu-id="85660-110">To navigate to the CSS, we'll use the **Inspect** tool to highlight a blue link on the sidebar navigation menu, and then view the DOM tree and CSS for the `a` element that defines that link.</span></span>

1.  <span data-ttu-id="85660-111">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="85660-111">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="85660-112">Seleccione el **botón Inspeccionar** \( Inspeccionar icono \) en la esquina superior izquierda de DevTools para que el botón esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="85660-112">Select the **Inspect** \(![Inspect icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="85660-113">Mantenga el mouse sobre el vínculo **azul Gatos** en el menú de navegación de la barra lateral.</span><span class="sxs-lookup"><span data-stu-id="85660-113">Hover over the blue **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="85660-114">Aparece la superposición Inspeccionar, que muestra que el elemento puede centrarse `a` en el teclado.</span><span class="sxs-lookup"><span data-stu-id="85660-114">The Inspect overlay appears, showing that the `a` element is keyboard-focusable.</span></span>  <span data-ttu-id="85660-115">Pero la superposición no muestra que no hay ninguna indicación visual cuando el vínculo tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="85660-115">But the overlay doesn't show that there's no visual indication when the link has focus.</span></span>

    <span data-ttu-id="85660-116">A continuación, inspeccionaremos el estilo CSS de este vínculo.</span><span class="sxs-lookup"><span data-stu-id="85660-116">Next, we'll inspect the CSS styling of this link.</span></span>
 
1.  <span data-ttu-id="85660-117">Selecciona el **vínculo Gatos** en el menú de navegación de la barra lateral.</span><span class="sxs-lookup"><span data-stu-id="85660-117">Select the **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="85660-118">La **herramienta Inspeccionar** se desactiva y se abre la herramienta **Elementos,** resaltando el `a` nodo en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="85660-118">The **Inspect** tool turns off, and the **Elements** tool opens, highlighting the `a` node in the DOM tree.</span></span>

1.  <span data-ttu-id="85660-119">Seleccione la **pestaña Estilos.**  Aparece la regla `#sidebar nav li a` CSS, junto con un vínculo a un número de línea en `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="85660-119">Select the **Styles** tab.  The CSS rule `#sidebar nav li a` appears, along with a link to a line number in `styles.css`.</span></span>

    :::image type="complex" source="../media/a11y-testing-menu-link.msft.png" alt-text="Inspeccionar el código fuente y los estilos aplicados de un vínculo en el menú" lightbox="../media/a11y-testing-menu-link.msft.png":::
        <span data-ttu-id="85660-121">Inspeccionar el código fuente y los estilos aplicados de un vínculo en el menú</span><span class="sxs-lookup"><span data-stu-id="85660-121">Inspecting the source code and the applied styles of a link in the menu</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="85660-122">Seleccione el vínculo al archivo CSS.</span><span class="sxs-lookup"><span data-stu-id="85660-122">Select the link to the CSS file.</span></span>  <span data-ttu-id="85660-123">El archivo CSS se abre dentro de la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="85660-123">The CSS file opens within the **Sources** tool.</span></span>

    :::image type="complex" source="../media/a11y-testing-menu-link-styles.msft.png" alt-text="Los estilos aplicados al vínculo en la herramienta Orígenes" lightbox="../media/a11y-testing-menu-link-styles.msft.png":::
        <span data-ttu-id="85660-125">Los estilos aplicados al vínculo en la herramienta Orígenes</span><span class="sxs-lookup"><span data-stu-id="85660-125">The styles applied to the link in the Sources tool</span></span>
    :::image-end:::
    
<span data-ttu-id="85660-126">Los estilos de la página tienen una regla de pseudo-clase CSS para el estado que indica el elemento de menú en el que se encuentra al `hover` usar un mouse: `#sidebar nav li a:hover` .</span><span class="sxs-lookup"><span data-stu-id="85660-126">The styles of the page have a CSS pseudo-class rule for the `hover` state that indicates which menu item you are on when you use a mouse: `#sidebar nav li a:hover`.</span></span>  <span data-ttu-id="85660-127">Sin embargo, no hay ninguna regla de pseudo class CSS para que el estado indique visualmente en qué elemento de menú está al usar `focus` un teclado, como `#sidebar nav li a:focus` .</span><span class="sxs-lookup"><span data-stu-id="85660-127">However, there is no CSS pseudo-class rule for the `focus` state to visually indicate which menu item you are on when you use a keyboard, such as `#sidebar nav li a:focus`.</span></span>

<span data-ttu-id="85660-128">Además, tenga en cuenta que los vínculos tienen una configuración de propiedad CSS de `outline: none` .</span><span class="sxs-lookup"><span data-stu-id="85660-128">Also, notice that the links have a CSS property setting of `outline: none`.</span></span>  <span data-ttu-id="85660-129">Este es un procedimiento común, para quitar el esquema que los exploradores agregan automáticamente a los elementos cuando se centran en ellos mediante un teclado.</span><span class="sxs-lookup"><span data-stu-id="85660-129">This is a common practice, to remove the outline which browsers automatically add to elements when you focus on them using a keyboard.</span></span>  <span data-ttu-id="85660-130">No usar `focus` el estilo causa confusión para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="85660-130">Not using `focus` styling causes confusion for your users.</span></span>


## <a name="see-also"></a><span data-ttu-id="85660-131">Consulta también</span><span class="sxs-lookup"><span data-stu-id="85660-131">See also</span></span> 

*  [<span data-ttu-id="85660-132">Rastrear qué elemento tiene el foco</span><span class="sxs-lookup"><span data-stu-id="85660-132">Track which element has focus</span></span>](focus.md)
*  [<span data-ttu-id="85660-133">Información general sobre las pruebas de accesibilidad con DevTools</span><span class="sxs-lookup"><span data-stu-id="85660-133">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="85660-134">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="85660-134">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

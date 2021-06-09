---
description: Comprobar la compatibilidad con el teclado y el lector de pantalla en el Árbol de accesibilidad.
title: Comprobar la compatibilidad con el teclado y el lector de pantalla en el Árbol de accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0ab5e5609485505d1ad5fa6e2fffced9af25edcb
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597705"
---
# <a name="check-the-accessibility-tree-for-keyboard-and-screen-reader-support"></a><span data-ttu-id="9993a-104">Comprobar la compatibilidad con el teclado y el lector de pantalla en el Árbol de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="9993a-104">Check the Accessibility Tree for keyboard and screen reader support</span></span>

<!-- Accessibility tab: Accessibility Tree -->

<span data-ttu-id="9993a-105">Varias características de DevTools comprueban la compatibilidad con el teclado y el lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="9993a-105">Several DevTools features check for keyboard and screen reader support.</span></span>  <span data-ttu-id="9993a-106">El uso **de la herramienta Inspeccionar** para comprobar la accesibilidad de cada elemento de página individualmente puede llevar bastante tiempo.</span><span class="sxs-lookup"><span data-stu-id="9993a-106">Using the **Inspect** tool to check the accessibility of each page element individually can become pretty time-consuming.</span></span>  <span data-ttu-id="9993a-107">Una forma alternativa de comprobar una página web es usar el árbol **de accesibilidad**.</span><span class="sxs-lookup"><span data-stu-id="9993a-107">An alternative way to check a webpage is to use the **Accessibility Tree**.</span></span>  <span data-ttu-id="9993a-108">El **Árbol de accesibilidad** indica qué información proporciona la página a la tecnología de asistencia, como los lectores de pantalla.</span><span class="sxs-lookup"><span data-stu-id="9993a-108">The **Accessibility Tree** indicates what information the page provides to assistive technology such as screen readers.</span></span>

<span data-ttu-id="9993a-109">El **árbol de accesibilidad** es un subconjunto del árbol DOM, que contiene elementos del árbol DOM que son relevantes y útiles para mostrar el contenido de una página en un lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="9993a-109">The **Accessibility Tree** is a subset of the DOM tree, which contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  <span data-ttu-id="9993a-110">El **árbol de accesibilidad** está en la pestaña **Accesibilidad** de la **herramienta Elementos** (cerca de la **pestaña** Estilos).</span><span class="sxs-lookup"><span data-stu-id="9993a-110">The **Accessibility Tree** is in the **Accessibility** tab of the **Elements** tool (near the **Styles** tab).</span></span>


<span data-ttu-id="9993a-111">Para explorar el uso del árbol de accesibilidad con la página de demostración:</span><span class="sxs-lookup"><span data-stu-id="9993a-111">To explore using the Accessibility Tree with the demo page:</span></span>

1.  <span data-ttu-id="9993a-112">Abra la [página web de demostración de pruebas de][DevToolsA11yErrorsDemopage] accesibilidad en una pestaña nueva.  A **continuación, seleccione F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="9993a-112">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="9993a-113">Seleccione el **botón Inspeccionar** \( el icono Inspeccionar \) de la esquina superior izquierda de DevTools para que el botón esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="9993a-113">Select the **Inspect** \(![the Inspect icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="9993a-114">En la página web que se representa, en la **sección Donación,** mantenga el mouse sobre el **botón 100.**</span><span class="sxs-lookup"><span data-stu-id="9993a-114">In the rendered webpage, in the **Donation** section, hover over the **100** button.</span></span>  <span data-ttu-id="9993a-115">Aparece **la superposición** de la herramienta Inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="9993a-115">The **Inspect** tool overlay appears.</span></span>

1.  <span data-ttu-id="9993a-116">En la página web representada, seleccione el **botón 100.**</span><span class="sxs-lookup"><span data-stu-id="9993a-116">In the rendered webpage, select the **100** button.</span></span>  <span data-ttu-id="9993a-117">En DevTools, se muestra **la** herramienta Elementos.</span><span class="sxs-lookup"><span data-stu-id="9993a-117">In DevTools, the **Elements** tool is displayed.</span></span>  <span data-ttu-id="9993a-118">El árbol DOM muestra el `div` elemento del **botón 100.**</span><span class="sxs-lookup"><span data-stu-id="9993a-118">The DOM tree shows the `div` element for the **100** button.</span></span>  <span data-ttu-id="9993a-119">El **panel Estilos** muestra la configuración CSS del elemento.</span><span class="sxs-lookup"><span data-stu-id="9993a-119">The **Styles** pane shows the CSS settings for the element.</span></span>

1.  <span data-ttu-id="9993a-120">A la derecha de la **pestaña Estilos,** seleccione la **pestaña Accesibilidad.**  Se **muestra el árbol de** accesibilidad del elemento y se expande.</span><span class="sxs-lookup"><span data-stu-id="9993a-120">To the right of the **Styles** tab, select the **Accessibility** tab.  The **Accessibility Tree** for the element is displayed, and is expanded.</span></span>

:::image type="complex" source="../media/a11y-testing-accessibility-tree.msft.png" alt-text="Botón formulario de donación en la herramienta Árbol de accesibilidad" lightbox="../media/a11y-testing-accessibility-tree.msft.png":::
    <span data-ttu-id="9993a-122">Botón formulario de donación en la herramienta Árbol de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="9993a-122">Donation form button in the Accessibility Tree tool</span></span>
:::image-end:::

<span data-ttu-id="9993a-123">Cualquier elemento del árbol que no tenga un nombre o tenga un rol de (como el elemento) es un problema, ya que ese elemento no estará disponible para los usuarios de teclado ni para los usuarios que usan tecnología de `generic` `div` asistencia.</span><span class="sxs-lookup"><span data-stu-id="9993a-123">Any element in the tree that doesn't have a name, or has a role of `generic` (such as the `div` element) is a problem, because that element won't be available to keyboard users, or to users who are using assistive technology.</span></span>


## <a name="see-also"></a><span data-ttu-id="9993a-124">Consulta también</span><span class="sxs-lookup"><span data-stu-id="9993a-124">See also</span></span>

*  [<span data-ttu-id="9993a-125">Ver la posición de un elemento en el árbol de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="9993a-125">View the position of an element in the Accessibility Tree</span></span>][DevtoolsAccessibilityAccessibilityTabViewTree]
*  [<span data-ttu-id="9993a-126">Información general sobre las pruebas de accesibilidad con DevTools</span><span class="sxs-lookup"><span data-stu-id="9993a-126">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9993a-127">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9993a-127">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityAccessibilityTabViewTree]: accessibility-tab.md#view-the-position-of-an-element-in-the-accessibility-tree "Ver la posición de un elemento en el árbol de accesibilidad: probar la accesibilidad mediante la pestaña Accesibilidad | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

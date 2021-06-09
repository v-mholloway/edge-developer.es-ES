---
description: Para comprobar que una página web se puede usar con la visión borrosa, en la herramienta representación, use la lista desplegable Emular deficiencias de visión.
title: Comprobar que la página es utilizable con la visión borrosa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 2fc1a1cf7746591573fce07946c7fb11abf42705
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597693"
---
# <a name="verify-that-the-page-is-usable-with-blurred-vision"></a><span data-ttu-id="93dc3-104">Comprobar que la página es utilizable con la visión borrosa</span><span class="sxs-lookup"><span data-stu-id="93dc3-104">Verify that the page is usable with blurred vision</span></span>

<!-- Rendering tool: Emulate vision deficiencies: Blurred vision -->

<span data-ttu-id="93dc3-105">Para simular una visión borrosa, en la **herramienta Representación,** use el **menú Emular deficiencias de visión.**</span><span class="sxs-lookup"><span data-stu-id="93dc3-105">To simulate blurred vision, in the **Rendering** tool, use the **Emulate vision deficiencies** menu.</span></span>  <span data-ttu-id="93dc3-106">Cuando usas esta característica con la página web de demostración, puedes ver que la sombra paralela en el texto del menú superior dificulta la lectura de los elementos del menú.</span><span class="sxs-lookup"><span data-stu-id="93dc3-106">When you use this feature with the demo webpage, you can see that the drop shadow on the text in the upper menu makes it hard to read the menu items.</span></span>

<span data-ttu-id="93dc3-107">Para comprobar si una página web se puede usar con la visión borrosa:</span><span class="sxs-lookup"><span data-stu-id="93dc3-107">To check whether a webpage is usable with blurred vision:</span></span>

1.  <span data-ttu-id="93dc3-108">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="93dc3-108">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="93dc3-109">Seleccione **Esc** para abrir el cajón en la parte inferior de DevTools.</span><span class="sxs-lookup"><span data-stu-id="93dc3-109">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="93dc3-110">Seleccione el icono en la parte superior del cajón para mostrar la lista de herramientas y, a **+** continuación, seleccione **Representación**.</span><span class="sxs-lookup"><span data-stu-id="93dc3-110">Select the **+** icon at the top of the Drawer to display the list of tools, and then select **Rendering**.</span></span>  

1.  <span data-ttu-id="93dc3-111">En la **lista desplegable Emular deficiencias** de visión, seleccione **Visión borrosa**.</span><span class="sxs-lookup"><span data-stu-id="93dc3-111">In the **Emulate vision deficiencies** dropdown list, select **Blurred vision**.</span></span>

    :::image type="complex" source="../media/a11y-testing-simulating-blur.msft.png" alt-text="Simulación de una página borrosa" lightbox="../media/a11y-testing-simulating-blur.msft.png":::
        <span data-ttu-id="93dc3-113">Simulación de una página borrosa</span><span class="sxs-lookup"><span data-stu-id="93dc3-113">Simulating a blurred page</span></span>
    :::image-end:::

    <span data-ttu-id="93dc3-114">Observe que la propiedad CSS dificulta la lectura del texto de los elementos de `text-shadow` menú en el menú superior.</span><span class="sxs-lookup"><span data-stu-id="93dc3-114">Notice that the `text-shadow` CSS property makes the text of the menu items difficult to read on the upper menu.</span></span> <span data-ttu-id="93dc3-115">Por ejemplo, revisa **Home**, Adopt a **Pet**y otros elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="93dc3-115">For example, review the **Home**, **Adopt a Pet**, and other menu items.</span></span>
    
1.  <span data-ttu-id="93dc3-116">En la **herramienta Representación,** en **Emular**deficiencias de visión, seleccione **Sin emulación** para quitar la simulación de visión borrosa.</span><span class="sxs-lookup"><span data-stu-id="93dc3-116">In the **Rendering** tool, in **Emulate vision deficiencies**, select **No emulation** to remove the blurred vision simulation.</span></span>


## <a name="see-also"></a><span data-ttu-id="93dc3-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="93dc3-117">See also</span></span>

*  [<span data-ttu-id="93dc3-118">Emular deficiencias visuales</span><span class="sxs-lookup"><span data-stu-id="93dc3-118">Emulate vision deficiencies</span></span>](emulate-vision-deficiencies.md)
*  [<span data-ttu-id="93dc3-119">Información general sobre las pruebas de accesibilidad con DevTools</span><span class="sxs-lookup"><span data-stu-id="93dc3-119">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="93dc3-120">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="93dc3-120">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

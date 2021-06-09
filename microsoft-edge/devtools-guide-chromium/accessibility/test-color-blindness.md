---
description: Compruebe que las páginas web son utilizables por personas con ceguera de colores mediante la lista desplegable Emular deficiencias de la visión en la herramienta de representación.
title: Comprobar que la página es utilizable por personas con daltonismo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 54cd7230f0402bfeb4b5ee28d2bcd0947794676f
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597691"
---
# <a name="verify-that-the-page-is-usable-by-people-with-color-blindness"></a><span data-ttu-id="6ab94-104">Comprobar que la página es utilizable por personas con daltonismo</span><span class="sxs-lookup"><span data-stu-id="6ab94-104">Verify that the page is usable by people with color blindness</span></span>

<!-- Rendering tool: Emulate vision deficiencies: Protanopia -->

<span data-ttu-id="6ab94-105">Para comprobar que las personas con ceguera de \*\*\*\* color pueden usar una página web, en la herramienta de representación, use la lista desplegable Emular deficiencias **de visión.**</span><span class="sxs-lookup"><span data-stu-id="6ab94-105">To check that a webpage is usable by people with color blindness, in the **Rendering** tool, use the **Emulate vision deficiencies** dropdown list.</span></span>

<span data-ttu-id="6ab94-106">En la página web de demostración de pruebas de accesibilidad, los distintos estados de donación usan el color como único medio de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="6ab94-106">On the accessibility-testing demo webpage, the different donation states use color as the only means of differentiation.</span></span>
*  <span data-ttu-id="6ab94-107">Verde significa que se ha recibido una gran cantidad de donaciones.</span><span class="sxs-lookup"><span data-stu-id="6ab94-107">Green means a high amount of donations have been received.</span></span>
*  <span data-ttu-id="6ab94-108">Amarillo significa que se ha recibido una cantidad media de donaciones.</span><span class="sxs-lookup"><span data-stu-id="6ab94-108">Yellow means a medium amount of donations have been received.</span></span>
*  <span data-ttu-id="6ab94-109">Rojo significa que se ha recibido una cantidad baja de donaciones.</span><span class="sxs-lookup"><span data-stu-id="6ab94-109">Red means a low amount of donations have been received.</span></span>

<span data-ttu-id="6ab94-110">Pero no puede esperar que todos los usuarios experimente estos colores según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="6ab94-110">But you can't expect all of your users to experience these colors as intended.</span></span>  <span data-ttu-id="6ab94-111">Al usar la característica **Emular** deficiencias de visión de la herramienta de representación, puede averiguar que este diseño no es lo suficientemente bueno, simulando cómo las personas con visión diferente perciben su diseño. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6ab94-111">By using the **Emulate vision deficiencies** feature of the **Rendering** tool, you can find out that this design is not good enough, by simulating how people with different vision would perceive your design.</span></span>


<span data-ttu-id="6ab94-112">Para comprobar si las personas con ceguera de color pueden usar una página web:</span><span class="sxs-lookup"><span data-stu-id="6ab94-112">To check whether a webpage is usable by people with color blindness:</span></span>

1.  <span data-ttu-id="6ab94-113">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="6ab94-113">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="6ab94-114">Seleccione **Esc** para abrir el cajón en la parte inferior de DevTools.</span><span class="sxs-lookup"><span data-stu-id="6ab94-114">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="6ab94-115">Seleccione el icono en la parte superior del cajón para ver la lista de herramientas y, a **+** continuación, seleccione **Representación**.</span><span class="sxs-lookup"><span data-stu-id="6ab94-115">Select the **+** icon at the top of the Drawer to see the list of tools, and then select **Rendering**.</span></span>  

1.  <span data-ttu-id="6ab94-116">En la **lista desplegable Emular deficiencias** de visión, seleccione **Protanopia**.</span><span class="sxs-lookup"><span data-stu-id="6ab94-116">In the **Emulate vision deficiencies** dropdown list, select **Protanopia**.</span></span>  <span data-ttu-id="6ab94-117">_Protanopia_ es una sensibilidad reducida a la luz roja, lo que hace que sea difícil diferenciar verde, rojo y amarillo.</span><span class="sxs-lookup"><span data-stu-id="6ab94-117">_Protanopia_ is reduced sensitivity to red light, making it hard to differentiate green, red, and yellow.</span></span>

    :::image type="complex" source="../media/a11y-testing-simulating-protanopia.msft.png" alt-text="Mostrar el documento como alguien con protanopia lo vería" lightbox="../media/a11y-testing-simulating-protanopia.msft.png":::
        <span data-ttu-id="6ab94-119">Mostrar el documento como alguien con protanopia lo vería</span><span class="sxs-lookup"><span data-stu-id="6ab94-119">Showing the document as someone with protanopia would see it</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="6ab94-120">En la **herramienta Representación,** debajo **de Emular deficiencias de**visión, seleccione Sin **emulación** para quitar la simulación.</span><span class="sxs-lookup"><span data-stu-id="6ab94-120">In the **Rendering** tool, below **Emulate vision deficiencies**, select **No emulation** to remove the simulation.</span></span>


## <a name="see-also"></a><span data-ttu-id="6ab94-121">Consulta también</span><span class="sxs-lookup"><span data-stu-id="6ab94-121">See also</span></span>

*  <span data-ttu-id="6ab94-122">[Emular las deficiencias][DevToolsVisionDeficiencies] de \*\*\*\* la visión: define los elementos de la lista desplegable Emular deficiencias de visión, como Protanopia, Deuteranopia, Tritanopia y Achromatopsia.</span><span class="sxs-lookup"><span data-stu-id="6ab94-122">[Emulate vision deficiencies][DevToolsVisionDeficiencies] - Defines the items in the **Emulate vision deficiencies** dropdown list, including Protanopia, Deuteranopia, Tritanopia, and Achromatopsia.</span></span>
*  [<span data-ttu-id="6ab94-123">Información general sobre las pruebas de accesibilidad con DevTools</span><span class="sxs-lookup"><span data-stu-id="6ab94-123">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6ab94-124">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6ab94-124">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsVisionDeficiencies]: ./emulate-vision-deficiencies.md "Emular las deficiencias de | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

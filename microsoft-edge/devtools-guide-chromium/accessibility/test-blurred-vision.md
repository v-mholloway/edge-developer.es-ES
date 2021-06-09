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
# <a name="verify-that-the-page-is-usable-with-blurred-vision"></a>Comprobar que la página es utilizable con la visión borrosa

<!-- Rendering tool: Emulate vision deficiencies: Blurred vision -->

Para simular una visión borrosa, en la **herramienta Representación,** use el **menú Emular deficiencias de visión.**  Cuando usas esta característica con la página web de demostración, puedes ver que la sombra paralela en el texto del menú superior dificulta la lectura de los elementos del menú.

Para comprobar si una página web se puede usar con la visión borrosa:

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.

1.  Seleccione **Esc** para abrir el cajón en la parte inferior de DevTools.  Seleccione el icono en la parte superior del cajón para mostrar la lista de herramientas y, a **+** continuación, seleccione **Representación**.  

1.  En la **lista desplegable Emular deficiencias** de visión, seleccione **Visión borrosa**.

    :::image type="complex" source="../media/a11y-testing-simulating-blur.msft.png" alt-text="Simulación de una página borrosa" lightbox="../media/a11y-testing-simulating-blur.msft.png":::
        Simulación de una página borrosa
    :::image-end:::

    Observe que la propiedad CSS dificulta la lectura del texto de los elementos de `text-shadow` menú en el menú superior. Por ejemplo, revisa **Home**, Adopt a **Pet**y otros elementos de menú.
    
1.  En la **herramienta Representación,** en **Emular**deficiencias de visión, seleccione **Sin emulación** para quitar la simulación de visión borrosa.


## <a name="see-also"></a>Consulta también

*  [Emular deficiencias visuales](emulate-vision-deficiencies.md)
*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

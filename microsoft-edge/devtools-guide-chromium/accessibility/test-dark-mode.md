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
# <a name="check-for-contrast-issues-with-dark-theme-and-light-theme"></a>Comprobar si hay problemas de contraste con el tema oscuro y el tema claro

<!-- Rendering tool: Emulate CSS media feature prefers-color-scheme -->

Al probar la accesibilidad de color, puede haber diferentes temas de color para mostrar que necesita probar para problemas de contraste.

La mayoría de los sistemas operativos vienen con un modo oscuro y un modo claro.  La página web puede reaccionar a esta configuración del sistema operativo mediante una consulta multimedia CSS.  Puede probar estos temas y probar la consulta multimedia CSS sin tener que cambiar la configuración del sistema operativo mediante las opciones `prefers-color-scheme` CSS de la herramienta **de** representación.

Por ejemplo, la página de demostración de pruebas de accesibilidad incluye un tema claro y un tema oscuro.  La página de demostración hereda la configuración del tema oscuro o claro del sistema operativo.  Si usamos DevTools para simular el sistema operativo que se va **** a establecer en un esquema de luz y, a continuación, actualizar la página web de demostración, la herramienta Problemas muestra seis problemas de contraste de color en lugar de dos.  (Es posible que vea números diferentes).


Para emular la selección de un usuario del tema de color preferido:

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.

1.  Seleccione **Esc** para abrir el cajón en la parte inferior de DevTools.  Seleccione el icono en la parte superior del cajón para ver la lista de herramientas y, a **+** continuación, seleccione **Representación**.  Aparece la herramienta de representación.

1.  En la lista desplegable Emular elementos **multimedia CSS prefers-color-scheme,** seleccione **prefers-color-scheme: light**.      La página web se vuelve a representar mediante `light-theme.css` .


    :::image type="complex" source="../media/a11y-testing-simulating-light-mode.msft.png" alt-text="Uso de la herramienta de representación para simular un modo de luz y desencadenar el otro tema del documento" lightbox="../media/a11y-testing-simulating-light-mode.msft.png":::
        Uso de la herramienta de representación para simular un modo de luz y desencadenar el otro tema del documento
    :::image-end:::


1.  Seleccione la **herramienta Problemas** y, a continuación, expanda la **sección Accesibilidad.**  Dependiendo de varios factores, es posible que reciba `Insufficient color contrast` advertencias. Observe que **en RECURSOS AFECTADOS** hay 6 elementos con contraste de color insuficiente.
    
    :::image type="complex" source="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png" alt-text="Nuevos problemas de contraste detectados debido al cambio al tema claro" lightbox="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png":::
        Nuevos problemas de contraste detectados debido al cambio al tema claro
    :::image-end:::
    
    En nuestra página de demostración, la sección **Estado de** donación de la página es ilegible en modo claro y debe cambiar. 
    
    :::image type="complex" source="../media/a11y-testing-donation-state-light-contrast.msft.png" alt-text="La sección Estado de donación tiene problemas de contraste en modo claro" lightbox="../media/a11y-testing-donation-state-light-contrast.msft.png":::
        La **sección Estado de donación** tiene problemas de contraste en modo claro
    :::image-end:::
    
1.  En DevTools, seleccione la **herramienta Elementos** y, a continuación, **seleccione Ctrl+F** en Windows/Linux o **Command+F** en macOS.  Aparece **el cuadro** de texto Buscar, para buscar en el árbol DOM HTML.
 
1.  Escriba `scheme` .  Se encuentran las siguientes consultas multimedia CSS y ahora se pueden actualizar los archivos CSS correspondientes.

    ```html
    <link rel="stylesheet" href="css/light-theme.css" media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)">
    <link rel="stylesheet" href="css/dark-theme.css" media="(prefers-color-scheme: dark)">
    ```


## <a name="see-also"></a>Consulta también

*  [Simulación de combinación de colores claros o oscuros][DevToolsColorSchemeSimulation]
*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsColorSchemeSimulation]: ./preferred-color-scheme-simulation.md "Simulación de combinación de colores claros o | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

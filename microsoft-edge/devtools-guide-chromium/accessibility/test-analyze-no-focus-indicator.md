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
# <a name="analyze-the-lack-of-indication-of-keyboard-focus-in-a-sidebar-menu"></a>Analizar la falta de indicación del foco del teclado en un menú lateral

<!-- Inspect tool, and CSS rules: pseudo-classes for states -->

En la página de demostración de pruebas de accesibilidad, el menú de navegación de la barra lateral con vínculos azules no indica visualmente qué vínculo tiene el foco al usar un teclado.  Para averiguar por qué el menú de la barra lateral es confuso para los usuarios de teclado, buscaremos reglas de pseudo-clase CSS para los estados y, junto con la propiedad CSS, para los esquemas `hover` `focus` de vínculo.  

Este análisis encuentra que la falta de indicación del foco del teclado en los vínculos del menú de navegación de la barra lateral se debe a:
*  Los `a` vínculos tienen una configuración de propiedad CSS de `outline: none` .
*  Los `a` vínculos carecen de una regla de pseudo-clase CSS para el `:focus` estado.

Para navegar al CSS, usaremos la herramienta **Inspeccionar** para resaltar un vínculo azul en el menú de navegación de la barra lateral y, a continuación, veremos el árbol DOM y CSS para el elemento que define ese `a` vínculo.

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.

1.  Seleccione el **botón Inspeccionar** \( Inspeccionar icono \) en la esquina superior izquierda de DevTools para que el botón esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).

1.  Mantenga el mouse sobre el vínculo **azul Gatos** en el menú de navegación de la barra lateral.  Aparece la superposición Inspeccionar, que muestra que el elemento puede centrarse `a` en el teclado.  Pero la superposición no muestra que no hay ninguna indicación visual cuando el vínculo tiene el foco.

    A continuación, inspeccionaremos el estilo CSS de este vínculo.
 
1.  Selecciona el **vínculo Gatos** en el menú de navegación de la barra lateral.  La **herramienta Inspeccionar** se desactiva y se abre la herramienta **Elementos,** resaltando el `a` nodo en el árbol DOM.

1.  Seleccione la **pestaña Estilos.**  Aparece la regla `#sidebar nav li a` CSS, junto con un vínculo a un número de línea en `styles.css` .

    :::image type="complex" source="../media/a11y-testing-menu-link.msft.png" alt-text="Inspeccionar el código fuente y los estilos aplicados de un vínculo en el menú" lightbox="../media/a11y-testing-menu-link.msft.png":::
        Inspeccionar el código fuente y los estilos aplicados de un vínculo en el menú
    :::image-end:::
    
1.  Seleccione el vínculo al archivo CSS.  El archivo CSS se abre dentro de la **herramienta Orígenes.**

    :::image type="complex" source="../media/a11y-testing-menu-link-styles.msft.png" alt-text="Los estilos aplicados al vínculo en la herramienta Orígenes" lightbox="../media/a11y-testing-menu-link-styles.msft.png":::
        Los estilos aplicados al vínculo en la herramienta Orígenes
    :::image-end:::
    
Los estilos de la página tienen una regla de pseudo-clase CSS para el estado que indica el elemento de menú en el que se encuentra al `hover` usar un mouse: `#sidebar nav li a:hover` .  Sin embargo, no hay ninguna regla de pseudo class CSS para que el estado indique visualmente en qué elemento de menú está al usar `focus` un teclado, como `#sidebar nav li a:focus` .

Además, tenga en cuenta que los vínculos tienen una configuración de propiedad CSS de `outline: none` .  Este es un procedimiento común, para quitar el esquema que los exploradores agregan automáticamente a los elementos cuando se centran en ellos mediante un teclado.  No usar `focus` el estilo causa confusión para los usuarios.


## <a name="see-also"></a>Consulta también 

*  [Rastrear qué elemento tiene el foco](focus.md)
*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

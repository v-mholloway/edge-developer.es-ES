---
description: Use la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar el mouse sobre la página web.
title: Usar la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar sobre la página web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 6e363e07c252dd0305216cdbeda1241d5aa2bc193e1111e6b69eeeae9f8deadd
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11802388"
---
# <a name="use-the-inspect-tool-to-detect-accessibility-issues-by-hovering-over-the-webpage"></a>Usar la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar sobre la página web

La **herramienta Inspeccionar** muestra información sobre los elementos individuales al pasar el puntero sobre la página web que se representa, incluida la información de accesibilidad.
En cambio, la **herramienta Problemas** notifica automáticamente los problemas de toda la página web.

El **botón de** la herramienta Inspeccionar \( Inspect \) se encuentra en la esquina superior izquierda de ![ ](../media/inspect-icon.msft.png) DevTools.  Al seleccionar el botón **Inspeccionar** herramienta, el botón se vuelve azul, lo que indica que **la herramienta Inspeccionar** está activa.

Cuando la **herramienta Inspeccionar** está activa, al mantener el mouse sobre cualquier elemento de la página web representada, se muestra **la superposición Inspeccionar.** Esta superposición muestra información general e información de accesibilidad sobre ese elemento.  La **sección Accesibilidad** de la superposición **Inspeccionar** muestra información sobre el contraste de color de texto, el texto del lector de pantalla y la compatibilidad con el teclado.

:::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="La herramienta Inspeccionar, que muestra el área del elemento como una superposición multicolor y muestra los detalles del elemento como una superposición de información grande" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
    La **herramienta Inspeccionar,** que muestra el área del elemento como una superposición multicolor y muestra los detalles del elemento como una superposición de información grande
:::image-end:::


## <a name="check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support"></a>Comprobar los elementos individuales para el contraste de texto, el texto del lector de pantalla y la compatibilidad con el teclado

<!-- Inspect tool: Accessibility section of overlay -->

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.

1.  Seleccione el **botón Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda de DevTools para que el icono esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).

    :::image type="complex" source="../media/a11y-testing-basics-inspector.msft.png" alt-text="Para activar la herramienta Inspeccionar, seleccione el botón Inspeccionar" lightbox="../media/a11y-testing-basics-inspector.msft.png":::
        Para activar la herramienta **Inspeccionar,** seleccione el **botón Inspeccionar**
    :::image-end:::

1.  Mantenga el mouse sobre cualquier elemento de la página web de demostración que se represente.  La **herramienta Inspeccionar** muestra una superposición de información debajo del elemento dentro de la página web representada.

    :::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="La herramienta Inspeccionar, que muestra el diseño del elemento como una superposición multicolor y muestra los detalles del elemento como una superposición de información grande" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
        La **herramienta Inspeccionar,** que muestra el diseño del elemento como una superposición multicolor y muestra los detalles del elemento como una superposición de información grande
    :::image-end:::

La parte inferior de la **superposición Inspeccionar** tiene **una sección Accesibilidad** que contiene la siguiente información:

*   **El** contraste define si un elemento puede ser comprendido por personas con visión baja.  La [relación de contraste][W3CContrastRatio] definida por las Directrices de [WCAG][WCAG] indica si hay suficiente contraste (un icono de marca de verificación verde) o no suficiente (icono de signo de exclamación naranja).

*   **Name** y **Role** son los elementos que la tecnología de asistencia, como los lectores de pantalla, informarán sobre el elemento.
    *   Name **es** el contenido de texto de un `a` elemento.  Para el elemento `<a href="/">About Us</a>` , el nombre **que** se muestra en la herramienta Inspeccionar es "Acerca de nosotros".
    *   Role **** del elemento.  Este suele ser el nombre del elemento, como `article` , `img` , o `link` `heading` .  Los `div` elementos y se `span` `generic` denominan .

*   **El enfoque de teclado** indica si los usuarios pueden llegar al elemento independientemente del dispositivo de entrada.
    *   Un icono de marca de verificación verde indica que el elemento se puede centrar en el teclado.
    *   Un círculo gris con línea diagonal indica que el elemento no se puede centrar en el teclado.


## <a name="additional-information-in-the-inspect-overlay"></a>Información adicional en la superposición Inspeccionar

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

La parte superior de la **superposición Inspeccionar,** que está encima de la sección **Accesibilidad,** enumera los siguientes detalles del elemento.

*   Tipo de diseño. Si el elemento se coloca mediante un flexbox o una cuadrícula, un icono \(![Icono de diseño de cuadrícula](../media/grid-icon.msft.png)\) se muestra.
*   Nombre del elemento, como `h1` , `h2` o `div` .
*   Dimensiones del elemento en píxeles.
*   El color como una muestra de color (o un cuadrado pequeño y coloreado) y como una cadena (como `#336699` ).
*   Información de fuentes, como el tamaño y las familias de fuentes.
*   Margen y relleno en píxeles.


## <a name="identify-nested-regions-using-color-highlighting"></a>Identificar regiones anidadas mediante resaltado de color 

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

Además de la superposición de información, la herramienta **Inspeccionar** también proporciona un color de región similar al mantener el mouse en el árbol DOM de la **herramienta** Elementos.

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.

1.  Seleccione el **botón Inspeccionar** \( Icono de la herramienta Inspeccionar \) en la esquina superior izquierda ![ de DevTools, de modo que el botón esté resaltado ](../media/inspect-icon.msft.png) (azul).

1.  Mantenga el mouse sobre diferentes partes de la página web de demostración representado.  Cada elemento de la página web ahora se muestra con una superposición multicolor. Esta superposición multicolor puede mostrar regiones anidadas dentro de un elemento. Por ejemplo, mantenga el mouse sobre el margen izquierdo de **Gatos**.  La **herramienta Inspeccionar** resalta varias partes **** rectangulares de la sección Gatos con diferentes colores, que muestran el diseño que resulta de las definiciones de flexbox CSS en la página web.

:::image type="complex" source="../media/inspect-tool-flexbox-overlay.msft.png" alt-text="Superposición de flexbox multicolor y superposición de información al usar la herramienta Inspeccionar" lightbox="../media/inspect-tool-flexbox-overlay.msft.png":::
    Superposición de flexbox multicolor y superposición de información al usar **la herramienta Inspeccionar**
:::image-end:::

Para configurar la superposición de cuadrícula o la superposición de flexbox, en la **herramienta Elementos,** seleccione la **pestaña** Diseño.  Para obtener más información, vaya a [Inspeccionar cuadrícula CSS](..\css\grid.md).


## <a name="use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css"></a>Usar la herramienta Inspeccionar para pasar el puntero sobre la página web para resaltar el DOM y CSS

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.

1.  Seleccione el **botón Inspeccionar** \( la herramienta Inspeccionar \) en la esquina superior izquierda ![ de DevTools, de modo que el botón esté ](../media/inspect-icon.msft.png) resaltado (azul).

1.  Seleccione la **herramienta** Elementos.

1.  Con la **herramienta Inspeccionar** activa, mantenga el puntero sobre distintas partes de la página web que se representa.  En la **herramienta Elementos,** el árbol DOM HTML se expande automáticamente para mostrar información sobre el elemento sobre el que se mueve el mouse.  Si se mantiene el mouse, el panel **Estilos no** se actualiza.

1.  Ahora seleccione cualquier elemento dentro de la página web que se represente.  La **herramienta Elementos** se abre automáticamente y muestra el CÓDIGO HTML del elemento en el árbol DOM. La herramienta también muestra el CSS aplicado en el elemento del **panel Estilos.**  Al seleccionar un elemento en la página web que se representa, se desactiva la **herramienta Inspeccionar.**

:::image type="complex" source="../media/a11y-testing-basics-inspector-selected-element.msft.png" alt-text="Los detalles sobre el elemento seleccionado se muestran en la herramienta Elementos" lightbox="../media/a11y-testing-basics-inspector-selected-element.msft.png":::
    Los detalles sobre el elemento seleccionado se muestran en la **herramienta** Elementos
:::image-end:::

Después de seleccionar un elemento en la página representada, puede **** usar la pestaña **** Accesibilidad (cerca de la pestaña Estilos) para ver el árbol de accesibilidad y usar el Visor de pedidos **de origen**. ****


## <a name="see-also"></a>Consulte también

*  [Inspeccionar un nodo](../dom/index.md#inspect-a-node)
*  [Comprobar el contraste de color de texto en el estado predeterminado con la herramienta Inspeccionar](test-inspect-text-contrast.md)
*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"
[W3CContrastRatio]: https://www.w3.org/TR/WCAG21/#dfn-contrast-ratio "relación de contraste | W3C"
[WCAG]: https://www.w3.org/TR/WCAG21/ "Directrices de accesibilidad de contenido web | W3C"

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
# <a name="check-text-color-contrast-in-the-default-state-using-the-inspect-tool"></a>Comprobar el contraste de color de texto en el estado predeterminado con la herramienta Inspeccionar

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

Compruebe el contraste de color del texto en el estado predeterminado mediante la **herramienta Inspeccionar.**  La **superposición** de información de la herramienta Inspeccionar en la página web tiene una sección **Accesibilidad** que incluye información **de** contraste.

Para comprobar el contraste de color de texto en el estado predeterminado mediante la superposición de información de la herramienta Inspeccionar, siga estos pasos.

<!-- Inspect tool -->
Para los elementos que tienen texto, **la superposición de** información de la herramienta Inspeccionar muestra lo siguiente:
*  Relación de contraste de texto frente a colores de fondo.
*  Icono de marca de verificación verde para elementos con contraste suficiente.
*  Icono de alerta amarilla para elementos que no tienen suficiente contraste.

En algunos casos, el contraste se ve afectado al establecer el explorador en tema claro u tema oscuro.

Por ejemplo, en la página de demostración, los vínculos azules **** del menú **** de navegación de la barra lateral tienen suficiente contraste, pero el vínculo verde Perros de la sección Estado de la donación no tiene suficiente contraste.  Revise esos elementos con **la herramienta Inspeccionar,** como se muestra a continuación:

1.  Abra la [página web de demostración de pruebas de][DevToolsA11yErrorsDemopage] accesibilidad en una pestaña nueva.  A **continuación, seleccione F12** para abrir DevTools.

1.  Seleccione el **botón Inspeccionar** \( Botón Inspeccionar \) en la esquina superior izquierda de DevTools para que el icono esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).

1.  En la página web que se representa, mantenga el mouse sobre el vínculo **azul Gatos** del menú de navegación de la barra lateral.  Aparece **la superposición** de información de la herramienta Inspeccionar.  En la **sección Accesibilidad** de la superposición de **** información, aparece una marca de verificación verde en la fila Contraste, que indica que este elemento tiene suficiente contraste de color de texto frente al color de fondo.

    :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Los elementos de menú tienen suficiente contraste, como se muestra en la herramienta Inspeccionar" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
        Los elementos de menú tienen suficiente contraste, como se muestra en la herramienta Inspeccionar
    :::image-end:::

1.  En la página web que se representa, en la sección **Estado de** la donación, mantenga el mouse sobre el **vínculo** Perros.  La **superposición** de información de la herramienta Inspeccionar muestra un signo de exclamación naranja en la fila **Contraste,** lo que indica que este elemento no tiene suficiente contraste de texto frente a los colores de fondo.

    :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Un elemento que no tiene suficiente contraste, como se muestra en la advertencia de la herramienta Inspeccionar" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
        Un elemento que no tiene suficiente contraste, como se muestra en la advertencia de la herramienta Inspeccionar
    :::image-end:::


## <a name="different-options-to-inspect-text-color-contrast-in-devtools"></a>Diferentes opciones para inspeccionar el contraste de color de texto en DevTools

Use las siguientes características de DevTools para inspeccionar el contraste de color de texto.

*  Use la **herramienta Inspeccionar** (como superposición de información en la página web) para comprobar si un elemento de página individual tiene suficiente contraste de color de texto.  La **superposición** de información de la herramienta Inspeccionar incluye una sección **Accesibilidad** que tiene una fila **información** de contraste.  La **herramienta Inspeccionar** solo muestra información de contraste de texto para el estado actual.  Este enfoque se describe en el artículo actual.

*  La **herramienta Problemas** notifica automáticamente cualquier problema de contraste de color para toda la página web, cuando el texto y el color de fondo no contrastan lo suficiente.  Este enfoque se describe en [Verify that text colors have enough contrast](test-issues-tool.md#verify-that-text-colors-have-enough-contrast).

*  Emular un estado no predeterminado, como el estado, mediante el uso del estado de elemento Toggle en el panel Estilos, descrito en `hover` [Verify accessibility of all states of elements](test-inspect-states.md). **** ****


## <a name="see-also"></a>Consulta también

*  [Comprobar la accesibilidad de todos los estados de elementos][DevtoolsAccessibilityTestInspectStates]
*  [Usar la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar el puntero sobre la página web](test-inspect-tool.md)
*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityTestInspectStates]: test-inspect-states.md "Comprobar la accesibilidad de todos los estados de elementos | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

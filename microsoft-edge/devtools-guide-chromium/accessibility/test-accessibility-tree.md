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
# <a name="check-the-accessibility-tree-for-keyboard-and-screen-reader-support"></a>Comprobar la compatibilidad con el teclado y el lector de pantalla en el Árbol de accesibilidad

<!-- Accessibility tab: Accessibility Tree -->

Varias características de DevTools comprueban la compatibilidad con el teclado y el lector de pantalla.  El uso **de la herramienta Inspeccionar** para comprobar la accesibilidad de cada elemento de página individualmente puede llevar bastante tiempo.  Una forma alternativa de comprobar una página web es usar el árbol **de accesibilidad**.  El **Árbol de accesibilidad** indica qué información proporciona la página a la tecnología de asistencia, como los lectores de pantalla.

El **árbol de accesibilidad** es un subconjunto del árbol DOM, que contiene elementos del árbol DOM que son relevantes y útiles para mostrar el contenido de una página en un lector de pantalla.  El **árbol de accesibilidad** está en la pestaña **Accesibilidad** de la **herramienta Elementos** (cerca de la **pestaña** Estilos).


Para explorar el uso del árbol de accesibilidad con la página de demostración:

1.  Abra la [página web de demostración de pruebas de][DevToolsA11yErrorsDemopage] accesibilidad en una pestaña nueva.  A **continuación, seleccione F12** para abrir DevTools.

1.  Seleccione el **botón Inspeccionar** \( el icono Inspeccionar \) de la esquina superior izquierda de DevTools para que el botón esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).

1.  En la página web que se representa, en la **sección Donación,** mantenga el mouse sobre el **botón 100.**  Aparece **la superposición** de la herramienta Inspeccionar.

1.  En la página web representada, seleccione el **botón 100.**  En DevTools, se muestra **la** herramienta Elementos.  El árbol DOM muestra el `div` elemento del **botón 100.**  El **panel Estilos** muestra la configuración CSS del elemento.

1.  A la derecha de la **pestaña Estilos,** seleccione la **pestaña Accesibilidad.**  Se **muestra el árbol de** accesibilidad del elemento y se expande.

:::image type="complex" source="../media/a11y-testing-accessibility-tree.msft.png" alt-text="Botón formulario de donación en la herramienta Árbol de accesibilidad" lightbox="../media/a11y-testing-accessibility-tree.msft.png":::
    Botón formulario de donación en la herramienta Árbol de accesibilidad
:::image-end:::

Cualquier elemento del árbol que no tenga un nombre o tenga un rol de (como el elemento) es un problema, ya que ese elemento no estará disponible para los usuarios de teclado ni para los usuarios que usan tecnología de `generic` `div` asistencia.


## <a name="see-also"></a>Consulta también

*  [Ver la posición de un elemento en el árbol de accesibilidad][DevtoolsAccessibilityAccessibilityTabViewTree]
*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityAccessibilityTabViewTree]: accessibility-tab.md#view-the-position-of-an-element-in-the-accessibility-tree "Ver la posición de un elemento en el árbol de accesibilidad: probar la accesibilidad mediante la pestaña Accesibilidad | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

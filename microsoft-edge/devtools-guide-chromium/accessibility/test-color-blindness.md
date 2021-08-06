---
description: Compruebe que las páginas web son utilizables por personas con ceguera de colores mediante la lista desplegable Emular deficiencias de la visión en la herramienta de representación.
title: Verificar si las personas con daltonismo pueden utilizar la página
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: cde0def6e15f8dd9e430ce56754df29f380db561b540849c65f85d449c9d028d
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11802231"
---
# <a name="verify-that-the-page-is-usable-by-people-with-color-blindness"></a>Verificar si las personas con daltonismo pueden utilizar la página

<!-- Rendering tool: Emulate vision deficiencies: Protanopia -->

Para comprobar que las personas con ceguera de **** color pueden usar una página web, en la herramienta de representación, use la lista desplegable Emular deficiencias **de visión.**

En la página web de demostración de pruebas de accesibilidad, los distintos estados de donación usan el color como único medio de diferenciación.
*  Verde significa que se ha recibido una gran cantidad de donaciones.
*  Amarillo significa que se ha recibido una cantidad media de donaciones.
*  Rojo significa que se ha recibido una cantidad baja de donaciones.

Pero no puede esperar que todos los usuarios experimente estos colores según lo previsto.  Al usar la característica **Emular** deficiencias de visión de la herramienta de representación, puede averiguar que este diseño no es lo suficientemente bueno, simulando cómo las personas con visión diferente perciben su diseño. ****


Para comprobar si las personas con ceguera de color pueden usar una página web:

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.

1.  Seleccione **Esc** para abrir el cajón en la parte inferior de DevTools.  Seleccione el icono en la parte superior del cajón para ver la lista de herramientas y, a **+** continuación, seleccione **Representación**.  

1.  En la **lista desplegable Emular deficiencias** de visión, seleccione **Protanopia**.  _Protanopia_ es una sensibilidad reducida a la luz roja, lo que hace que sea difícil diferenciar verde, rojo y amarillo.

    :::image type="complex" source="../media/a11y-testing-simulating-protanopia.msft.png" alt-text="Mostrar el documento como alguien con protanopia lo vería" lightbox="../media/a11y-testing-simulating-protanopia.msft.png":::
        Mostrar el documento como alguien con protanopia lo vería
    :::image-end:::
    
1.  En la **herramienta Representación,** debajo **de Emular deficiencias de**visión, seleccione Sin **emulación** para quitar la simulación.


## <a name="see-also"></a>Consulte también

*  [Emular las deficiencias][DevToolsVisionDeficiencies] de **** la visión: define los elementos de la lista desplegable Emular deficiencias de visión, como Protanopia, Deuteranopia, Tritanopia y Achromatopsia.
*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsVisionDeficiencies]: ./emulate-vision-deficiencies.md "Emular las deficiencias de | Microsoft Docs"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"

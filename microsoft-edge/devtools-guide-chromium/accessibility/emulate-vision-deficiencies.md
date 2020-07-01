---
title: Emular deficiencias de la visión en Microsoft Edge DevTools (daltonismo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: b70499fa189d162fa7589966bab183f4c12f68f7
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843924"
---
# Emular deficiencias de la visión

Para satisfacer mejor las necesidades de los usuarios con [deficiencia][ColorblindawarenessMain] de la visión del color \ (daltonismo \), [Microsoft Edge DevTools][MicrosoftEdgeDevTools] le permite simular determinadas deficiencias de la visión del color.  La herramienta **emular deficiencias** de la visión simula las siguientes categorías.  

| Deficiencia de la visión del color | Detalles |  
|:--- |:--- |  
| Visión borrosa | El usuario tiene dificultades para centrarse en detalles. |   
| Protanopia | El usuario no puede percibir ninguna luz roja. |  
| Deuteranopia | El usuario no puede percibir ninguna luz verde. |  
| Tritanopia | El usuario no puede percibir ninguna luz azul. |  
| Achromatopsia | El usuario no puede percibir ningún color, lo que reduce todo el color a un tono de gris. |  

## Ir a las herramientas de representación  

Para simular una deficiencia de la visión que se aplica a su producto Web, abra las [herramientas de representación][RenderingTools].  

1.  Abrir las herramientas de representación seleccionando el `...` elemento de menú de la barra de herramientas  
1.  Seleccionar `More tools`  
1.  Seleccionar `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrir las herramientas de representación" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Abrir las **herramientas de representación**  
    :::image-end:::  

El menú de **fotorrealismo** aparece en el cajón.  

1.  Desplácese hacia abajo hasta el `Emulate vision deficiencies` elemento de menú y seleccione el menú desplegable para mostrar las opciones.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="El menú emular deficiencias de la visión en el alimentador de representación" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       El menú **emular deficiencias** de la visión en el alimentador de **representación**  
    :::image-end:::  
    
1.  Elija una opción.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Las opciones del menú emular deficiencias de visión" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Las opciones del menú **emular deficiencias de visión**  
    :::image-end:::  
    
1.  En la ventana principal se muestra la simulación de la opción seleccionada que se ha aplicado a la página actual.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Mostrar con * * simulación de enfoque * * borroso" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Mostrar con simulación de **visión borrosa**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Pantalla con * * achromatopsia * * simulación" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Mostrar con simulación de **achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## Usar el menú de comandos  

También puede usar el **menú de comandos** para acceder a las distintas simulaciones.  

1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       El **menú de comandos**  
    :::image-end:::  
    
1.  Escriba `emulate` , elija lo que desea simular y presione `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Las diferentes opciones de simulación disponibles en el menú de comandos" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Las diferentes opciones de simulación disponibles en el **menú de comandos**  
    :::image-end:::  
    
> [!IMPORTANT]
> Las herramientas **emular deficiencias** de la visión simulan aproximaciones sobre cómo una persona con deficiencias puede ver su producto.  Cada persona es diferente; por lo tanto, las deficiencias de la visión varían en gravedad de persona a persona.  Para satisfacer mejor las necesidades de los usuarios, evite cualquier combinación de colores que pueda ser un problema.  Las herramientas **emular deficiencias de Vision** no son una evaluación completa de la accesibilidad del producto.  En su lugar, las herramientas **emular deficiencias** de la visión deberían darle un buen primer paso para evitar problemas.  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "La organización de conocimiento de colores ciegos"  
[AmfcbMain]: https://www.amfcb.org "American Foundation para el color Blind (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Herramientas de representación de Microsoft Edge (cromo)"  

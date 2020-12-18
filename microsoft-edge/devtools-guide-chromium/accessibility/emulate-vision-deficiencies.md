---
description: Emular las deficiencias de la visión en Microsoft Edge DevTools.
title: Emular deficiencias de la visión en Microsoft Edge DevTools (daltonismo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 5343d32992880f8c60501a86db6cb3a92f417331
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230827"
---
# Emular deficiencias visuales

Para satisfacer mejor las necesidades de los usuarios con [deficiencia][ColorblindawarenessMain] de la visión del color \ (daltonismo \), [Microsoft Edge DevTools][DevtoolsIndex] le permite simular determinadas deficiencias de la visión del color.  La herramienta **emular deficiencias** de la visión simula las siguientes categorías.  

| Deficiencia de la visión del color | Detalles |  
|:--- |:--- |  
| Visión borrosa | El usuario tiene dificultades para centrarse en detalles. |   
| Protanopia | El usuario no puede percibir ninguna luz roja. |  
| Deuteranopia | El usuario no puede percibir ninguna luz verde. |  
| Tritanopia | El usuario no puede percibir ninguna luz azul. |  
| Achromatopsia | El usuario no puede percibir ningún color, lo que reduce todo el color a un tono de gris. |  

## Ir a las herramientas de representación  

Para simular una deficiencia de la visión que se aplica a su producto Web, abra las [herramientas de representación][DevtoolsRenderingToolsIndex].  

1.  Para abrir las herramientas de representación, elija el `...` elemento de menú de la barra de herramientas  
1.  Elegir `More tools`  
1.  Elegir `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrir las herramientas de representación" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Abrir las **herramientas de representación**  
    :::image-end:::  

El menú de **fotorrealismo** aparece en el cajón.  

1.  Desplácese hacia abajo hasta el `Emulate vision deficiencies` elemento de menú y elija el menú desplegable para mostrar las opciones.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="El menú emular deficiencias de la visión en el alimentador de representación" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       El menú **emular deficiencias** de la visión en el alimentador de **representación**  
    :::image-end:::  
    
1.  Elija una opción.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Las opciones del menú emular deficiencias de visión" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Las opciones del menú **emular deficiencias de visión**  
    :::image-end:::  
    
1.  En la ventana principal, se muestra la simulación de la opción que ha elegido aplicada a la página actual.  
    
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

1.  Seleccione `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       El **menú de comandos**  
    :::image-end:::  
    
1.  Escriba `emulate` , elija lo que desea simular y seleccione `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Las diferentes opciones de simulación disponibles en el menú de comandos" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Las diferentes opciones de simulación disponibles en el **menú de comandos**  
    :::image-end:::  
    
> [!IMPORTANT]
> Las herramientas **emular deficiencias** de la visión simulan aproximaciones sobre cómo una persona con deficiencias puede ver su producto.  Cada persona es diferente; por lo tanto, las deficiencias de la visión varían en gravedad de persona a persona.  Para satisfacer mejor las necesidades de los usuarios, evite cualquier combinación de colores que pueda ser un problema.  Las herramientas **emular deficiencias de Vision** no son una evaluación completa de la accesibilidad del producto.  En su lugar, las herramientas **emular deficiencias** de la visión deberían darle un buen primer paso para evitar problemas.  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analizar rendimiento en tiempo de ejecución | Microsoft docs"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "La organización de conocimiento de colores ciegos"  

[AmfcbMain]: https://www.amfcb.org "American Foundation para el color Blind (AFCB)"  


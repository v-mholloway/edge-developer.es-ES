---
title: Emular deficiencias de la visión en Microsoft Edge DevTools (daltonismo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0b608f5fe67724eee81aeb993577ee9b45cbca09
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758120"
---
# Emular deficiencias de la visión

En todo el mundo, aproximadamente el 8% de hombres y 0,5% de mujeres tienen una deficiencia de la [visión de color][ColorblindawarenessMain] que comúnmente se denomina "daltonismo".  [Microsoft Edge DevTools][MicrosoftEdgeDevTools] le permite emular diversas deficiencias conocidas y ofrecer una vista previa del producto para que lo revise.  

| Deficiencia de color | Detalles |  
|:--- |:--- |  
| Visión borrosa |  |   
| Protanopia | La incapacidad de percibir cualquier luz roja. |  
| Deuteranopia | La incapacidad de percibir cualquier luz verde. |  
| Tritanopia | La incapacidad de percibir cualquier luz azul. |  
| Achromatopsia | La incapacidad de percibir cualquier color, excepto tonos de gris. |  

## Ir a las herramientas de representación  

Para probar el producto Web actual por deficiencias de color, abra las [herramientas de representación][RenderingTools].  

1.  Abrir las herramientas de representación seleccionando el `...` elemento de menú de la barra de herramientas  
1.  Seleccionar `More tools`  
1.  Seleccionar `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrir las herramientas de representación" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Abrir las **herramientas de representación**  
    :::image-end:::  

El menú de **fotorrealismo** aparece en la mitad inferior de la DevTools.  

1.  Desplácese hacia abajo hasta el `Emulate Vision deficiencies` elemento de menú y seleccione una de las opciones.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="El menú emular deficiencias de la visión de las herramientas de representación" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       El menú **emular deficiencias** de la visión de las herramientas de **representación**  
    :::image-end:::  
    
1.  Elija cualquiera de las opciones  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Las opciones del menú emular deficiencias de visión" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Las opciones del menú **emular deficiencias de visión**  
    :::image-end:::  
    
1.  La página actual se muestra en una simulación de cómo puede mostrarse a un usuario con la deficiencia elegida.  

    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Documentación de las herramientas de desarrollo de Microsoft Edge en emulación de visión borrosa" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Se muestra con la emulación de la **visión borrosa**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Documentación de las herramientas de desarrollo de Microsoft Edge en achromatopsia Vision Emulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Mostrar con la emulación de la **visión de achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## Usar el menú de comandos  

También puede alcanzar las distintas emulaciones sin pasar por los distintos menús mediante el **menú de comandos**.  

1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       El **menú de comandos**  
    :::image-end:::  
    
1.  Escriba `emulate` , elija lo que desea simular y presione `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Las diferentes opciones de emulación disponibles en el menú de comandos" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Las diferentes opciones de emulación disponibles en el **menú de comandos**  
    :::image-end:::  
    
> [!IMPORTANT]
> Las herramientas de emulación son aproximaciones de la manera en que una persona con deficiencias puede ver su producto.  Cada persona es diferente; por lo tanto, las deficiencias de la visión varían en gravedad de persona a persona.  Para satisfacer mejor las necesidades de los usuarios, evite cualquier combinación de colores que pueda ser un problema.  Las herramientas de emulación no son una evaluación completa de la accesibilidad de su producto, pero usted debe tener un buen primer paso para evitar las mayores deficiencias.  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "La organización de conocimiento de colores ciegos"  
[AmfcbMain]: https://www.amfcb.org "American Foundation para el color Blind (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Herramientas de representación de Microsoft Edge (cromo)"  

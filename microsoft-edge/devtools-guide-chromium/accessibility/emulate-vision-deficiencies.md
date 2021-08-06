---
description: Emular las deficiencias de visión en Microsoft Edge DevTools.
title: Emular las deficiencias de la visión Microsoft Edge DevTools (daltonismo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 8af8e621fe67fbb17d6319f9b8e6ff28595312543b73eba33277ab0c291fc450
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11803115"
---
# <a name="emulate-vision-deficiencies"></a>Emular deficiencias visuales  

Para satisfacer mejor las necesidades de los usuarios con deficiencia de visión de [color][ColorblindawarenessMain] \(daltonismo\) o visión borrosa, [Microsoft Edge DevTools][DevtoolsIndex] le permite simular las deficiencias de visión borrosa y las deficiencias específicas de la visión de color.  La **herramienta Emular deficiencias de visión** simula las siguientes categorías.  

| Deficiencia de la visión del color | Detalles |  
|:--- |:--- |  
| Visión borrosa | El usuario tiene dificultades para centrarse en detalles finos. |  
| Protanopia | El usuario no puede percibir ninguna luz roja. |  
| Deuteranopia | El usuario no puede percibir ninguna luz verde. |  
| Tritanopia | El usuario no puede percibir ninguna luz azul. |  
| Achromatopsia | El usuario no puede percibir ningún color, lo que reduce todo el color a una sombra de gris. |  


## <a name="navigate-to-the-rendering-tool"></a>Vaya a la herramienta de representación

Para simular una deficiencia de visión que se está aplicando para el producto web, abra las herramientas [de representación][DevtoolsRenderingToolsIndex].  

1.  Para abrir la herramienta Representación, elija el elemento `...` de menú de la barra de herramientas  
1.  Elegir **más herramientas**  
1.  Elegir **representación**  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrir la herramienta de representación" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Abrir la herramienta **de** representación
    :::image-end:::  
    
El **menú** Representación aparece en el cajón.  

1.  Desplácese hacia abajo hasta el `Emulate vision deficiencies` elemento de menú y elija el menú desplegable para mostrar las opciones.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Menú Emular deficiencias de visión en la herramienta de representación" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       Menú **Emular deficiencias de visión** en la herramienta **de** representación
    :::image-end:::  
    
1.  Elija una opción.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Opciones del menú Emular deficiencias de la visión" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Opciones **del menú Emular deficiencias** de visión  
    :::image-end:::  
    
1.  Las ventanas principales muestran la simulación de la opción elegida aplicada a la página actual.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Visualización con simulación de visión borrosa" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Visualización con **simulación de visión borrosa**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Mostrar con la simulación de Achromatopsia" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Mostrar con **la simulación de Achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    

## <a name="use-the-command-menu"></a>Usar el menú de comandos  

También puede usar el **menú comando para** tener acceso a las diferentes simulaciones.  

1.  Seleccione `Ctrl` + `Shift` + `P` \(Windows/Linux\) o `Command` + `Shift` + `P` \(macOS\) para **** abrir el menú de comandos .  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menú comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Menú **comando**  
    :::image-end:::  
    
1.  Escriba `emulate` , elija lo que desea simular y elija `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Las distintas opciones de simulación disponibles en el menú comando" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Las distintas opciones de simulación disponibles en el **menú comando**  
    :::image-end:::  
    
> [!IMPORTANT]
> Las **herramientas Emular deficiencias de** visión simulan aproximaciones de cómo una persona con cada deficiencia puede ver el producto.  Cada persona es diferente, por lo tanto, las deficiencias de la vista varían en la gravedad de una persona a otra.  Para satisfacer mejor las necesidades de los usuarios, evite cualquier combinación de colores que pueda ser un problema.  Las **herramientas Emular deficiencias** de visión no son una evaluación de accesibilidad completa del producto.  En su lugar, **las herramientas Emular** deficiencias de visión deben darle un buen primer paso para evitar problemas.  


## <a name="see-also"></a>Consulte también

* [Verificar si la página se puede utilizar con la visión borrosa](test-blurred-vision.md)


<!-- links -->  
[DevToolsIndex]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analizar el rendimiento en tiempo de ejecución | Microsoft Docs"  

[ColorblindawarenessMain]: https://www.colourblindawareness.org "La organización de concienciación de ciegos de color"  

[AmfcbMain]: https://www.amfcb.org "The American Foundation for the Color Blind (AFCB)"  

---
Description: Forzar que Microsoft Edge DevTools en el modo de vista previa de combinación de colores.
title: Forzar el modo de vista previa de la combinación de colores de Microsoft Edge DevTools (CSS prefiere la combinación de colores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 29b0121a616a037fa11b61799efeffd201eb1821
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230799"
---
# Simulación de combinación de colores oscuro o claro  

Los sistemas operativos tienen una manera de mostrar cualquier aplicación en colores más oscuros o claros.  Tener un producto Web con un tema claro en un sistema operativo de modo oscuro es Grating y puede ser un problema de accesibilidad para algunos usuarios.  En la web, puede usar la consulta de medios [preferidas-combinación de colores][MDNPrefersColorScheme] de CSS para detectar si los usuarios prefieren ver su producto en una combinación más oscura o más clara.  Use [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] para simular un cambio de modo oscuro a claro sin tener que cambiar todo el sistema operativo.  

1.  Abrir el **menú de comandos**.  
    1.  Seleccione `Control` + `Shift` + `P` en Windows/Linux o `Command` + `Shift` + `P` en MacOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           El **menú de comandos**  
        :::image-end:::  
        
1.  `emulate color`En tipo, elija **EMULAr CSS preferentemente-esquema de color: oscuro** o **emular CSS preferentes-esquema de color: Light** y, a continuación, seleccione `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Opción de combinación de colores del menú comando" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       Opción de combinación de colores del menú **comando**  
    :::image-end:::  
    
    > [!IMPORTANT]
    > Simplemente escribe `dark` o `light` no revela la herramienta adecuada, ya que también hay una forma de [elegir un tema para DevTools][DevtoolsGuideChromiumCustomizeDarkTheme].  Si se pregunta qué elegir, asegúrese de que está seleccionando un elemento de menú de **representación** , no un elemento de menú de **apariencia** .  

1.  Después de elegir una combinación de colores, vuelva a cargar el documento actual para ver el modo simulado.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Modo de luz simulada dentro de Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Modo de luz simulada dentro de Microsoft Edge DevTools  
    :::image-end:::  
    
    Ver y cambiar su CSS, como cualquier otra página web.  Para obtener más información, consulte Introducción [a la visualización y el cambio de CSS][DevtoolsGuideChromiumCssIndex].  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Habilitar tema oscuro en Microsoft Edge DevTools | Microsoft docs"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Introducción a la visualización y el cambio de CSS | Microsoft docs"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "preferida-combinación de colores | MDN"  

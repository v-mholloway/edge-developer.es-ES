---
description: Fuerza Microsoft Edge DevTools al modo de vista previa de esquema de color.
title: Forzar Microsoft Edge DevTools en modo de vista previa de esquema de color (CSS prefiere combinación de colores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 1cdc9601e9e6fea1f6921c6cc40a1ed8232a0da8
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519152"
---
# <a name="dark-or-light-color-scheme-simulation"></a>Simulación de combinación de colores claros o oscuros  

Los sistemas operativos tienen una forma de mostrar cualquier aplicación en colores más oscuros o más claros.  Tener un producto web que tenga un tema claro en un sistema operativo en modo oscuro es una rejilla y puede ser un problema de accesibilidad para algunos usuarios.  En la web, puede usar la consulta multimedia CSS [prefers-color-scheme][MDNPrefersColorScheme] para detectar si los usuarios prefieren mostrar el producto en una combinación de colores más oscura o más clara.  Usa [Microsoft Edge DevTools para][DevtoolsIndex] simular un cambio del modo oscuro a el modo claro sin tener que cambiar todo el sistema operativo.  

1.  Abra el **Menú de comandos**.  
    1.  Seleccione `Ctrl` + `Shift` + `P` \(Windows/Linux\) o `Command` + `Shift` + `P` \(macOS\).  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menú comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Menú **comando**  
        :::image-end:::  
        
1.  Type `emulate color` , choose either Emulate CSS **prefers-color-scheme: dark** or Emulate CSS **prefers-color-scheme: light** and then select `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Opción combinación de colores del menú comando" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       Opción combinación de colores del **menú** comando  
    :::image-end:::  
    
    > [!IMPORTANT]
    > Simplemente escribiendo o no revela la herramienta adecuada, ya que también hay una forma de `dark` elegir un tema para `light` [DevTools][DevtoolsCustomizeDarkTheme].  Si se pregunta qué elegir, asegúrese de elegir **** un elemento de menú de representación, no un **elemento de** menú de apariencia.  

1.  Después de elegir una combinación de colores, actualice el documento actual para mostrar el modo simulado.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Modo de luz simulada dentro Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Modo de luz simulada dentro Microsoft Edge DevTools  
    :::image-end:::  
    
    Ver y cambiar el CSS como cualquier otra página web.  Para obtener más información, vaya [a Introducción Con ver y cambiar CSS][DevtoolsCssIndex].  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Habilitar tema oscuro en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCssIndex]: ../css/index.md "Introducción Con vista y cambio de CSS | Microsoft Docs"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  

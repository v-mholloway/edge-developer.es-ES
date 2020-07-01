---
title: Simular un movimiento reducido con herramientas de desarrollo (CSS prefiere reducir el movimiento)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f1bf90de4ac1832fff07e9ac963c26f92adeea2c
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843987"
---
# Simulación de movimiento reducida  

La animación en productos Web puede ser un problema de accesibilidad.  Los sistemas operativos se enfrentan al problema incluyendo una opción para desactivar las animaciones para evitar la confusión de los usuarios y posibles problemas relacionados con el estado, como desencadenar ataques.  En la web, puede usar la consulta de medios [preferidas, de CSS de movimiento reducido][MDNPrefersReducedMotion] para detectar si los usuarios prefieren ver las animaciones.  En el producto, puede ajustar el código de la animación en una prueba para evitar que se muestren animaciones para los usuarios afectados.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

Con el [DevTools de Microsoft Edge][DevtoolsGuideChromiumMain], puede simular esta configuración de movimiento reducida sin necesidad de cambiar el sistema operativo.  

1.  Abrir el **menú de comandos**.  
    1.  Pulse `Control` + `Shift` + `P` en Windows o `Command` + `Shift` + `P` en MacOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           El **menú de comandos**  
        :::image-end:::   
        
1.  Escriba `reduced` para activar y desactivar la simulación.  Seleccione la opción y pulse `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activar o desactivar la opción de configuración reducir el movimiento preferido desde el menú de comandos" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Activar o desactivar la opción de configuración **reducir el movimiento preferido** desde el **menú de comandos**  
    :::image-end:::  
    
1.  Actualice la página actual para comprobar si las animaciones están activadas o visibles.  
    
<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Ilustración 1: el menú de comandos"  
[ImageToggleReducedMotionFromCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png "Ilustración 2: conmutar movimiento reducido desde la paleta de comandos"

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) Microsoft | Microsoft docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion "preferido: ahorro: movimiento | MDN"  

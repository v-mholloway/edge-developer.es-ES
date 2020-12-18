---
description: Simular el movimiento reducido con las herramientas de desarrollo.
title: Simular un movimiento reducido con herramientas de desarrollo (CSS prefiere reducir el movimiento)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0e5243e01ca6c9344dceffb0bf004dadccc3d4d7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230792"
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

Con el [DevTools de Microsoft Edge][DevtoolsIndex], puede simular esta configuración de movimiento reducida sin necesidad de cambiar el sistema operativo.  

1.  Abrir el **menú de comandos**.  
    1.  Seleccione `Control` + `Shift` + `P` en Windows/Linux o `Command` + `Shift` + `P` en MacOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           El **menú de comandos**  
        :::image-end:::  
        
1.  Escriba `reduced` para activar y desactivar la simulación.  Elija la opción y seleccione `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activar o desactivar la opción de configuración reducir el movimiento preferido desde el menú de comandos" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Activar o desactivar la opción de configuración **reducir el movimiento preferido** desde el **menú de comandos**  
    :::image-end:::  
    
1.  Actualice la página actual para comprobar si las animaciones están activadas o visibles.  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "preferido: ahorro: movimiento | MDN"  

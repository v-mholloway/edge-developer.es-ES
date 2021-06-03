---
description: Simular movimiento reducido con herramientas de desarrollador.
title: Simular movimiento reducido con herramientas de desarrollador (CSS prefiere el movimiento reducido)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 29cdbd7492665e819315910b3f743d444470cc12
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397870"
---
# <a name="reduced-motion-simulation"></a>Simulación de movimiento reducida  

La animación en productos web puede ser un problema de accesibilidad.  Los sistemas operativos tratan el problema mediante la inclusión de una opción para desactivar animaciones para evitar confusiones del usuario y posibles problemas relacionados con el estado, como desencadenar ataques.  En la web, puede usar la consulta multimedia CSS [prefers-reduced-motion][MDNPrefersReducedMotion] para detectar si los usuarios prefieren no ejecutar o mostrar animaciones.  En el producto, puedes ajustar el código de animación en una prueba para evitar que se muestren animaciones para los usuarios afectados.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

Con el [Microsoft Edge DevTools,][DevtoolsIndex]puedes simular esta configuración de movimiento reducido sin tener que cambiar el sistema operativo.  

1.  Abra el **Menú de comandos**.  
    1.  Seleccione `Control` + `Shift` + `P` en Windows/Linux o `Command` + `Shift` + `P` en macOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menú comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Menú **comando**  
        :::image-end:::  
        
1.  Escriba `reduced` , para activar y desactivar la simulación.  Elija la opción y seleccione `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activar o desactivar la configuración de movimiento reducido preferido desde el menú comando" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Activar o desactivar la configuración **de movimiento reducido** preferido desde el menú **comando**  
    :::image-end:::  
    
1.  Actualice la página actual para comprobar si las animaciones están desactivadas o visibles.  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  

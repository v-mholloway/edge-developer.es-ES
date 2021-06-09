---
description: Simular movimiento reducido con herramientas de desarrollador.
title: Simular movimiento reducido con herramientas de desarrollador (CSS prefiere el movimiento reducido)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7244c2e80bbf9070214b6abd02583792c785953c
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597057"
---
# <a name="reduced-motion-simulation"></a>Simulación de movimiento reducida  

La animación en productos web puede ser un problema de accesibilidad.  Los sistemas operativos tratan este problema al incluir una opción para desactivar animaciones para evitar confusiones del usuario y posibles problemas relacionados con el estado, como desencadenar ataques.  

En una página web, puede usar la consulta multimedia [CSS][MDNPrefersReducedMotion] de movimiento reducido preferido para detectar si el usuario prefiere mostrar animaciones.  A continuación, ajusta el código de animación en una prueba para ejecutar animaciones condicionalmente.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

A continuación, pruebe el código de la siguiente manera.

Para simular la configuración de movimiento reducido del sistema operativo, sin tener que cambiar la configuración del sistema operativo:

1.  Abra el **Menú de comandos**.  
    1.  Seleccione `Control` + `Shift` + `P` en Windows/Linux o `Command` + `Shift` + `P` en macOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menú comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Menú **comando**  
        :::image-end:::  
        
1.  Escriba `reduced` , para activar y desactivar la simulación.  Elija la opción y seleccione `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activar o desactivar la configuración de movimiento reducido preferido desde el menú comando" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Activar o desactivar la configuración **de movimiento reducido** preferido desde el menú **comando**  
    :::image-end:::  
    
1.  Actualice la página web y compruebe si se ejecutan las animaciones.


## <a name="see-also"></a>Consulta también

* [Compruebe que la página se puede usar con la animación](test-reduced-ui-motion.md) de la interfaz de usuario desactivada: un tutorial con una página de demostración, con explicaciones.

    
<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  

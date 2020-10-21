---
description: Cómo mover Microsoft Edge DevTools a la parte inferior o a la izquierda de la ventanilla o a una ventana independiente.
title: Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 65c0849af5da671bb0d76397d6d9395bc249eaac
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125051"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)  

De forma predeterminada DevTools se acopla a la derecha de la ventanilla.  También puede acoplar a la parte inferior, acoplar a la izquierda o desacoplar el DevTools en una ventana independiente.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-right-docked.msft.png" alt-text="Seleccionar acoplar a la izquierda" lightbox="../media/customize-elements-styles-right-docked.msft.png":::
         Seleccionar `Dock To Left`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-bottom-docked.msft.png" alt-text="Seleccionar acoplar a la izquierda" lightbox="../media/customize-elements-styles-bottom-docked.msft.png":::
         Seleccionar `Dock To Bottom`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight-browser.msft.png" alt-text="Seleccionar acoplar a la izquierda" lightbox="../media/customize-elements-styles-options-dock-side-highlight-browser.msft.png":::
         Explorador en una ventana independiente  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png" alt-text="Seleccionar acoplar a la izquierda" lightbox="../media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png":::
         DevTools desacoplado en una ventana independiente  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Cambiar la ubicación desde el menú principal  

1.  Elija **personalizar y controlar DevTools** \ ( `...` \) y seleccione **desacoplar en ventana independiente** \ ( ![ desacoplar ][ImageUndockIcon] \), **acoplar en la parte inferior** \ ( ![ acoplar a la inferior ][ImageBottomIcon] \) o **acoplar** a la izquierda \ ( ![ acoplar a la izquierda ][ImageLeftIcon] \).  
    
    :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight.msft.png" alt-text="Seleccionar acoplar a la izquierda" lightbox="../media/customize-elements-styles-options-dock-side-highlight.msft.png":::
       Seleccione **desacoplar en ventana independiente**  
    :::image-end:::  
    
## Cambiar la ubicación desde el menú de comandos  

1.  [Abrir el menú de comandos][DevtoolsCommandMenu].  
1.  Ejecute uno de los siguientes comandos: `Dock To Bottom` , `Undock Into Separate Window` .  Por el momento, no hay ningún comando para acoplar a la izquierda, pero puede acceder a él desde el [menú principal](#change-placement-from-the-main-menu).  
    
    :::image type="complex" source="../media/customize-elements-styles-command-menu-undo.msft.png" alt-text="Seleccionar acoplar a la izquierda" lightbox="../media/customize-elements-styles-command-menu-undo.msft.png":::
       El comando desacoplar  
    :::image-end:::  
    
## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageUndockIcon]: ../media/undock-icon.msft.png  
[ImageBottomIcon]: ../media/bottom-icon.msft.png  
[ImageLeftIcon]: ../media/left-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenu]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/customize/placement) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
title: Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f0be6243d4780e4ed49428ebaf2b6b37d9da323e
ms.sourcegitcommit: 67ce64f810afdb304844bae0f3918d4e9108dcec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/24/2020
ms.locfileid: "10601349"
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

> ##### Figura 1  
> Acoplar a la izquierda  
> ![Acoplar a la izquierda][ImageDockLeft]  

> ##### Figura 2  
> Acoplar a la parte inferior  
> ![Acoplar a la parte inferior][ImageDockBottom]  

> ##### Imagen 3  
> Explorador en una ventana independiente  
> ![Explorador en una ventana independiente][ImageUndockBrowser]  

> ##### Imagen 4  
> DevTools desacoplado en una ventana independiente  
> ![DevTools desacoplado en una ventana independiente][ImageUndockDevTools]  

## Cambiar la ubicación desde el menú principal   

1.  Haga clic en **personalizar y controlar DevTools** `...` y seleccione **desacoplar en** ![ desacoplar ventana separada ][ImageUndockIcon] , **acoplar** a acoplar en la parte inferior ![ ][ImageBottomIcon] o en **acoplar a** la izquierda ![ acoplar a la izquierda ][ImageLeftIcon] .  
    
    > ##### Imagen 5  
    > Seleccionar **desacoplar en una ventana independiente**  
    > ![Seleccionar desacoplar en una ventana independiente][ImageUndockSettings]  
    
## Cambiar la ubicación desde el menú de comandos   

1.  [Abrir el menú de comandos][DevtoolsCommandMenu].  
1.  Ejecute uno de los siguientes comandos: `Dock To Bottom` , `Undock Into Separate Window` .  Por el momento, no hay ningún comando para acoplar a la izquierda, pero puede acceder a él desde el [menú principal](#change-placement-from-the-main-menu).  
    
    > ##### Imagen 6  
    > El comando desacoplar  
    > ![El comando desacoplar][ImageUndockCommand]  

 



<!-- image links -->  

[ImageUndockIcon]: /microsoft-edge/devtools-guide-chromium/media/undock-icon.msft.png  
[ImageBottomIcon]: /microsoft-edge/devtools-guide-chromium/media/bottom-icon.msft.png  
[ImageLeftIcon]: /microsoft-edge/devtools-guide-chromium/media/left-icon.msft.png  

[ImageDockLeft]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-right-docked.msft.png "Ilustración 1: acoplar a la izquierda"  
[ImageDockBottom]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-bottom-docked.msft.png "Ilustración 2: acoplar a la parte inferior"  
[ImageUndockBrowser]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-browser.msft.png "Ilustración 3: explorador en una ventana independiente"  
[ImageUndockDevTools]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png "Ilustración 4: DevTools desacoplado en una ventana independiente"  
[ImageUndockSettings]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight.msft.png "Ilustración 5: seleccionar desacoplar en una ventana independiente"  
[ImageUndockCommand]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-command-menu-undo.msft.png "Ilustración 6: el comando desacoplable"  

<!-- links -->  

[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/customize/placement) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

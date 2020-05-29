---
title: Personalizar Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 42c1cce2ca26c81b0482429cface83f09e34f5df
ms.sourcegitcommit: 67ce64f810afdb304844bae0f3918d4e9108dcec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/24/2020
ms.locfileid: "10601356"
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





# Personalizar Microsoft Edge DevTools   

  

Esta página muestra las formas de personalizar Microsoft Edge DevTools.  

## Configuración   

**Configuración**  >  **Preferencias** contiene muchas opciones para personalizar DevTools.  

Para abrir la configuración, siga uno de estos procedimientos:  

*   Pulsa `F1` mientras DevTools el foco.  
*   Abra el **menú principal** y, a continuación, seleccione **configuración**.  

> ##### Figura 1  
> Configuración  
> ![Configuración][ImageSettings]  

## Ventana   

El **cajón** contiene muchas características ocultas.  

Pulse `Escape` para abrir o cerrar el cajón.  

> ##### Figura 2  
> El cajón  
> ![El cajón][ImageDrawerExample]  

Haga clic en **más** ![ ][ImageMoreIcon] para abrir las pestañas de otros cajón.  

> ##### Imagen 3  
> El botón para abrir las pestañas de cajón  
> ![El botón para abrir las pestañas de cajón][ImageMoreDrawerTabs]  

## Reordenar paneles   

Haga clic y arrastre una pestaña de panel para cambiar su orden.  El orden de tabulación personalizado se conserva en todas las sesiones de DevTools.  

> [!NOTE]
> De forma predeterminada, la ficha panel de red suele ser la cuarta de la izquierda.  En la [figura 4](#figure-4), es la primera de la izquierda.  

> ##### Imagen 4  
> Una ventana de DevTools con un orden de tabulación personalizado    
> ![Una ventana de DevTools con un orden de tabulación de panel personalizado][ImageCustomTabOrdering]  

## Cambiar la ubicación de DevTools   

Vea [Ubicación de Microsoft Edge DevTools][DevToolsPlacement].  

> ##### Imagen 5  
> DevTools desacoplado  
> ![DevTools desacoplado][ImageUndock]  

## Tema oscuro   

Consulte [Habilitar tema oscuro][DarkTheme].  

> ##### Imagen 6  
> El tema oscuro  
> ![El tema oscuro][ImageDarkTheme]  

## Experimentos   

Para habilitar los experimentos de DevTools:  

1.  Vaya a `edge://flags/#enable-devtools-experiments` .  
1.  Haz clic en **Habilitar**.  
1.  Haga clic en volver a **Ejecutar ahora**, en la parte inferior de la página.  

La próxima vez que abras DevTools, se mostrará una página nueva llamada **experimentos** en [configuración](#settings).  

   

  

<!-- image links -->  

[ImageMoreIcon]: /microsoft-edge/devtools-guide-chromium/media/more-icon.msft.png  

[ImageSettings]: /microsoft-edge/devtools-guide-chromium/media/customize-settings-preferences.msft.png "Ilustración 1: configuración"  
[ImageDrawerExample]: /microsoft-edge/devtools-guide-chromium/media/customize-drawer-open.msft.png "Ilustración 2: el cajón"  
[ImageMoreDrawerTabs]: /microsoft-edge/devtools-guide-chromium/media/customize-drawer-open-more-tools.msft.png "Ilustración 3: el botón para abrir las pestañas de un cajón"  
[ImageCustomTabOrdering]: /microsoft-edge/devtools-guide-chromium/media/customize-network-first-position.msft.png "Ilustración 4: una ventana de DevTools con un orden de tabulación de panel personalizado"  
[ImageUndock]: /microsoft-edge/devtools-guide-chromium/media/customize-dev-tools-dock-side.msft.png "Ilustración 5: DevTools desacoplado"  
[ImageDarkTheme]: /microsoft-edge/devtools-guide-chromium/media/customize-settings-appearance-theme.msft.png "Ilustración 6: el tema oscuro"  

<!-- links -->  

[DevToolsPlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  
[DarkTheme]: /microsoft-edge/devtools-guide-chromium/customize/dark-theme "Habilitar tema oscuro en Microsoft Edge DevTools"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/customize/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

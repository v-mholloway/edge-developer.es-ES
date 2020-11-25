---
description: Una lista de formas de personalizar Microsoft Edge DevTools
title: Personalizar Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 682ff78b6a5272c1f6462648d64241448838edac
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "11189997"
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

Para abrir la configuración, complete una de las siguientes acciones.  

*   Seleccione `F1` mientras la DevTools está en el foco.  
*   Abra el **menú principal** y, a continuación, elija **configuración**.  
    
:::image type="complex" source="../media/customize-settings-preferences.msft.png" alt-text="Configuración" lightbox="../media/customize-settings-preferences.msft.png":::
   **Configuración**  
:::image-end:::  

## Ventana  

El **cajón** es un segundo panel en el que se muestran las herramientas de su elección.  

Para abrir \ (o cerrar \) el **cajón**, seleccione `Escape` .  

:::image type="complex" source="../media/customize-drawer-open.msft.png" alt-text="El cajón" lightbox="../media/customize-drawer-open.msft.png":::
   El **cajón**  
:::image-end:::  

De forma predeterminada, algunas herramientas se abren en el panel principal, mientras que otras aparecen en el **cajón**.  Elija **más** \ ( `...` ) para abrir una herramienta en el **cajón**.  

:::image type="complex" source="../media/customize-drawer-open-more-tools.msft.png" alt-text="Botón para abrir el cajón" lightbox="../media/customize-drawer-open-more-tools.msft.png":::
   Botón para abrir el **cajón**  
:::image-end:::  

Puede mover herramientas entre el panel principal y el alimentador.  

*   Para mover una herramienta del cajón al panel principal, desplace el puntero sobre una herramienta, abra el menú contextual \ (haga clic con el botón derecho \) y elija **mover a la parte superior**.  
    
    :::image type="complex" source="../media/move-from-drawer.msft.png" alt-text="Mover la herramienta del cajón al panel principal" lightbox="../media/move-from-drawer.msft.png":::
       Mover la herramienta del **cajón** al panel principal  
    :::image-end:::  
    
*   Para mover una herramienta del panel principal al cajón, desplace el puntero sobre una herramienta, abra el menú contextual \ (haga clic con el botón derecho \) y elija **mover a la parte inferior**.  
    
    :::image type="complex" source="../media/move-to-drawer.msft.png" alt-text="Mover la herramienta del panel principal al cajón" lightbox="../media/move-to-drawer.msft.png":::
       Mover la herramienta del panel principal al **cajón**
    :::image-end:::  
    

## Reordenar paneles  

Elija y arrastre una herramienta para cambiar el orden.  El orden de la herramienta personalizada se conserva en todas las sesiones de DevTools.  

> [!NOTE]
> De forma predeterminada, la herramienta **red** suele ser la cuarta de la izquierda.  En la siguiente ilustración, el panel **red** es el primero de la izquierda.  

:::image type="complex" source="../media/customize-network-first-position.msft.png" alt-text="Orden personalizado de DevTools en un panel" lightbox="../media/customize-network-first-position.msft.png":::
   Orden personalizado de DevTools en un panel  
:::image-end:::  

## Cambiar la ubicación de DevTools  

Vea [Ubicación de Microsoft Edge DevTools][DevToolsPlacement].  

:::image type="complex" source="../media/customize-dev-tools-dock-side.msft.png" alt-text="DevTools desacoplado" lightbox="../media/customize-dev-tools-dock-side.msft.png":::
   DevTools desacoplado  
:::image-end:::  

## Tema oscuro  

Consulte [Habilitar tema oscuro][DarkTheme].  

:::image type="complex" source="../media/customize-settings-appearance-theme.msft.png" alt-text="El tema oscuro" lightbox="../media/customize-settings-appearance-theme.msft.png":::
   El tema oscuro  
:::image-end:::  

## Experimentos  

Para habilitar experimentos DevTools, complete las siguientes acciones.  

1.  Vaya a `edge://flags/#enable-devtools-experiments` .  
1.  Elija **Habilitar**.  
1.  Seleccione volver a **iniciar ahora**, en la parte inferior de la página.  

La próxima vez que abras DevTools, aparecerá en [configuración](#settings)una nueva página con el nombre **experimentos** .  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreIcon]: ../media/more-icon.msft.png  

<!-- links -->  

[DevToolsPlacement]: ./placement.md "Cambiar la ubicación de DevTools de Microsoft Edge | Microsoft docs"  
[DarkTheme]: ./dark-theme.md "Habilitar tema oscuro en Microsoft Edge DevTools | Microsoft docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/customize/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

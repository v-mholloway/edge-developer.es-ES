---
description: Una lista de formas de personalizar Microsoft Edge DevTools
title: Personalizar Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 073c4f8c5d899e2e9cf4cc2f72882d1c009544f4
ms.sourcegitcommit: 01ed086305c06b4e3a0436586524986700276148
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/14/2021
ms.locfileid: "11893059"
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
# <a name="customize-microsoft-edge-devtools"></a>Personalizar Microsoft Edge DevTools  

En esta página se enumeran las formas de personalizar Microsoft Edge DevTools.  

## <a name="settings"></a>Configuración  

**Configuración**  >  **Las** preferencias contienen muchas opciones para personalizar DevTools.  

Para abrir Configuración, realice una de las siguientes acciones.
*   En DevTools, seleccione el **icono Configuración** \( Configuración ![ icono ](../media/settings-icon-dark.msft.png) \).
*   Mientras DevTools tenga el foco, seleccione `F1` .
    
:::image type="complex" source="../media/customize-settings-preferences.msft.png" alt-text="Configuración" lightbox="../media/customize-settings-preferences.msft.png":::
   **Configuración**  
:::image-end:::  

## <a name="drawer"></a>Cajón  

El **cajón** es un segundo panel donde puede elegir qué herramientas mostrar.  

Para abrir \(o cerrar\) el **cajón**, seleccione `Escape` .  

:::image type="complex" source="../media/customize-drawer-open.msft.png" alt-text="El cajón" lightbox="../media/customize-drawer-open.msft.png":::
   El **cajón**  
:::image-end:::  

De forma predeterminada, algunas herramientas se abren en el panel principal, mientras que otras aparecen en el **cajón**.  Seleccione **Más** \( `...` \) para abrir una herramienta en el **cajón**.  

:::image type="complex" source="../media/customize-drawer-open-more-tools.msft.png" alt-text="Botón para abrir el cajón" lightbox="../media/customize-drawer-open-more-tools.msft.png":::
   Botón para abrir el **cajón**  
:::image-end:::  

Puede mover herramientas entre el panel principal y el cajón.  

*   Para mover una herramienta del cajón al panel principal, mantenga el mouse sobre una herramienta, abra el menú contextual \(hacer clic con el botón derecho\) y seleccione **Mover a la parte superior**.  
    
    :::image type="complex" source="../media/move-from-drawer.msft.png" alt-text="Mover la herramienta del cajón al panel principal" lightbox="../media/move-from-drawer.msft.png":::
       Mover la herramienta del **cajón** al panel principal  
    :::image-end:::  
    
*   Para mover una herramienta del panel principal al cajón, mantenga el mouse sobre una herramienta, abra el menú contextual \(clic con el botón derecho\) y seleccione **Mover a la parte inferior**.  
    
    :::image type="complex" source="../media/move-to-drawer.msft.png" alt-text="Mover la herramienta desde el panel principal al cajón" lightbox="../media/move-to-drawer.msft.png":::
       Mover la herramienta desde el panel principal al **cajón**
    :::image-end:::  
    

## <a name="reorder-panels"></a>Reordenar paneles  

Seleccione y arrastre una herramienta para cambiar el orden.  El orden de la herramienta personalizada persiste en las sesiones de DevTools.  

> [!NOTE]
> De forma predeterminada, la **herramienta Red** suele ser la cuarta desde la izquierda.  En la siguiente figura, la **herramienta Red** es la primera desde la izquierda.  

:::image type="complex" source="../media/customize-network-first-position.msft.png" alt-text="Orden personalizado de Devtools en un panel" lightbox="../media/customize-network-first-position.msft.png":::
   Orden personalizado de Devtools en un panel  
:::image-end:::  

## <a name="change-devtools-placement"></a>Cambiar la ubicación de DevTools  

Vaya a [Microsoft Edge ubicación de DevTools][DevToolsPlacement].  

:::image type="complex" source="../media/customize-dev-tools-dock-side.msft.png" alt-text="DevTools desacopladas" lightbox="../media/customize-dev-tools-dock-side.msft.png":::
   DevTools desacopladas  
:::image-end:::  

## <a name="theme"></a>Tema  

Vaya a [Aplicar temas de color a DevTools][Theme].  

:::image type="complex" source="./media/customize-theme-setting.png" alt-text="Selección de un tema de color diferente" lightbox="./media/customize-theme-setting.png":::
   Selección de un tema de color diferente  
:::image-end:::  

## <a name="experiments"></a>Experimentos  

Para activar los experimentos de DevTools, realice las siguientes acciones.  

1.  Vaya a `edge://flags/#enable-devtools-experiments`.  
1.  Seleccione **Habilitar**.  
1.  Seleccione **Volver a iniciar ahora**, en la parte inferior de la página.  

La próxima vez que abra DevTools, se mostrará una nueva página denominada **Experiments** en [Configuración](#settings).  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreIcon]: ../media/more-icon.msft.png  

<!-- links -->  

[DevToolsPlacement]: ./placement.md "Cambiar Microsoft Edge ubicación de DevTools | Microsoft Docs"  
[Theme]: ./theme.md "Aplicar temas de color a DevTools | Microsoft Docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/customize/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

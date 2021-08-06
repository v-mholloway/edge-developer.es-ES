---
description: Cómo mover de Microsoft Edge DevTools a la parte inferior o izquierda de la ventanilla, o a una ventana independiente.
title: Cambiar la ubicación de DevTools (Undock, Dock to bottom, Dock to left)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: ff28f8ed79998a929811e99cbe788f2b71131aa4503e13b97f33655a164a4ed9
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11800781"
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
# <a name="change-devtools-placement-undock-dock-to-bottom-dock-to-left"></a>Cambiar la ubicación de DevTools (Undock, Dock to bottom, Dock to left)  

De forma predeterminada, Microsoft Edge DevTools está acoplada a la derecha de la ventanilla (ventana).  También puede acoplar DevTools a la parte inferior o izquierda de la ventana, o desacoplar DevTools a una ventana independiente.

:::row:::
   :::column span="":::
      DevTools acoplada al lado izquierdo de la ventana:
   :::column-end:::
   :::column span="":::
      DevTools acoplada a la parte inferior de la ventana:
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-right-docked.msft.png" alt-text="Elija Dock a la izquierda" lightbox="../media/customize-elements-styles-right-docked.msft.png":::
         Elija **Dock a la izquierda**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-bottom-docked.msft.png" alt-text="Elija Acoplar en la parte inferior" lightbox="../media/customize-elements-styles-bottom-docked.msft.png":::
         Elegir `Dock to bottom`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

DevTools puede desacoplarse a una ventana independiente, que puede mover a un monitor independiente:

:::row:::
   :::column span="":::
      Ventana del explorador:
   :::column-end:::
   :::column span="":::
      DevTools se desacopla en una ventana independiente:
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight-browser.msft.png" alt-text="Explorador en ventana independiente" lightbox="../media/customize-elements-styles-options-dock-side-highlight-browser.msft.png":::
         Explorador en ventana independiente  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png" alt-text="DevTools desacoplado en una ventana independiente" lightbox="../media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png":::
         DevTools desacoplado en una ventana independiente  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="change-placement-from-the-main-menu"></a>Cambiar la ubicación desde el menú principal  

1.  Elija Personalizar y **controlar DevTools** \( \) y elija `...` **Undock into separate window** \( ![ Undock ](../media/undock-icon.msft.png) \), Dock to **bottom** \( Dock to ![ bottom ](../media/bottom-icon.msft.png) \) o Dock to **left** \( Dock to ![ left ](../media/left-icon.msft.png) \).  
    
    :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight.msft.png" alt-text="Elegir Desacoplar en ventana independiente" lightbox="../media/customize-elements-styles-options-dock-side-highlight.msft.png":::
       Elija **Desacoplar en una ventana independiente**  
    :::image-end:::  
    
## <a name="change-placement-from-the-command-menu"></a>Cambiar la ubicación desde el menú comando  

1.  [Abra el menú Comando][DevtoolsCommandMenu], `Shift` + `Ctrl` + `P` seleccionando en Windows/Linux o `Command` + `Shift` + `P` en macOS.  
1.  Después del `>` carácter, escriba y, a `dock` continuación, elija uno de los siguientes comandos:  
    
    *  **Acoplar a la parte inferior**
    *  **Acoplar a la izquierda**
    *  **Acoplar a la derecha**
    *  **Restaurar la última posición de acoplamiento**
    *  **Desacoplar en una ventana independiente**
    
    También puede tener acceso a los comandos desde el [menú principal](#change-placement-from-the-main-menu). 
    
    :::image type="complex" source="../media/customize-elements-styles-command-menu-undo.msft.png" alt-text="El comando Undock" lightbox="../media/customize-elements-styles-command-menu-undo.msft.png":::
       El comando Undock  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenu]: ../command-menu/index.md "Ejecute comandos con el menú de comandos de DevTools de Microsoft Edge | Microsoft Docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/customize/placement) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

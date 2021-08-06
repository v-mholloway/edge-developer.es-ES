---
description: Cómo aplicar diferentes temas de color a Microsoft Edge DevTools.
title: Aplicar temas de color a DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/03/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 93f7655d878375d946e78f5867b80d46522f4654cf42be4934920bfc6ccb0208
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11801937"
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
# <a name="apply-color-themes-to-devtools"></a>Aplicar temas de color a DevTools

Puede aplicar varios temas de color a Microsoft Edge DevTools, incluidos varios temas de [Visual Studio Code][VSCode], como Monokai y Solarized Dark.  Los temas afectan al color de los paneles, los botones y el resaltado de la sintaxis de código. 

:::image type="complex" source="./media/all-devtools-themes.png" alt-text="Varios temas de color de DevTools" lightbox="./media/all-devtools-themes.png":::
   Varios temas de color de DevTools
:::image-end:::  

> [!NOTE]
> Antes de [Microsoft Edge 93][WhatsNew93], DevTools solo tenía un tema claro y oscuro.  

Este artículo trata sobre cómo cambiar la apariencia de DevTools.  Para cambiar en su lugar cómo se muestra la página web en desarrollo, vaya a Emular esquemas oscuros o [claros en la página mostrada.][AccessibilityPreferredColorSchemeSimulation]


## <a name="available-themes"></a>Temas disponibles  

De forma predeterminada, el tema DevTools se establece en **Preferencia del** sistema (también denominado tema de color preferido **del sistema).**  Si el sistema operativo está establecido en tema Light, DevTools usa el **tema Light+.**  Si el sistema operativo está establecido en Tema oscuro, DevTools usa el **tema Dark+.**  Sin embargo, puedes cambiar DevTools a cualquiera de los otros temas, de modo que DevTools no se ve afectado al establecer el sistema operativo en Tema claro u oscuro.

Temas claros:  
- Light+ (valor predeterminado)  
- Chromium Luz  
- Luz silenciosa  
- Luz solarizada  

Temas oscuros:  
- Dark+ (valor predeterminado)  
- Abyss  
- Chromium Oscuro  
- Kimbie Dark  
- Monokai  
- Monokai atenuado  
- Rojo  
- Oscuro solarizado  
- Tomorrow Night Blue  

## <a name="changing-the-color-theme-from-settings"></a>Cambiar el tema de color desde Configuración

1.  Abra DevTools y, a **continuación, seleccione Configuración** (el icono de engranaje).

    :::image type="complex" source="./media/setting-button.png" alt-text="Icono Configuración (engranaje)" lightbox="./media/setting-button.png":::
       Icono **Configuración** (engranaje)  
    :::image-end:::  

1.  Selecciona **Preferencias**y, a continuación, en la **sección Apariencia,** selecciona un tema de la **lista** desplegable Tema.  
    
    :::image type="complex" source="./media/customize-theme-setting.png" alt-text="Seleccionar un tema en Preferencias" lightbox="./media/customize-theme-setting.png":::
       Seleccionar un tema en **Preferencias**  
    :::image-end:::  


## <a name="changing-the-color-theme-from-the-command-menu"></a>Cambiar el tema de color desde el menú comando

Para usar el menú comando para cambiar el tema de color que se aplica a DevTools:

1.  [Abra el menú de comandos][DevtoolsCommandMenu].  
1.  Escriba la palabra "tema".
1.  Seleccione un **comando Appearance** para el tema que desea usar.  Por ejemplo, **Appearance: Switch to Abyss theme** or **Appearance: Switch to Light+ (Default) theme**.
1.  Seleccione `Enter` para ejecutar el comando.  
    
    :::image type="complex" source="./media/customize-theme-command-menu.png" alt-text="La lista de temas del menú comando" lightbox="./media/customize-theme-command-menu.png":::
       La lista de temas del **menú comando**  
    :::image-end:::  


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  
[DevtoolsCommandMenu]: ../command-menu/index.md "Menú de comandos | Microsoft Docs"  
[WhatsNew93]: ../whats-new/2021/07/devtools.md "Novedades de DevTools (Microsoft Edge 93) | Microsoft Docs"  
[VSCode]: https://code.visualstudio.com  
[AccessibilityPreferredColorSchemeSimulation]: ../accessibility/preferred-color-scheme-simulation.md "Emular esquemas oscuros o claros en la página | Microsoft Docs"

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/customize/dark-theme) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  
[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

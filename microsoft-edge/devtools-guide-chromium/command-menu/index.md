---
description: Una guía sobre cómo abrir el menú comando, ejecutar comandos, revisar otras acciones y mucho más.
title: Ejecutar comandos con el menú Microsoft Edge comando DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 97603345173a7fdf0cf65968dd4ecbef85a146963176d0815361004137461c71
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11801570"
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
# <a name="run-commands-with-the-microsoft-edge-devtools-command-menu"></a>Ejecutar comandos con el menú Microsoft Edge comando DevTools  

El menú de comandos proporciona una forma rápida de navegar por la Microsoft Edge de DevTools y realizar tareas comunes, como [deshabilitar JavaScript][JavascriptDisable].  Es posible que esté familiarizado con una característica similar en Microsoft Visual Studio Code denominada paleta de comandos [,][VisualStudioCodeUICommandPalette]que fue la inspiración original del menú de comandos.  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Uso del menú comando para deshabilitar JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   Uso del menú comando para deshabilitar JavaScript  
:::image-end:::  

## <a name="open-the-command-menu"></a>Abrir el menú de comandos  

Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\). O elija **Personalizar y controlar DevTools** \( `...` \) > Ejecutar **comando**.  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Ejecutar comando" lightbox="../media/command-menu-options-run-command.msft.png":::
   Ejecutar comando  
:::image-end:::  

## <a name="display-other-available-actions"></a>Mostrar otras acciones disponibles  

Si usa el flujo de trabajo descrito en [Abrir el](#open-the-command-menu)menú de comandos , el menú comando se abre con un carácter previamente escrito en el cuadro de texto Menú `>` de comandos.  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="El carácter de comando" lightbox="../media/command-menu-run-command.msft.png":::
   El carácter de comando  
:::image-end:::  

Elimine el `>` carácter y el tipo para mostrar `?` otras acciones que están disponibles en el menú comando.  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Otras acciones disponibles" lightbox="../media/command-menu-help.msft.png":::
   Otras acciones disponibles  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Deshabilitar JavaScript con Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Paleta de comandos: Visual Studio Code interfaz de usuario"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

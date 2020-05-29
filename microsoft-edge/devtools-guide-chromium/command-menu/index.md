---
title: Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 748008b347a3498008748b9c3f9ecc1445c47f12
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601750"
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





# Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools   

  

El menú de comandos proporciona una forma rápida de navegar por la interfaz de usuario de Microsoft Edge DevTools y realizar tareas comunes, como la [deshabilitación de JavaScript][JavascriptDisable].  Es posible que esté familiarizado con una característica similar de Visual Studio que se denomina [paleta de comandos][VisualStudioCodeUICommandPalette], que es la inspiración original para el menú de comandos.  

> ##### Figura 1  
> Usar el menú de comandos para deshabilitar JavaScript  
> ![Usar el menú de comandos para deshabilitar JavaScript][ImageDisableJS]  

## Abrir el menú de comandos   

Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \). O bien, haga clic en **personalizar y controlar DevTools** `...` y, a continuación, seleccione **Ejecutar comando**.  

> ##### Figura 2  
> Comando ejecutar  
> ![Comando ejecutar][ImageRunCommand]  

## Ver otras acciones disponibles   

Si usa el flujo de trabajo esquematizado en [abrir el menú de comandos](#open-the-command-menu), el menú de comandos se abre con un `>` carácter antepuesto al cuadro de texto del menú de comandos.  

> ##### Imagen 3  
> El carácter de comando  
> ![El carácter de comando][ImageCommandCharacter]  

Elimine el `>` carácter y escriba `?` para ver otras acciones disponibles en el menú de comandos.  

> ##### Imagen 4  
> Otras acciones disponibles  
> ![Otras acciones disponibles][ImageActions]  

 



<!-- image links -->  

[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command-java.msft.png "Ilustración 1: usar el menú de comandos para deshabilitar JavaScript"  
[ImageRunCommand]: /microsoft-edge/devtools-guide-chromium/media/command-menu-options-run-command.msft.png "Ilustración 2: comando ejecutar"  
[ImageCommandCharacter]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command.msft.png "Ilustración 3: el carácter de comando"  
[ImageActions]: /microsoft-edge/devtools-guide-chromium/media/command-menu-help.msft.png "Ilustración 4: otras acciones disponibles"  

<!-- links -->  

[JavascriptDisable]: /microsoft-edge/devtools-guide-chromium/javascript/disable "Deshabilitar JavaScript con Microsoft Edge DevTools"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Paleta de comandos: interfaz de usuario de Visual Studio"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

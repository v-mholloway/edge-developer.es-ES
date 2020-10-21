---
description: Guía sobre cómo abrir el menú de comandos, ejecutar comandos, revisar otras acciones y mucho más.
title: Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 2f13461fdf04e034b324db63c6ec6d9090f80f50
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125282"
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

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Usar el menú de comandos para deshabilitar JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   Usar el menú de comandos para deshabilitar JavaScript  
:::image-end:::  

## Abrir el menú de comandos  

Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \). O elija **personalizar y controlar DevTools** `...` y, a continuación, elija **Ejecutar comando**.  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Usar el menú de comandos para deshabilitar JavaScript" lightbox="../media/command-menu-options-run-command.msft.png":::
   Comando ejecutar  
:::image-end:::  

## Ver otras acciones disponibles  

Si usa el flujo de trabajo esquematizado en [abrir el menú de comandos](#open-the-command-menu), el menú comando se abre con un `>` carácter preestablecido en el cuadro de texto del menú de comandos.  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Usar el menú de comandos para deshabilitar JavaScript" lightbox="../media/command-menu-run-command.msft.png":::
   El carácter de comando  
:::image-end:::  

Elimine el `>` carácter y escriba `?` para ver otras acciones disponibles en el menú de comandos.  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Usar el menú de comandos para deshabilitar JavaScript" lightbox="../media/command-menu-help.msft.png":::
   Otras acciones disponibles  
:::image-end:::  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Deshabilitar JavaScript con Microsoft Edge DevTools | Microsoft docs"  

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

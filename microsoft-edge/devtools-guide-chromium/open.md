---
description: Todas las formas en que se abre el DevTools de Microsoft Edge.
title: Abrir Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ffc05a1eff2cdb7f3020a7dbb853a7520a0502dd
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993600"
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
   limitations under the License. -->

# Abrir Microsoft Edge DevTools  

Hay muchas maneras de abrir Microsoft Edge DevTools, ya que cada usuario desea obtener acceso rápido a distintas partes de la interfaz de usuario de DevTools.  

## Abrir el panel elementos para inspeccionar el DOM o CSS  

Cada una de las siguientes tareas le permite inspeccionar los estilos o los atributos de un nodo DOM.

*   Mantenga el puntero sobre el elemento, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.  
*   Pulse `Control` + `Shift` + `C` \ (Windows \) o `Command` + `Option` + `C` \ (MacOS \).  Para obtener más información, vea [métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].  

:::image type="complex" source="./media/bing-right-click-inspect.msft.png" alt-text="La opción * * inspeccionar * *" lightbox="./media/bing-right-click-inspect.msft.png":::
   La opción **inspeccionar**  
:::image-end:::  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Abrir el panel de consola  

Cada una de las siguientes tareas le permite abrir el panel [consola][DevToolsConsoleIndex] para ver los mensajes registrados o ejecutar JavaScript.  

*   Siga estos pasos para abrir el panel de [consola][DevToolsConsoleIndex] .  
    
    1.  [Abra DevTools](#open-microsoft-edge-devtools).  
    1.  Seleccione el panel de [consola][DevToolsConsoleIndex] .  

*   Para ir directamente al panel de la [consola][DevToolsConsoleIndex] , pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).  Para obtener más información, vea [métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Abrir el panel anterior  

Para ir al panel anterior que tenía abierto, pulse `Control` + `Shift` + `I` \ (Windows \) o `Command` + `Option` + `I` \ (MacOS \).  Para obtener más información, vea [métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].  

## Abrir Microsoft Edge DevTools  

Cada una de las siguientes tareas le permite abrir DevTools.  

*   Siga estos pasos para abrir Microsoft Edge DevTools.  
    
    1.  Seleccione el  `...` icono \ (el icono **configuración y más** ).  
    1.  Seleccione **más herramientas**.  
    1.  Seleccione **herramientas de desarrollo**.  
    
*   Para abrir Microsoft Edge DevTools, pulse `F12` o `Control` + `Shift` + `I` \ (Windows \) o `Command` + `Option` + `I` \ (MacOS \).  Para obtener más información, vea [métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].  

:::image type="complex" source="./media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Abrir DevTools desde el menú principal de Microsoft Edge" lightbox="./media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Abrir DevTools desde el menú principal de Microsoft Edge  
:::image-end:::  

## DevTools de apertura automática en todas las pestañas nuevas  

Para abrir DevTools automáticamente en todas las pestañas nuevas, abra Microsoft Edge desde la línea de comandos y pase la `--auto-open-devtools-for-tabs` bandera.  

#### [CMD (Windows)](#tab/cmd-windows/)  

<a id="selenium-tools-install"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

#### [PowerShell (Windows)](#tab/powershell-windows/)  

<a id="selenium-tools-install"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

#### [Bash (macOS)](#tab/bash-macos/)  

<a id="selenium-tools-install"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

* * *  

<!-- links -->  

[DevToolsConsoleIndex]: ./console/index.md "Descripción general de la consola | Microsoft docs"  
[DevtoolsShortcuts]: ./shortcuts.md "Métodos abreviados de teclado de Microsoft Edge DevTools-Microsoft docs"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/open) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

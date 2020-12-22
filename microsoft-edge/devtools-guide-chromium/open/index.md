---
description: Todas las formas en que se abre el DevTools de Microsoft Edge.
title: Abrir Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d21ebbf0b84be757c1b7a69d36b3bd3cc8403c6d
ms.sourcegitcommit: 77c8f42cc84600c2b853b15aaaecf0749b74bb01
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/22/2020
ms.locfileid: "11238232"
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

*   Mantenga el puntero sobre el elemento, abra el menú contextual \ (haga clic con el botón derecho \) y elija **inspeccionar**.  
*   Seleccione `Control` + `Shift` + `C` \ (Windows, Linux \) o `Command` + `Option` + `C` \ (MacOS \).  Para obtener más información, vaya a [métodos abreviados de teclado de Microsoft Edge DevTools][DevtoolsShortcutsIndex].  

:::image type="complex" source="../media/bing-right-click-inspect.msft.png" alt-text="La opción inspeccionar" lightbox="../media/bing-right-click-inspect.msft.png":::
   La opción **inspeccionar**  
:::image-end:::  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Abrir el panel de consola  

Cada una de las siguientes tareas le permite abrir el panel [consola][DevtoolsConsoleIndex] para ver los mensajes registrados o ejecutar JavaScript.  

*   Siga estos pasos para abrir el panel de [consola][DevtoolsConsoleIndex] .  
    
    1.  [Abra DevTools](#open-microsoft-edge-devtools).  
    1.  Seleccione el panel de [consola][DevtoolsConsoleIndex] .  

*   Para ir directamente al panel de la [consola][DevtoolsConsoleIndex] , seleccione `Control` + `Shift` + `J` \ (Windows, Linux \) o `Command` + `Option` + `J` \ (MacOS \).  Para obtener más información, vaya a [métodos abreviados de teclado de Microsoft Edge DevTools][DevtoolsShortcutsIndex].  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Abrir el panel anterior  

Para ir al panel anterior que tenía abierto, seleccione `Control` + `Shift` + `I` \ (Windows, Linux \) o `Command` + `Option` + `I` \ (MacOS \).  Para obtener más información, vaya a [métodos abreviados de teclado de Microsoft Edge DevTools][DevtoolsShortcutsIndex].  

## Abrir Microsoft Edge DevTools  

Para abrir DevTools, use una de las siguientes opciones.  

*   Use la interfaz de usuario de Microsoft Edge.  
    
    1.  Seleccione el icono **configuración y más** \ ( `...` \).  
    1.  Elija **más herramientas**.  
    1.  Elija **herramientas de desarrollo**.  
    
*   Use el teclado.  
    *   Seleccione `F12` o `Control` + `Shift` + `I` \ (Windows, Linux \) o `Command` + `Option` + `I` \ (MacOS \).  

Para obtener más información, vaya a [métodos abreviados de teclado de Microsoft Edge DevTools][DevtoolsShortcutsIndex].  

:::image type="complex" source="../media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Abrir DevTools desde el menú principal de Microsoft Edge" lightbox="../media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Abrir DevTools desde el menú principal de Microsoft Edge  
:::image-end:::  

## DevTools de apertura automática en todas las pestañas nuevas  

Para abrir DevTools automáticamente en todas las pestañas nuevas, abra Microsoft Edge desde la línea de comandos y pase la `--auto-open-devtools-for-tabs` bandera.  

### [CMD (Windows)](#tab/cmd-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

### [PowerShell (Windows)](#tab/powershell-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

### [Bash (macOS)](#tab/bash-macos/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

### [Bash (Linux)](#tab/bash-linux/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
microsoft-edge-dev --auto-open-devtools-for-tabs
```  

* * *  

## Activar o desactivar el método abreviado de teclado F12  

Para cambiar la `F12` configuración del método abreviado de teclado que abre el DevTools, complete las siguientes acciones.  

1.  Elija el icono **configuración y más** icono \ ( `...` \) > **configuración**.  
1.  En **configuración de búsqueda**, escriba `Developer Tools` .  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-on.msft.png" alt-text="La opción abrir la DevTools cuando se presiona la tecla F12" lightbox="../media/settings-developer-tools-f12-on.msft.png":::
       La opción **abrir la DevTools cuando se presiona la tecla F12**  
    :::image-end:::  
    
1.  Elija **abrir la DevTools cuando se presione la tecla F12** para alternar la configuración a desactivado \ (o en \).  Cambie la configuración a desactivado para evitar que el `F12` método abreviado de teclado abra DevTools.  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-off.msft.png" alt-text="La opción abrir la DevTools cuando se presiona la tecla F12 está desactivada" lightbox="../media/settings-developer-tools-f12-off.msft.png":::
       La opción **abrir la DevTools cuando se presiona la tecla F12** está desactivada  
    :::image-end:::  
    
1.  Después de establecer el botón de alternancia en desactivado, seleccione `F12` para confirmar que DevTools ya no se abre.  
    
    > [!NOTE]
    > Después de desactivar la opción **abrir la DevTools al presionar la tecla F12** , para abrir la DevTools, realice una de las siguientes acciones.  
    > 
    > *   Seleccione `Ctrl` + `Shift` + `I` .  
    > *   Abra el menú contextual \ (haga clic con el botón derecho \) > **inspeccionar**.  
    
## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Descripción general de la consola | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft docs"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/open) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

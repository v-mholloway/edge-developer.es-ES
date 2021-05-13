---
description: Todas las formas en que se abre el Microsoft Edge DevTools.
title: Abrir Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f5e011edd9889f226d705e51838e5d73c2a3b98d
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564738"
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
# <a name="open-microsoft-edge-devtools"></a>Abrir Microsoft Edge DevTools  

Hay muchas maneras de abrir Microsoft Edge DevTools, ya que diferentes usuarios desean un acceso rápido a diferentes partes de la interfaz de usuario de DevTools.  

## <a name="open-the-elements-panel-to-inspect-the-dom-or-css"></a>Abra el panel Elementos para inspeccionar el DOM o CSS  

Cada una de las siguientes tareas permite inspeccionar los estilos o atributos de un nodo DOM.

*   Mantenga el mouse sobre el elemento, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.  
*   Seleccione `Control` + `Shift` + `C` \(Windows, Linux\) o `Command` + `Option` + `C` \(macOS\).  Para obtener más información, vaya [a Microsoft Edge métodos abreviados de teclado de DevTools][DevtoolsShortcutsIndex].  

:::image type="complex" source="../media/bing-right-click-inspect.msft.png" alt-text="La opción Inspeccionar" lightbox="../media/bing-right-click-inspect.msft.png":::
   La **opción Inspeccionar**  
:::image-end:::  

<!--Navigate to [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## <a name="open-the-console-panel"></a>Abrir el panel Consola  

Cada una de las siguientes tareas permite abrir el panel [Consola][DevtoolsConsoleIndex] para ver los mensajes registrados o ejecutar JavaScript.  

*   Siga estos pasos para abrir el [panel Consola.][DevtoolsConsoleIndex]  
    
    1.  [Abra DevTools](#open-microsoft-edge-devtools).  
    1.  Elija el [panel Consola.][DevtoolsConsoleIndex]  

*   Para ir directamente al panel [consola,][DevtoolsConsoleIndex] seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).  Para obtener más información, vaya [a Microsoft Edge métodos abreviados de teclado de DevTools][DevtoolsShortcutsIndex].  

<!--Navigate to [Get Started With The Console][ConsoleGetStarted].  -->

## <a name="open-the-previous-panel"></a>Abrir el panel anterior  

Para pasar al panel anterior que tenía abierto, seleccione `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\).  Para obtener más información, vaya [a Microsoft Edge métodos abreviados de teclado de DevTools][DevtoolsShortcutsIndex].  

## <a name="open-microsoft-edge-devtools"></a>Abrir Microsoft Edge DevTools  

Para abrir DevTools, use cualquiera de las siguientes opciones.  

*   Usa la interfaz Microsoft Edge usuario.  
    
    1.  Elija el **Configuración y más** \( `...` \) icono > Herramientas más **herramientas**  >   **para desarrolladores**.  
    
*   Use el teclado.  
    *   Seleccione `F12` o `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\).  

Para obtener más información, vaya [a Microsoft Edge métodos abreviados de teclado de DevTools][DevtoolsShortcutsIndex].  

:::image type="complex" source="../media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Abra DevTools desde el Microsoft Edge menú principal" lightbox="../media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Abra DevTools desde el Microsoft Edge menú principal  
:::image-end:::  

## <a name="auto-open-devtools-on-every-new-tab"></a>Abrir automáticamente DevTools en cada pestaña nueva  

Para abrir automáticamente DevTools en cada pestaña nueva, abra Microsoft Edge desde la línea de comandos y pase la `--auto-open-devtools-for-tabs` marca.  

### [<a name="cmd-windows"></a>CMD (Windows)](#tab/cmd-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

### [<a name="powershell-windows"></a>PowerShell (Windows)](#tab/powershell-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

### [<a name="bash-macos"></a>bash (macOS)](#tab/bash-macos/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

### [<a name="bash-linux"></a>bash (Linux)](#tab/bash-linux/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
microsoft-edge-dev --auto-open-devtools-for-tabs
```  

* * *  

## <a name="toggle-the-f12-keyboard-shortcut-on-or-off"></a>Activar o desactivar el método abreviado de teclado F12  

Para cambiar la configuración `F12` de método abreviado de teclado que abre DevTools, realice las siguientes acciones.  

1.  Elija el icono Configuración **y más** \( `...` \) icono > **Configuración**.  
1.  En **Configuración de búsqueda,** escriba `Developer Tools` .  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-on.msft.png" alt-text="La opción Abrir las DevTools cuando se presiona la tecla F12" lightbox="../media/settings-developer-tools-f12-on.msft.png":::
       La **opción Abrir las DevTools cuando se presiona** la tecla F12  
    :::image-end:::  
    
1.  Elija **Abrir las DevTools cuando se** presione la tecla F12 para alternar la configuración a off \(or on\).  Alterna la configuración a desactivado para impedir que el método abreviado de `F12` teclado abra DevTools.  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-off.msft.png" alt-text="La opción Abrir las DevTools cuando se presiona la tecla F12 está desactivada" lightbox="../media/settings-developer-tools-f12-off.msft.png":::
       La **opción Abrir las DevTools cuando se presiona** la tecla F12 está desactivada  
    :::image-end:::  
    
1.  Después de establecer el botón de alternancia en desactivado, seleccione `F12` para confirmar que DevTools ya no está abierto.  
    
    > [!NOTE]
    > Después de desactivar la opción Abrir las DevTools cuando se presiona la tecla **F12,** para abrir DevTools, complete una de las siguientes acciones.  
    > 
    > *   Seleccione `Ctrl` + `Shift` + `I` .  
    > *   Abra el menú contextual \(clic con el botón derecho\) > **Inspeccionar**.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Descripción general de la consola | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Microsoft Edge Métodos abreviados de teclado de DevTools | Microsoft Docs"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/open) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

---
description: Todas las formas en que se abre el Microsoft Edge DevTools.
title: Abrir Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a6e83d0651c5611b53735447f6ddc34c90550db1
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643444"
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

Hay muchas maneras de abrir Microsoft Edge DevTools, lo que te ayuda a acceder rápidamente a diferentes partes de la interfaz de usuario de DevTools. 

## <a name="open-microsoft-edge-devtools"></a>Abrir Microsoft Edge DevTools  

Para abrir DevTools, use cualquiera de las siguientes opciones.  

*   Usa la interfaz Microsoft Edge usuario.
    *  Elija el **Configuración y más** \( `...` \) icono > Herramientas más **herramientas**  >   **para desarrolladores**.  
    
*   Use el teclado.  
    *   Seleccione `F12` o `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\).  

Para obtener más información, vaya [a Microsoft Edge métodos abreviados de teclado de DevTools][DevtoolsShortcutsIndex].  

:::image type="complex" source="../media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Abra DevTools desde el Microsoft Edge menú principal" lightbox="../media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Abra DevTools desde el Microsoft Edge menú principal  
:::image-end:::  

## <a name="open-the-elements-panel-to-inspect-the-dom-or-css"></a>Abra el panel Elementos para inspeccionar el DOM o CSS  

Cualquiera de las siguientes tareas permite inspeccionar los estilos o atributos de un nodo [del](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) modelo de objetos de documento \(DOM\).

*   Mantenga el mouse sobre el elemento, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.  
*   Seleccione `Control` + `Shift` + `C` \(Windows, Linux\) o `Command` + `Option` + `C` \(macOS\). Para obtener más información, vaya [a Microsoft Edge métodos abreviados de teclado de DevTools][DevtoolsShortcutsIndex].  

<!-- :::image type="complex" source="../media/bing-right-click-inspect.msft.png" alt-text="The Inspect option" lightbox="../media/bing-right-click-inspect.msft.png":::
   The **Inspect** option  
:::image-end:::  --> 

<!--Navigate to [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## <a name="open-the-console-panel"></a>Abrir el panel Consola  

Para abrir el panel [Consola][DevtoolsConsoleIndex] para ver mensajes registrados o ejecutar JavaScript, seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\). Para obtener más información, vaya [a Microsoft Edge métodos abreviados de teclado de DevTools][DevtoolsShortcutsIndex].  

<!--Navigate to [Get Started With The Console][ConsoleGetStarted].  -->

## <a name="open-the-previous-panel"></a>Abrir el panel anterior  

Para ir al panel abierto anteriormente, seleccione `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\).  Para obtener más información, vaya [a Microsoft Edge métodos abreviados de teclado de DevTools][DevtoolsShortcutsIndex].  

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

Para cambiar la configuración `F12` de método abreviado de teclado que abre DevTools, realice las siguientes acciones:  

1.  Vaya a `edge://settings/system`.  
1.  In `Developer Tools` , choose Open the **DevTools when the F12 key is pressed** to toggle the setting to off or on. Alterna la configuración a desactivado para impedir que el método abreviado de `F12` teclado abra DevTools.  
1.  Después de establecer la alternancia en desactivado, compruebe que `F12` ya no abra DevTools.  
    
    > [!NOTE]
    > Después de desactivar **Abrir Las DevTools**cuando se presiona la tecla F12 , realice una de las siguientes acciones para abrir DevTools.  
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

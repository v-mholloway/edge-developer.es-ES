---
title: Abrir Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 48f80ea9f85bd3509f2ba3d834f99c25247c0761
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601890"
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

Cuando desee inspeccionar los estilos o los atributos de un nodo DOM, haga clic con el botón derecho en el elemento y seleccione **inspeccionar**.  

> ##### Figura 1  
> La opción **inspeccionar**  
> ![La opción inspeccionar][ImageInspectOption]  

O pulse `Control` + `Shift` + `C` \ (Windows \) o `Command` + `Option` + `C` \ (MacOS \).  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Abrir el panel de consola para ver mensajes registrados o ejecutar JavaScript   

Pulsa `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \) para ir directamente al panel de la **consola** .  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Abrir el último panel que tenía abierto   

Pulse `Control` + `Shift` + `I` \ (Windows \) o `Command` + `Option` + `I` \ (MacOS \).  

## Abrir DevTools desde el menú principal de Microsoft Edge  

Haga clic en **configuración y más (Alt + F \)** `...` y, a continuación, seleccione **más**herramientas  >  **herramientas para desarrolladores**.  

> ##### Figura 2  
> Abrir DevTools desde el menú principal de Microsoft Edge  
> ![Abrir DevTools desde el menú principal de Microsoft Edge][ImageOpenFromMain]  

## DevTools de apertura automática en todas las pestañas nuevas   

Abra Microsoft Edge desde la línea de comandos y pase la `--auto-open-devtools-for-tabs` bandera.  

Windows \ (CMD \):  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

Windows \ (PowerShell \):  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

MacOS  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

 



<!-- image links -->  

[ImagesMainIcon]: /microsoft-edge/devtools-guide-chromium/media/main-menu-icon.msft.png  

[ImageInspectOption]: /microsoft-edge/devtools-guide-chromium/media/bing-right-click-inspect.msft.png "Ilustración 1: la opción inspeccionar"  
[ImageOpenFromMain]: /microsoft-edge/devtools-guide-chromium/media/bing-customize-more-tools-developer-tools-transparent.msft.png "Ilustración 2: abrir DevTools desde el menú principal de Microsoft Edge"  

<!-- links -->  

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

---
title: Simular la orientación del dispositivo con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 9e8115819fa6c3209a6c82940e033113783ece0c
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607319"
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





# Simular la orientación del dispositivo con Microsoft Edge DevTools   



Para simular distintas orientaciones del dispositivo en Microsoft Edge DevTools:  

<!--todo: update device orientation section when available -->  

1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.  
    
    > ##### Figura 1  
    > El menú de comandos  
    > ![El menú de comandos][ImageCommandMenu]  
    
1.  Escriba `sensors` , seleccione **Mostrar sensores**y, a continuación, pulse `Enter` .  La ficha **sensores** se abre en la parte inferior de la ventana de DevTools.  
1.  En la lista **orientación** , seleccione una de las orientaciones preestablecidas, como `Portrait upside down` , o seleccione **orientación personalizada** para proporcionar su propia orientación exacta.  
    
    > ##### Figura 2  
    > Selección `Portrait upside down` de la lista de **orientación**  
    > ![Selección de vertical al revés en la lista de orientación][ImageOrientationPortraitUpsideDown]  
    
    Después de seleccionar la **orientación personalizada**, `alpha` `beta` `gamma` se habilitan los campos, y.  
    <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how these axes work.  -->  
    <!--todo: update links to alpha, beta, and gamma section when available -->  
    También puede establecer una orientación personalizada arrastrando el **modelo de orientación**.  Espera `Shift` antes de arrastrar para girar a lo largo del `alpha` eje.  
    
    > ##### Imagen 3  
    > El **modelo de orientación**  
    > ![El modelo de orientación][ImageOrientationModel]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Ilustración 1: el menú de comandos"  
[ImageOrientationPortraitUpsideDown]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png "Ilustración 2: selección vertical vertical de la lista de orientación"  
[ImageOrientationModel]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-orientation-custom.msft.png "Ilustración 3: el modelo de orientación"  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation \& Motion"  -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

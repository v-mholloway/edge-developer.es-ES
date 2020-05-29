---
title: Invalidar geolocalización con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 307064bedf992e528b6d79eed3a2ade3367830d4
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607443"
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





# Invalidar geolocalización con Microsoft Edge DevTools   



Muchos sitios web aprovechan la ubicación del usuario para proporcionar una experiencia más relevante a los usuarios.  Por ejemplo, un sitio web de Meteorología puede mostrar la previsión local en el área de un usuario, después de que el usuario haya concedido permiso al sitio web para acceder a la ubicación del usuario actual.  

<!--todo: add link to user location section when available -->  

Si estás creando una interfaz de usuario que varía según el lugar donde se encuentre el usuario, probablemente quieras asegurarte de que el sitio se comparará correctamente en diferentes lugares de todo el mundo.  Para invalidar su ubicación geográfica en Microsoft Edge DevTools:  

1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.  
    
    > ##### Figura 1  
    > El menú de comandos  
    > ![El menú de comandos][ImageCommandMenu]  
    
1.  Escriba `sensors` , seleccione **Mostrar sensores**y, a continuación, pulse `Enter` .  La ficha **sensores** se abre en la parte inferior de la ventana de DevTools.  
1.  En la lista **geolocation** , seleccione una de las ciudades preconfiguradas, `Tokyo` o seleccione **ubicación personalizada** para especificar las coordenadas de longitud y latitud personalizadas, o seleccione **ubicación no disponible** para ver cómo se comporta su sitio cuando la ubicación del usuario no está disponible.  
    
    > ##### Figura 2  
    > Selección `Tokyo` de la lista de **ubicación geográfica**  
    > ![Selección de Tokyo desde la lista de geolocalización][ImageGeolocationTokyo]  
    
<!--## Feedback   

  -->  

<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Ilustración 1: el menú de comandos"  
[ImageGeolocationTokyo]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-geolocation-tokyo.msft.png "Ilustración 2: selección de Tokio de la lista de ubicación geográfica"  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

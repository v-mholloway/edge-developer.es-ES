---
description: Abra la herramienta Sensores y seleccione coordenadas en la lista Ubicación geográfica.
title: Invalidar la geolocalización con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 8f6ad09b2f8db110f6743aae32e16cc9b1185400
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399004"
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

# <a name="override-geolocation-with-microsoft-edge-devtools"></a>Invalidar la geolocalización con Microsoft Edge DevTools  

Muchos sitios web aprovechan la ubicación del usuario para proporcionar una experiencia más relevante para los usuarios.  Por ejemplo, un sitio web meteorológico puede mostrar la previsión local en el área de un usuario, después de que el usuario haya concedido al sitio web permiso para tener acceso a la ubicación del usuario actual.  

<!--todo: add link to user location section when available -->  

Si vas a crear una interfaz de usuario que cambie en función de dónde se encuentra el usuario, probablemente quieras asegurarte de que el sitio se comporta correctamente en diferentes lugares del mundo.  Para invalidar la geolocalización en Microsoft Edge DevTools, realice las siguientes acciones.  

1.  Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir el **menú de comandos**.  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menú comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       Menú **comando**  
    :::image-end:::  
    
1.  Escriba `sensors` , elija Mostrar **sensores**y seleccione `Enter` .  La **herramienta** Sensores se abre en la parte inferior de la ventana DevTools.  
1.  En la lista **Ubicación** geográfica, seleccione una de las ciudades preestablecidas, como , o elija Ubicación personalizada para especificar coordenadas de longitud y latitud personalizadas, o elija Ubicación no disponible para mostrar cómo se comporta el sitio cuando la ubicación del usuario no está `Tokyo` disponible. **** ****  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Elegir Tokio en la lista De ubicación geográfica" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       Elegir `Tokyo` en la lista **Ubicación** geográfica  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

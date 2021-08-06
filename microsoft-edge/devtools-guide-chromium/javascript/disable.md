---
description: Abra el menú comando y ejecute el comando "Deshabilitar JavaScript".
title: Deshabilitar JavaScript con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: d3fdbec237e6e29b4ba489a728d378cfff1cc23d28ac4f8cd046fdc873a1b0aa
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11800472"
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
# <a name="disable-javascript-with-microsoft-edge-devtools"></a>Deshabilitar JavaScript con Microsoft Edge DevTools  

Para revisar cómo se representa la página web cuando un explorador no tiene compatibilidad con JavaScript, desactive temporalmente JavaScript.

Complete las siguientes acciones para examinar cómo se muestra y se comporta una página web al desactivar JavaScript.  

1.  [Abra Microsoft Edge DevTools][DevToolsOpen].  
1.  Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para **** abrir el menú de comandos .  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Menú comando" lightbox="../media/javascript-console-command.msft.png":::
       Menú **comando**  
    :::image-end:::  
    
1.  Empiece a `javascript` escribir , elija Deshabilitar **JavaScript**y, a continuación, `Enter` seleccione para ejecutar el comando.  JavaScript ahora está deshabilitado.  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Elija Deshabilitar JavaScript en el menú comando" lightbox="../media/javascript-console-command-javascript.msft.png":::
       Elija **Deshabilitar JavaScript en** el menú **comando**  
    :::image-end:::  
    
    El icono de advertencia amarillo junto **a Orígenes** le recuerda que JavaScript está deshabilitado.  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="El icono de advertencia junto a Orígenes" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       El icono de advertencia junto a **Orígenes**  
    :::image-end:::  
    
JavaScript permanece deshabilitado en la pestaña durante el tiempo que tenga DevTools abierto.  

Es posible que desee actualizar la página para revisar si y cómo la página web depende de JavaScript durante la carga.  

Para volver a habilitar JavaScript, realice las siguientes acciones.  

*   Abra de **nuevo el menú comando** y ejecute el `Enable JavaScript` comando.  
*   Cierre DevTools.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Abrir Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

---
title: Deshabilitar JavaScript con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 829902ddd76800bb8d36268cb07a61361aa1a159
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986118"
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

# Deshabilitar JavaScript con Microsoft Edge DevTools  

Complete las acciones siguientes para ver el aspecto y el comportamiento de una página web cuando JavaScript está deshabilitado.  

1.  [Abre Microsoft Edge DevTools][DevToolsOpen].  
1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="El menú de comandos" lightbox="../media/javascript-console-command.msft.png":::
       El **menú de comandos**  
    :::image-end:::  
    
1.  Comience `javascript` a escribir, seleccione **deshabilitar JavaScript**y, a continuación, presione `Enter` para ejecutar el comando.  Ahora JavaScript está deshabilitado.  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Seleccione deshabilitar JavaScript en el menú de comandos" lightbox="../media/javascript-console-command-javascript.msft.png":::
       Seleccione **deshabilitar JavaScript** en el **menú de comandos**  
    :::image-end:::  
    
    El icono amarillo que aparece junto a los **orígenes** recuerda que JavaScript está deshabilitado.  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Icono de advertencia junto a orígenes" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       Icono de advertencia junto a **orígenes**  
    :::image-end:::  
    
JavaScript permanece desactivado en la pestaña mientras haya DevTools abierto.  

Es posible que desee volver a cargar la página para ver si la página depende de JavaScript mientras se carga.  

Para volver a Habilitar JavaScript, complete las siguientes acciones.  

*   Vuelva a abrir el **menú de comandos** y ejecute el `Enable JavaScript` comando.  
*   Cierre DevTools.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

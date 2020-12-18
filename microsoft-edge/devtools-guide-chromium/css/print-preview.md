---
description: Abre la pestaña "Fotorrealismo" y selecciona "emular los medios CSS" > "Imprimir".
title: Forzar que Microsoft Edge DevTools al modo de vista previa de impresión (tipo de archivo CSS de impresión)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a036e710de998f03e876126581956929d8652f1e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230925"
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

# Forzar que Microsoft Edge DevTools al modo de vista previa de impresión (tipo de archivo CSS de impresión)  

La [consulta multimedia de impresión][MDNUsingMediaQueries] controla el aspecto que tendrá la página impresa.  Para forzar la página al modo de vista previa de impresión:  

1.  Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       El **menú de comandos**  
    :::image-end:::  
    
1.  Escriba `rendering` , elija **Mostrar procesamiento**y, a continuación, seleccione `Enter` .  
1.  En **emular medios CSS**, seleccione **Imprimir**.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Modo de vista previa de impresión" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       Modo de vista previa de impresión  
    :::image-end:::  
    
Desde aquí, puede ver y cambiar su CSS, como cualquier otra página web.  Vaya a [Introducción a la visualización y el cambio de CSS][DevToolsCSSGetStarted].  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevToolsCSSGetStarted]: ./index.md "Introducción a la visualización y el cambio de CSS | Microsoft docs"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usar consultas multimedia | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

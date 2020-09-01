---
title: Marcar scripts de contenido como código de biblioteca
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 410a74b906e3b1ff7ff98b6d1791e057e4fa89c4
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982809"
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





# Marcar las secuencias de comandos de contenido como código de biblioteca   



Al usar el panel **orígenes** de la DevTools de Microsoft Edge para [recorrer el código][DevToolsJavascriptStepThroughCode], a veces deténgase en el código que no reconoce.  Probablemente hayas pausado el código para una de las extensiones de Microsoft Edge que instalaste.  Complete los pasos siguientes para no hacer una pausa en el código de extensión.  

1.  Abra DevTools, seleccione **personalizar y control DevTools** \ ( `...` \) y haga clic en **configuración**.  También puede abrir la **configuración** pulsando `F1` .  

1.  Seleccione la pestaña **código de biblioteca** que abre la sección código de la biblioteca de **Marcos** de **configuración**.  
1.  Active la casilla **marcar scripts de contenido como código de biblioteca** .  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Active la casilla marcar scripts de contenido como código de biblioteca" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       Active la casilla **marcar scripts de contenido como código de biblioteca**  
    :::image-end:::  
    
<!--  
## Feedback   


-->  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Paso 4: desplazarse por el código: Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) y está creada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

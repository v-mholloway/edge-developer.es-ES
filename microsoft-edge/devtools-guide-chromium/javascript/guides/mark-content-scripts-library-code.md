---
description: Habilite "Marcar scripts de contenido como código de biblioteca" en Configuración > código de biblioteca de Framework.
title: Marcar scripts de contenido como código de biblioteca
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ffc27cdd04ce28df888507fb2e1dc460d5bb4f21
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398955"
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

# <a name="mark-content-scripts-as-library-code"></a>Marcar scripts de contenido como código de biblioteca  

Al usar el panel **Orígenes** de Microsoft Edge DevTools para pasar por el [código,][DevToolsJavascriptStepThroughCode]a veces se pausa en el código que no reconoce.  Probablemente haya pausado el código para una de las extensiones de Microsoft Edge que instaló.  Siga estos pasos para no pausar el código de extensión.  

1.  Abra DevTools, elija **Personalizar y controlar DevTools** \( `...` \) > **Configuración**.  También puede abrir **Configuración** seleccionando `F1` .  

1.  Elija el panel **Código de biblioteca** que abre la sección Código de **biblioteca** marco de **Configuración**.  
1.  Active la casilla **Marcar scripts de contenido como código de biblioteca.**  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Habilitar la casilla Marcar scripts de contenido como código de biblioteca" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       Habilitar la casilla **Marcar scripts de contenido como código de biblioteca**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Paso 4: Paso a paso por el código: introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

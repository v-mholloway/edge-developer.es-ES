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





# <span data-ttu-id="5a249-103">Marcar las secuencias de comandos de contenido como código de biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a249-103">Mark content scripts as Library code</span></span>   



<span data-ttu-id="5a249-104">Al usar el panel **orígenes** de la DevTools de Microsoft Edge para [recorrer el código][DevToolsJavascriptStepThroughCode], a veces deténgase en el código que no reconoce.</span><span class="sxs-lookup"><span data-stu-id="5a249-104">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="5a249-105">Probablemente hayas pausado el código para una de las extensiones de Microsoft Edge que instalaste.</span><span class="sxs-lookup"><span data-stu-id="5a249-105">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="5a249-106">Complete los pasos siguientes para no hacer una pausa en el código de extensión.</span><span class="sxs-lookup"><span data-stu-id="5a249-106">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="5a249-107">Abra DevTools, seleccione **personalizar y control DevTools** \ ( `...` \) y haga clic en **configuración**.</span><span class="sxs-lookup"><span data-stu-id="5a249-107">Open DevTools, select **Customize and control DevTools** \(`...`\) and click **Settings**.</span></span>  <span data-ttu-id="5a249-108">También puede abrir la **configuración** pulsando `F1` .</span><span class="sxs-lookup"><span data-stu-id="5a249-108">You may also open **Settings** by pressing `F1`.</span></span>  

1.  <span data-ttu-id="5a249-109">Seleccione la pestaña **código de biblioteca** que abre la sección código de la biblioteca de **Marcos** de **configuración**.</span><span class="sxs-lookup"><span data-stu-id="5a249-109">Select the **Library code** tab which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="5a249-110">Active la casilla **marcar scripts de contenido como código de biblioteca** .</span><span class="sxs-lookup"><span data-stu-id="5a249-110">Enable the **Mark content scripts as Library code** checkbox.</span></span>  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Active la casilla marcar scripts de contenido como código de biblioteca" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       <span data-ttu-id="5a249-112">Active la casilla **marcar scripts de contenido como código de biblioteca**</span><span class="sxs-lookup"><span data-stu-id="5a249-112">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    :::image-end:::  
    
<!--  
## Feedback   


-->  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Paso 4: desplazarse por el código: Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="5a249-114">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5a249-114">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5a249-115">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) y está creada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5a249-115">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5a249-117">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5a249-117">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

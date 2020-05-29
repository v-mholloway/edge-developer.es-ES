---
title: Marcar las secuencias de comandos de contenido como código de biblioteca
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fe34d8f2fb656283b1821441162b93d47d51d24e
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581792"
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





# <span data-ttu-id="44d2e-103">Marcar las secuencias de comandos de contenido como código de biblioteca</span><span class="sxs-lookup"><span data-stu-id="44d2e-103">Mark Content Scripts as Library Code</span></span>   



<span data-ttu-id="44d2e-104">Al usar el panel **orígenes** de la DevTools de Microsoft Edge para [recorrer el código][DevToolsJavascriptStepThroughCode], a veces deténgase en el código que no reconoce.</span><span class="sxs-lookup"><span data-stu-id="44d2e-104">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="44d2e-105">Probablemente hayas pausado el código para una de las extensiones de Microsoft Edge que instalaste.</span><span class="sxs-lookup"><span data-stu-id="44d2e-105">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="44d2e-106">Complete los pasos siguientes para no hacer una pausa en el código de extensión.</span><span class="sxs-lookup"><span data-stu-id="44d2e-106">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="44d2e-107">Abra DevTools, seleccione **personalizar y controle DevTools** `...` y haga clic en **configuración**.</span><span class="sxs-lookup"><span data-stu-id="44d2e-107">Open DevTools, select **Customize and control DevTools** `...` and click **Settings**.</span></span>  <span data-ttu-id="44d2e-108">También puede abrir la **configuración** pulsando `F1` .</span><span class="sxs-lookup"><span data-stu-id="44d2e-108">You may also open **Settings** by pressing `F1`.</span></span>  

1.  <span data-ttu-id="44d2e-109">Seleccione la pestaña **código de biblioteca** que abre la sección código de la biblioteca de **Marcos** de **configuración**.</span><span class="sxs-lookup"><span data-stu-id="44d2e-109">Select the **Library code** tab which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="44d2e-110">Active la casilla **marcar scripts de contenido como código de biblioteca** .</span><span class="sxs-lookup"><span data-stu-id="44d2e-110">Enable the **Mark content scripts as Library code** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="44d2e-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="44d2e-111">Figure 1</span></span>  
    > <span data-ttu-id="44d2e-112">Active la casilla **marcar scripts de contenido como código de biblioteca**</span><span class="sxs-lookup"><span data-stu-id="44d2e-112">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    > ![Active la casilla marcar scripts de contenido como código de biblioteca][ImageMarkContentScriptsLibraryCode]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMarkContentScriptsLibraryCode]: /microsoft-edge/devtools-guide-chromium/media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png "Ilustración 1: Active la casilla marcar scripts de contenido como código de biblioteca"  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Paso 4: desplazarse por el código: Introducción a la depuración de JavaScript en Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="44d2e-116">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="44d2e-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="44d2e-117">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) y está creada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="44d2e-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="44d2e-119">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="44d2e-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

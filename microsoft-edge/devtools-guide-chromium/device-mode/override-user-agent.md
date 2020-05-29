---
title: Invalidar la cadena de agente de usuario de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 376e1550d0dc31f3b47b6badd6970076a8c13f91
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607310"
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





# <span data-ttu-id="8f0e4-103">Invalidar la cadena de agente de usuario de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8f0e4-103">Override The User Agent String From Microsoft Edge DevTools</span></span>   



<span data-ttu-id="8f0e4-104">Para invalidar la cadena de [agente de usuario][MDNUserAgent] de Microsoft Edge DevTools:</span><span class="sxs-lookup"><span data-stu-id="8f0e4-104">To override the [user agent][MDNUserAgent] string from Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="8f0e4-105">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="8f0e4-105">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="8f0e4-106">Figura 1</span><span class="sxs-lookup"><span data-stu-id="8f0e4-106">Figure 1</span></span>  
    > <span data-ttu-id="8f0e4-107">El menú de comandos</span><span class="sxs-lookup"><span data-stu-id="8f0e4-107">The Command Menu</span></span>  
    > ![El menú de comandos][ImageCommandMenu]  
    
1.  <span data-ttu-id="8f0e4-109">Escriba `network conditions` , seleccione **Mostrar condiciones de red**y presione `Enter` para abrir la pestaña **condiciones de red** .</span><span class="sxs-lookup"><span data-stu-id="8f0e4-109">Type `network conditions`, select **Show Network conditions**, and press `Enter` to open the **Network conditions** tab.</span></span>  
1.  <span data-ttu-id="8f0e4-110">En la sección **agente de usuario** , deshabilite la casilla **seleccionar automáticamente** .</span><span class="sxs-lookup"><span data-stu-id="8f0e4-110">In the **User agent** section, disable the **Select automatically** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="8f0e4-111">Figura 2</span><span class="sxs-lookup"><span data-stu-id="8f0e4-111">Figure 2</span></span>  
    > <span data-ttu-id="8f0e4-112">Deshabilitar **la selección automática**</span><span class="sxs-lookup"><span data-stu-id="8f0e4-112">Disabling **Select automatically**</span></span>  
    > ![Deshabilitar la selección automática][ImageUserAgentDisableSelectAutomatically]  
    
1.  <span data-ttu-id="8f0e4-114">Seleccione una cadena de agente de usuario de la lista o escriba su propia cadena personalizada.</span><span class="sxs-lookup"><span data-stu-id="8f0e4-114">Select a user agent string from the list, or enter your own custom string.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Ilustración 1: el menú de comandos"  
[ImageUserAgentDisableSelectAutomatically]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png "Ilustración 2: deshabilitar la selección automática"  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuario | MDN"  

> [!NOTE]
> <span data-ttu-id="8f0e4-118">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8f0e4-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8f0e4-119">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="8f0e4-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8f0e4-121">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8f0e4-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

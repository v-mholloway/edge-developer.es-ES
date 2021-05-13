---
description: Abra la herramienta Condiciones de red, deshabilite Seleccionar automáticamente y elija en la lista o escriba una cadena personalizada.
title: Invalidar la cadena de agente de usuario Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 50d831847342c749cd36f203998351d53325a6f8
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564297"
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
# <a name="override-the-user-agent-string-from-microsoft-edge-devtools"></a><span data-ttu-id="bba81-104">Invalidar la cadena de agente de usuario Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bba81-104">Override the user agent string from Microsoft Edge DevTools</span></span>  

<span data-ttu-id="bba81-105">Para invalidar la [cadena de agente][MDNUserAgent] de usuario Microsoft Edge DevTools:</span><span class="sxs-lookup"><span data-stu-id="bba81-105">To override the [user agent][MDNUserAgent] string from Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="bba81-106">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para \*\*\*\* abrir el menú de comandos .</span><span class="sxs-lookup"><span data-stu-id="bba81-106">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menú comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="bba81-108">Menú **comando**</span><span class="sxs-lookup"><span data-stu-id="bba81-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bba81-109">Escriba `network conditions` , elija Mostrar condiciones de **red**y seleccione para abrir la herramienta `Enter` Condiciones **de** red.</span><span class="sxs-lookup"><span data-stu-id="bba81-109">Type `network conditions`, choose **Show Network conditions**, and select `Enter` to open the **Network conditions** tool.</span></span>  
1.  <span data-ttu-id="bba81-110">En la **sección Agente de** usuario, desactive la casilla Seleccionar **automáticamente.**</span><span class="sxs-lookup"><span data-stu-id="bba81-110">In the **User agent** section, turn off the **Select automatically** checkbox.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png" alt-text="Desactivar Seleccionar automáticamente" lightbox="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png":::
       <span data-ttu-id="bba81-112">Desactivar **Seleccionar automáticamente**</span><span class="sxs-lookup"><span data-stu-id="bba81-112">Turn off **Select automatically**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bba81-113">Elija una cadena de agente de usuario de la lista o escriba su propia cadena personalizada.</span><span class="sxs-lookup"><span data-stu-id="bba81-113">Choose a user agent string from the list, or enter your own custom string.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="bba81-114">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bba81-114">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuario | MDN"  

> [!NOTE]
> <span data-ttu-id="bba81-116">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bba81-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bba81-117">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="bba81-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="bba81-119">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bba81-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

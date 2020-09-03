---
description: Abra la pestaña condiciones de red, desactive la opción seleccionar automáticamente y elija de la lista o escriba una cadena personalizada.
title: Invalidar la cadena de agente de usuario de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ecaa1247824e5c3acb07a2c631feab30d25aba8d
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992928"
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

# <span data-ttu-id="72f42-104">Invalidar la cadena de agente de usuario de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="72f42-104">Override the user agent string from Microsoft Edge DevTools</span></span>  

<span data-ttu-id="72f42-105">Para invalidar la cadena de [agente de usuario][MDNUserAgent] de Microsoft Edge DevTools:</span><span class="sxs-lookup"><span data-stu-id="72f42-105">To override the [user agent][MDNUserAgent] string from Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="72f42-106">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="72f42-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="El menú de comandos" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="72f42-108">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="72f42-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="72f42-109">Escriba `network conditions` , seleccione **Mostrar condiciones de red**y presione `Enter` para abrir la pestaña **condiciones de red** .</span><span class="sxs-lookup"><span data-stu-id="72f42-109">Type `network conditions`, select **Show Network conditions**, and press `Enter` to open the **Network conditions** tab.</span></span>  
1.  <span data-ttu-id="72f42-110">En la sección **agente de usuario** , deshabilite la casilla **seleccionar automáticamente** .</span><span class="sxs-lookup"><span data-stu-id="72f42-110">In the **User agent** section, disable the **Select automatically** checkbox.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png" alt-text="Deshabilitar selección automática" lightbox="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png":::
       <span data-ttu-id="72f42-112">Deshabilitar **selección automática**</span><span class="sxs-lookup"><span data-stu-id="72f42-112">Disable **Select automatically**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="72f42-113">Seleccione una cadena de agente de usuario de la lista o escriba su propia cadena personalizada.</span><span class="sxs-lookup"><span data-stu-id="72f42-113">Select a user agent string from the list, or enter your own custom string.</span></span>  

## <span data-ttu-id="72f42-114">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="72f42-114">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuario | MDN"  

> [!NOTE]
> <span data-ttu-id="72f42-116">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="72f42-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="72f42-117">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="72f42-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="72f42-119">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="72f42-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

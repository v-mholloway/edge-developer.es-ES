---
description: Abra el menú comando y ejecute el comando "Deshabilitar JavaScript".
title: Deshabilitar JavaScript con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c9b5605aff5680ff0f44386c4a69e4c9f7c08cc8
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564164"
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
# <a name="disable-javascript-with-microsoft-edge-devtools"></a><span data-ttu-id="3b0e5-104">Deshabilitar JavaScript con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3b0e5-104">Disable JavaScript with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="3b0e5-105">Para revisar cómo se representa la página web cuando un explorador no tiene compatibilidad con JavaScript, desactive temporalmente JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-105">To review how your webpage renders when a browser doesn't have JavaScript support, temporarily turn off JavaScript.</span></span>

<span data-ttu-id="3b0e5-106">Complete las siguientes acciones para examinar cómo se muestra y se comporta una página web al desactivar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-106">Complete the following actions to examine how a webpage displays and behaves when you turn off JavaScript.</span></span>  

1.  <span data-ttu-id="3b0e5-107">[Abra Microsoft Edge DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="3b0e5-107">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="3b0e5-108">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para \*\*\*\* abrir el menú de comandos .</span><span class="sxs-lookup"><span data-stu-id="3b0e5-108">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Menú comando" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="3b0e5-110">Menú **comando**</span><span class="sxs-lookup"><span data-stu-id="3b0e5-110">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b0e5-111">Empiece a `javascript` escribir , elija Deshabilitar **JavaScript**y, a continuación, `Enter` seleccione para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-111">Start typing `javascript`, choose **Disable JavaScript**, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="3b0e5-112">JavaScript ahora está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-112">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Elija Deshabilitar JavaScript en el menú comando" lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="3b0e5-114">Elija **Deshabilitar JavaScript en** el menú **comando**</span><span class="sxs-lookup"><span data-stu-id="3b0e5-114">Choose **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="3b0e5-115">El icono de advertencia amarillo junto **a Orígenes** le recuerda que JavaScript está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-115">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="El icono de advertencia junto a Orígenes" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="3b0e5-117">El icono de advertencia junto a **Orígenes**</span><span class="sxs-lookup"><span data-stu-id="3b0e5-117">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="3b0e5-118">JavaScript permanece deshabilitado en la pestaña durante el tiempo que tenga DevTools abierto.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-118">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="3b0e5-119">Es posible que desee actualizar la página para revisar si y cómo la página web depende de JavaScript durante la carga.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-119">You may want to refresh the page to review if and how the webpage depends on JavaScript while loading.</span></span>  

<span data-ttu-id="3b0e5-120">Para volver a habilitar JavaScript, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-120">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="3b0e5-121">Abra de **nuevo el menú comando** y ejecute el `Enable JavaScript` comando.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-121">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="3b0e5-122">Cierre DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-122">Close DevTools.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="3b0e5-123">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3b0e5-123">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="3b0e5-125">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3b0e5-125">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3b0e5-126">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="3b0e5-126">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3b0e5-128">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3b0e5-128">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

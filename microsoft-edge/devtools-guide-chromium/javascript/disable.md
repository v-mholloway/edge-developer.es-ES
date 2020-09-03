---
description: Abre el menú de comandos y ejecuta el comando "deshabilitar JavaScript".
title: Deshabilitar JavaScript con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: de756e04c91768c49eed50debce97ae91fdaa3bd
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992802"
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

# <span data-ttu-id="8fe43-104">Deshabilitar JavaScript con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8fe43-104">Disable JavaScript With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="8fe43-105">Complete las acciones siguientes para ver el aspecto y el comportamiento de una página web cuando JavaScript está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8fe43-105">Complete the following actions to see how a web page looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="8fe43-106">[Abre Microsoft Edge DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="8fe43-106">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="8fe43-107">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-107">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="El menú de comandos" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="8fe43-109">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="8fe43-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8fe43-110">Comience `javascript` a escribir, seleccione **deshabilitar JavaScript**y, a continuación, presione `Enter` para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="8fe43-110">Start typing `javascript`, select **Disable JavaScript**, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="8fe43-111">Ahora JavaScript está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8fe43-111">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Seleccione deshabilitar JavaScript en el menú de comandos" lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="8fe43-113">Seleccione **deshabilitar JavaScript** en el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="8fe43-113">Select **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="8fe43-114">El icono amarillo que aparece junto a los **orígenes** recuerda que JavaScript está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8fe43-114">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Icono de advertencia junto a orígenes" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="8fe43-116">Icono de advertencia junto a **orígenes**</span><span class="sxs-lookup"><span data-stu-id="8fe43-116">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="8fe43-117">JavaScript permanece desactivado en la pestaña mientras haya DevTools abierto.</span><span class="sxs-lookup"><span data-stu-id="8fe43-117">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="8fe43-118">Es posible que desee volver a cargar la página para ver si la página depende de JavaScript mientras se carga.</span><span class="sxs-lookup"><span data-stu-id="8fe43-118">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="8fe43-119">Para volver a Habilitar JavaScript, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="8fe43-119">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="8fe43-120">Vuelva a abrir el **menú de comandos** y ejecute el `Enable JavaScript` comando.</span><span class="sxs-lookup"><span data-stu-id="8fe43-120">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="8fe43-121">Cierre DevTools.</span><span class="sxs-lookup"><span data-stu-id="8fe43-121">Close DevTools.</span></span>  

## <span data-ttu-id="8fe43-122">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8fe43-122">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="8fe43-124">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8fe43-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8fe43-125">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="8fe43-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8fe43-127">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8fe43-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

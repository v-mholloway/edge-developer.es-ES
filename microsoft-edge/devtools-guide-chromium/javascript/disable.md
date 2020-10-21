---
description: Abre el menú de comandos y ejecuta el comando "deshabilitar JavaScript".
title: Deshabilitar JavaScript con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 4a200e2faa303a12d46fe2daf7ba89226a985b1f
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124722"
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

# <span data-ttu-id="e97db-104">Deshabilitar JavaScript con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e97db-104">Disable JavaScript With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="e97db-105">Complete las acciones siguientes para ver el aspecto y el comportamiento de una página web cuando JavaScript está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="e97db-105">Complete the following actions to see how a web page looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="e97db-106">[Abre Microsoft Edge DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="e97db-106">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="e97db-107">Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="e97db-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="El menú de comandos" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="e97db-109">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="e97db-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e97db-110">Comience `javascript` a escribir, elija **deshabilitar JavaScript**y, a continuación, seleccione `Enter` para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="e97db-110">Start typing `javascript`, choose **Disable JavaScript**, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="e97db-111">Ahora JavaScript está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="e97db-111">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="El menú de comandos" lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="e97db-113">Elija **deshabilitar JavaScript** en el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="e97db-113">Choose **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e97db-114">El icono amarillo que aparece junto a los **orígenes** recuerda que JavaScript está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="e97db-114">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="El menú de comandos" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="e97db-116">Icono de advertencia junto a **orígenes**</span><span class="sxs-lookup"><span data-stu-id="e97db-116">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e97db-117">JavaScript permanece desactivado en la pestaña mientras haya DevTools abierto.</span><span class="sxs-lookup"><span data-stu-id="e97db-117">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="e97db-118">Es posible que desee volver a cargar la página para ver si la página depende de JavaScript mientras se carga.</span><span class="sxs-lookup"><span data-stu-id="e97db-118">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="e97db-119">Para volver a Habilitar JavaScript, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e97db-119">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="e97db-120">Vuelva a abrir el **menú de comandos** y ejecute el `Enable JavaScript` comando.</span><span class="sxs-lookup"><span data-stu-id="e97db-120">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="e97db-121">Cierre DevTools.</span><span class="sxs-lookup"><span data-stu-id="e97db-121">Close DevTools.</span></span>  

## <span data-ttu-id="e97db-122">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e97db-122">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="e97db-124">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e97db-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e97db-125">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e97db-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e97db-127">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e97db-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

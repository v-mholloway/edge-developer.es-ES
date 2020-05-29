---
title: Deshabilitar JavaScript con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f3838b4e8eccf83aaa71be35ff477ec56cbe7455
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581813"
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





# <span data-ttu-id="190d4-103">Deshabilitar JavaScript con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="190d4-103">Disable JavaScript With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="190d4-104">Para ver el aspecto y el comportamiento de una página web cuando JavaScript está deshabilitado:</span><span class="sxs-lookup"><span data-stu-id="190d4-104">To see how a web page looks and behaves when JavaScript is disabled:</span></span>  

1.  <span data-ttu-id="190d4-105">[Abre Microsoft Edge DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="190d4-105">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="190d4-106">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="190d4-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="190d4-107">Figura 1</span><span class="sxs-lookup"><span data-stu-id="190d4-107">Figure 1</span></span>  
    > <span data-ttu-id="190d4-108">El menú de comandos</span><span class="sxs-lookup"><span data-stu-id="190d4-108">The Command Menu</span></span>  
    > ![El menú de comandos][ImageCommandMenu]  
    
1.  <span data-ttu-id="190d4-110">Comience `javascript` a escribir, seleccione **deshabilitar JavaScript**y, a continuación, presione `Enter` para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="190d4-110">Start typing `javascript`, select **Disable JavaScript**, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="190d4-111">Ahora JavaScript está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="190d4-111">JavaScript is now disabled.</span></span>  
    
    > ##### <span data-ttu-id="190d4-112">Figura 2</span><span class="sxs-lookup"><span data-stu-id="190d4-112">Figure 2</span></span>  
    > <span data-ttu-id="190d4-113">Selección de **deshabilitar JavaScript** en el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="190d4-113">Selecting **Disable JavaScript** in the Command Menu</span></span>  
    > ![Selección de deshabilitar JavaScript en el menú de comandos][ImageDisableJS]  
    
    <span data-ttu-id="190d4-115">El icono amarillo que aparece junto a los **orígenes** recuerda que JavaScript está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="190d4-115">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    > ##### <span data-ttu-id="190d4-116">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="190d4-116">Figure 3</span></span>  
    > <span data-ttu-id="190d4-117">Icono de advertencia junto a **orígenes**</span><span class="sxs-lookup"><span data-stu-id="190d4-117">The warning icon next to **Sources**</span></span>  
    > ![Icono de advertencia junto a orígenes][ImageDisableJSWarning]  

<span data-ttu-id="190d4-119">JavaScript permanece deshabilitado en esta pestaña mientras haya DevTools abierto.</span><span class="sxs-lookup"><span data-stu-id="190d4-119">JavaScript remains disabled in this tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="190d4-120">Es posible que desee volver a cargar la página para ver si la página depende de JavaScript mientras se carga.</span><span class="sxs-lookup"><span data-stu-id="190d4-120">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="190d4-121">Para volver a Habilitar JavaScript:</span><span class="sxs-lookup"><span data-stu-id="190d4-121">To re-enable JavaScript:</span></span>  

*   <span data-ttu-id="190d4-122">Vuelva a abrir el **menú de comandos** y ejecute el `Enable JavaScript` comando.</span><span class="sxs-lookup"><span data-stu-id="190d4-122">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="190d4-123">Cierre DevTools.</span><span class="sxs-lookup"><span data-stu-id="190d4-123">Close DevTools.</span></span>  

## <span data-ttu-id="190d4-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="190d4-124">Feedback</span></span>   



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command.msft.png "Ilustración 1: el menú de comandos"  
[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command-javascript.msft.png "Ilustración 2: seleccionar deshabilitar JavaScript en el menú de comandos"  
[ImageDisableJSWarning]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-javascript-disabled-warning.msft.png "Ilustración 3: el icono de advertencia junto a orígenes"  

<!-- links -->  

[DevToolsOpen]: ../open.md "Abrir Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="190d4-129">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="190d4-129">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="190d4-130">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="190d4-130">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="190d4-132">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="190d4-132">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

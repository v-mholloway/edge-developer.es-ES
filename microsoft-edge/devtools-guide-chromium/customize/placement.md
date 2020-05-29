---
title: Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f0be6243d4780e4ed49428ebaf2b6b37d9da323e
ms.sourcegitcommit: 67ce64f810afdb304844bae0f3918d4e9108dcec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/24/2020
ms.locfileid: "10601349"
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





# <span data-ttu-id="584a6-103">Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)</span><span class="sxs-lookup"><span data-stu-id="584a6-103">Change Microsoft Edge DevTools Placement (Undock, Dock To Bottom, Dock To Left)</span></span>   



<span data-ttu-id="584a6-104">De forma predeterminada DevTools se acopla a la derecha de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="584a6-104">By default DevTools is docked to the right of your viewport.</span></span>  <span data-ttu-id="584a6-105">También puede acoplar a la parte inferior, acoplar a la izquierda o desacoplar el DevTools en una ventana independiente.</span><span class="sxs-lookup"><span data-stu-id="584a6-105">You may also dock to bottom, dock to left, or undock the DevTools to a separate window.</span></span>  

> ##### <span data-ttu-id="584a6-106">Figura 1</span><span class="sxs-lookup"><span data-stu-id="584a6-106">Figure 1</span></span>  
> <span data-ttu-id="584a6-107">Acoplar a la izquierda</span><span class="sxs-lookup"><span data-stu-id="584a6-107">Dock To Left</span></span>  
> ![Acoplar a la izquierda][ImageDockLeft]  

> ##### <span data-ttu-id="584a6-109">Figura 2</span><span class="sxs-lookup"><span data-stu-id="584a6-109">Figure 2</span></span>  
> <span data-ttu-id="584a6-110">Acoplar a la parte inferior</span><span class="sxs-lookup"><span data-stu-id="584a6-110">Dock To Bottom</span></span>  
> ![Acoplar a la parte inferior][ImageDockBottom]  

> ##### <span data-ttu-id="584a6-112">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="584a6-112">Figure 3</span></span>  
> <span data-ttu-id="584a6-113">Explorador en una ventana independiente</span><span class="sxs-lookup"><span data-stu-id="584a6-113">Browser in separate window</span></span>  
> ![Explorador en una ventana independiente][ImageUndockBrowser]  

> ##### <span data-ttu-id="584a6-115">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="584a6-115">Figure 4</span></span>  
> <span data-ttu-id="584a6-116">DevTools desacoplado en una ventana independiente</span><span class="sxs-lookup"><span data-stu-id="584a6-116">Undocked DevTools in separate window</span></span>  
> ![DevTools desacoplado en una ventana independiente][ImageUndockDevTools]  

## <span data-ttu-id="584a6-118">Cambiar la ubicación desde el menú principal</span><span class="sxs-lookup"><span data-stu-id="584a6-118">Change placement from the main menu</span></span>   

1.  <span data-ttu-id="584a6-119">Haga clic en **personalizar y controlar DevTools** `...` y seleccione **desacoplar en** ![ desacoplar ventana separada ][ImageUndockIcon] , **acoplar** a acoplar en la parte inferior ![ ][ImageBottomIcon] o en **acoplar a** la izquierda ![ acoplar a la izquierda ][ImageLeftIcon] .</span><span class="sxs-lookup"><span data-stu-id="584a6-119">Click **Customize And Control DevTools** `...` and select **Undock Into Separate Window** ![Undock][ImageUndockIcon], **Dock To Bottom** ![Dock To Bottom][ImageBottomIcon], or **Dock To Left** ![Dock To Left][ImageLeftIcon].</span></span>  
    
    > ##### <span data-ttu-id="584a6-120">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="584a6-120">Figure 5</span></span>  
    > <span data-ttu-id="584a6-121">Seleccionar **desacoplar en una ventana independiente**</span><span class="sxs-lookup"><span data-stu-id="584a6-121">Selecting **Undock Into Separate Window**</span></span>  
    > ![Seleccionar desacoplar en una ventana independiente][ImageUndockSettings]  
    
## <span data-ttu-id="584a6-123">Cambiar la ubicación desde el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="584a6-123">Change placement from the Command Menu</span></span>   

1.  <span data-ttu-id="584a6-124">[Abrir el menú de comandos][DevtoolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="584a6-124">[Open the Command Menu][DevtoolsCommandMenu].</span></span>  
1.  <span data-ttu-id="584a6-125">Ejecute uno de los siguientes comandos: `Dock To Bottom` , `Undock Into Separate Window` .</span><span class="sxs-lookup"><span data-stu-id="584a6-125">Run one of the following commands: `Dock To Bottom`, `Undock Into Separate Window`.</span></span>  <span data-ttu-id="584a6-126">Por el momento, no hay ningún comando para acoplar a la izquierda, pero puede acceder a él desde el [menú principal](#change-placement-from-the-main-menu).</span><span class="sxs-lookup"><span data-stu-id="584a6-126">Currently there is no command for docking to left, but you may access it from the [main menu](#change-placement-from-the-main-menu).</span></span>  
    
    > ##### <span data-ttu-id="584a6-127">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="584a6-127">Figure 6</span></span>  
    > <span data-ttu-id="584a6-128">El comando desacoplar</span><span class="sxs-lookup"><span data-stu-id="584a6-128">The undock command</span></span>  
    > ![El comando desacoplar][ImageUndockCommand]  

 



<!-- image links -->  

[ImageUndockIcon]: /microsoft-edge/devtools-guide-chromium/media/undock-icon.msft.png  
[ImageBottomIcon]: /microsoft-edge/devtools-guide-chromium/media/bottom-icon.msft.png  
[ImageLeftIcon]: /microsoft-edge/devtools-guide-chromium/media/left-icon.msft.png  

[ImageDockLeft]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-right-docked.msft.png "Ilustración 1: acoplar a la izquierda"  
[ImageDockBottom]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-bottom-docked.msft.png "Ilustración 2: acoplar a la parte inferior"  
[ImageUndockBrowser]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-browser.msft.png "Ilustración 3: explorador en una ventana independiente"  
[ImageUndockDevTools]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png "Ilustración 4: DevTools desacoplado en una ventana independiente"  
[ImageUndockSettings]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight.msft.png "Ilustración 5: seleccionar desacoplar en una ventana independiente"  
[ImageUndockCommand]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-command-menu-undo.msft.png "Ilustración 6: el comando desacoplable"  

<!-- links -->  

[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="584a6-137">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="584a6-137">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="584a6-138">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/customize/placement) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="584a6-138">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/customize/placement) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="584a6-140">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="584a6-140">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

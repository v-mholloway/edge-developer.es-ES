---
title: Simular la orientación del dispositivo con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 9e8115819fa6c3209a6c82940e033113783ece0c
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607319"
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





# <span data-ttu-id="42b42-103">Simular la orientación del dispositivo con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="42b42-103">Simulate Device Orientation With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="42b42-104">Para simular distintas orientaciones del dispositivo en Microsoft Edge DevTools:</span><span class="sxs-lookup"><span data-stu-id="42b42-104">To simulate different device orientations from Microsoft Edge DevTools:</span></span>  

<!--todo: update device orientation section when available -->  

1.  <span data-ttu-id="42b42-105">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="42b42-105">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="42b42-106">Figura 1</span><span class="sxs-lookup"><span data-stu-id="42b42-106">Figure 1</span></span>  
    > <span data-ttu-id="42b42-107">El menú de comandos</span><span class="sxs-lookup"><span data-stu-id="42b42-107">The Command Menu</span></span>  
    > ![El menú de comandos][ImageCommandMenu]  
    
1.  <span data-ttu-id="42b42-109">Escriba `sensors` , seleccione **Mostrar sensores**y, a continuación, pulse `Enter` .</span><span class="sxs-lookup"><span data-stu-id="42b42-109">Type `sensors`, select **Show Sensors**, and press `Enter`.</span></span>  <span data-ttu-id="42b42-110">La ficha **sensores** se abre en la parte inferior de la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="42b42-110">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="42b42-111">En la lista **orientación** , seleccione una de las orientaciones preestablecidas, como `Portrait upside down` , o seleccione **orientación personalizada** para proporcionar su propia orientación exacta.</span><span class="sxs-lookup"><span data-stu-id="42b42-111">From the **Orientation** list, select one of the preset orientations, such as `Portrait upside down`, or select **Custom orientation** to provide your own exact orientation.</span></span>  
    
    > ##### <span data-ttu-id="42b42-112">Figura 2</span><span class="sxs-lookup"><span data-stu-id="42b42-112">Figure 2</span></span>  
    > <span data-ttu-id="42b42-113">Selección `Portrait upside down` de la lista de **orientación**</span><span class="sxs-lookup"><span data-stu-id="42b42-113">Selecting `Portrait upside down` from the **Orientation** list</span></span>  
    > ![Selección de vertical al revés en la lista de orientación][ImageOrientationPortraitUpsideDown]  
    
    <span data-ttu-id="42b42-115">Después de seleccionar la **orientación personalizada**, `alpha` `beta` `gamma` se habilitan los campos, y.</span><span class="sxs-lookup"><span data-stu-id="42b42-115">After selecting **Custom orientation**, the `alpha`, `beta`, and `gamma` fields are enabled.</span></span>  
    <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how these axes work.  -->  
    <!--todo: update links to alpha, beta, and gamma section when available -->  
    <span data-ttu-id="42b42-116">También puede establecer una orientación personalizada arrastrando el **modelo de orientación**.</span><span class="sxs-lookup"><span data-stu-id="42b42-116">You are also able to set a custom orientation by dragging the **Orientation Model**.</span></span>  <span data-ttu-id="42b42-117">Espera `Shift` antes de arrastrar para girar a lo largo del `alpha` eje.</span><span class="sxs-lookup"><span data-stu-id="42b42-117">Hold `Shift` before dragging to rotate along the `alpha` axis.</span></span>  
    
    > ##### <span data-ttu-id="42b42-118">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="42b42-118">Figure 3</span></span>  
    > <span data-ttu-id="42b42-119">El **modelo de orientación**</span><span class="sxs-lookup"><span data-stu-id="42b42-119">The **Orientation Model**</span></span>  
    > ![El modelo de orientación][ImageOrientationModel]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Ilustración 1: el menú de comandos"  
[ImageOrientationPortraitUpsideDown]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png "Ilustración 2: selección vertical vertical de la lista de orientación"  
[ImageOrientationModel]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-orientation-custom.msft.png "Ilustración 3: el modelo de orientación"  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation \& Motion"  -->  

> [!NOTE]
> <span data-ttu-id="42b42-124">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="42b42-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="42b42-125">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="42b42-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="42b42-127">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="42b42-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

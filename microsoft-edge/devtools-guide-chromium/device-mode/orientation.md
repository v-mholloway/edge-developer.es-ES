---
description: Abra la ficha sensores y vaya a la sección orientación.
title: Simular la orientación del dispositivo con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 42b58ef2d4b132eedad2663287894e25e72b2572
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992935"
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

# <span data-ttu-id="1450e-104">Simular la orientación del dispositivo con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1450e-104">Simulate device orientation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="1450e-105">Complete las siguientes acciones para simular distintas orientaciones del dispositivo en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="1450e-105">Complete the following actions to simulate different device orientations from Microsoft Edge DevTools.</span></span>  

<!--todo: update device orientation section when available -->  

1.  <span data-ttu-id="1450e-106">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="1450e-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="El menú de comandos" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="1450e-108">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="1450e-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1450e-109">Escriba `sensors` , seleccione **Mostrar sensores**y, a continuación, pulse `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1450e-109">Type `sensors`, select **Show Sensors**, and press `Enter`.</span></span>  <span data-ttu-id="1450e-110">La ficha **sensores** se abre en la parte inferior de la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="1450e-110">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="1450e-111">En la lista **orientación** , seleccione una de las orientaciones preestablecidas, como `Portrait upside down` , o seleccione **orientación personalizada** para proporcionar su propia orientación exacta.</span><span class="sxs-lookup"><span data-stu-id="1450e-111">From the **Orientation** list, select one of the preset orientations, such as `Portrait upside down`, or select **Custom orientation** to provide your own exact orientation.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png" alt-text="Seleccione vertical hacia abajo en la lista orientación" lightbox="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png":::
             <span data-ttu-id="1450e-113">Seleccione una `Portrait upside down` de la lista de **orientación**</span><span class="sxs-lookup"><span data-stu-id="1450e-113">Select `Portrait upside down` from the **Orientation** list</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="1450e-114">Después de seleccionar la **orientación personalizada**, `alpha` `beta` `gamma` se habilitan los campos, y.</span><span class="sxs-lookup"><span data-stu-id="1450e-114">After you select **Custom orientation**, the `alpha`, `beta`, and `gamma` fields are enabled.</span></span>  
          <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how each axis works.  -->  
          <!--todo: update links to alpha, beta, and gamma section when available -->  
          <span data-ttu-id="1450e-115">También puede establecer una orientación personalizada arrastrando el **modelo de orientación**.</span><span class="sxs-lookup"><span data-stu-id="1450e-115">You are also able to set a custom orientation by dragging the **Orientation Model**.</span></span>  <span data-ttu-id="1450e-116">Espera `Shift` antes de arrastrar para girar a lo largo del `alpha` eje.</span><span class="sxs-lookup"><span data-stu-id="1450e-116">Hold `Shift` before dragging to rotate along the `alpha` axis.</span></span>  
          
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-custom.msft.png" alt-text="El modelo de orientación" lightbox="../media/device-mode-console-sensors-orientation-custom.msft.png":::
             <span data-ttu-id="1450e-118">El **modelo de orientación**</span><span class="sxs-lookup"><span data-stu-id="1450e-118">The **Orientation Model**</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="1450e-119">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1450e-119">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation & Motion"  -->  

> [!NOTE]
> <span data-ttu-id="1450e-120">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1450e-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1450e-121">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="1450e-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1450e-123">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1450e-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
description: Abra la herramienta Sensores y vaya a la sección Orientación.
title: Simular la orientación del dispositivo con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 754df3b271b44f986802c2847862624f6a8b5bd9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398717"
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

# <a name="simulate-device-orientation-with-microsoft-edge-devtools"></a><span data-ttu-id="41047-104">Simular la orientación del dispositivo con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="41047-104">Simulate device orientation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="41047-105">Complete las siguientes acciones para simular diferentes orientaciones de dispositivo desde Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="41047-105">Complete the following actions to simulate different device orientations from Microsoft Edge DevTools.</span></span>  

<!--todo: update device orientation section when available -->  

1.  <span data-ttu-id="41047-106">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="41047-106">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menú comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="41047-108">Menú **comando**</span><span class="sxs-lookup"><span data-stu-id="41047-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="41047-109">Escriba `sensors` , elija Mostrar **sensores**y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="41047-109">Type `sensors`, choose **Show Sensors**, and select `Enter`.</span></span>  <span data-ttu-id="41047-110">La **herramienta** Sensores se abre en la parte inferior de la ventana DevTools.</span><span class="sxs-lookup"><span data-stu-id="41047-110">The **Sensors** tool opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="41047-111">En la **lista Orientación,** seleccione una de las orientaciones preestablecidas, como , o elija Orientación personalizada para proporcionar `Portrait upside down` su propia orientación exacta. </span><span class="sxs-lookup"><span data-stu-id="41047-111">From the **Orientation** list, select one of the preset orientations, such as `Portrait upside down`, or choose **Custom orientation** to provide your own exact orientation.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png" alt-text="Elija Vertical al revés en la lista Orientación" lightbox="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png":::
             <span data-ttu-id="41047-113">Elegir `Portrait upside down` en la lista **Orientación**</span><span class="sxs-lookup"><span data-stu-id="41047-113">Choose `Portrait upside down` from the **Orientation** list</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="41047-114">Después de elegir **Orientación personalizada,** los `alpha` campos , y están `beta` `gamma` habilitados.</span><span class="sxs-lookup"><span data-stu-id="41047-114">After you choose **Custom orientation**, the `alpha`, `beta`, and `gamma` fields are enabled.</span></span>  
          <!--To understand how each axis works, navigate to [Alpha][alpha], [Beta][beta], and [Gamma][gamma].  -->  
          <!--todo: update links to alpha, beta, and gamma section when available -->  
          <span data-ttu-id="41047-115">También puede establecer una orientación personalizada arrastrando el **modelo de orientación**.</span><span class="sxs-lookup"><span data-stu-id="41047-115">You are also able to set a custom orientation by dragging the **Orientation Model**.</span></span>  <span data-ttu-id="41047-116">Mantenga `Shift` presionado antes de arrastrar para girar a lo largo del `alpha` eje.</span><span class="sxs-lookup"><span data-stu-id="41047-116">Hold `Shift` before dragging to rotate along the `alpha` axis.</span></span>  
          
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-custom.msft.png" alt-text="Modelo de orientación" lightbox="../media/device-mode-console-sensors-orientation-custom.msft.png":::
             <span data-ttu-id="41047-118">Modelo **de orientación**</span><span class="sxs-lookup"><span data-stu-id="41047-118">The **Orientation Model**</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="41047-119">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="41047-119">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation & Motion"  -->  

> [!NOTE]
> <span data-ttu-id="41047-120">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="41047-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="41047-121">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="41047-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="41047-123">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="41047-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

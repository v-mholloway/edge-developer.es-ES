---
description: Abra la herramienta Sensores y seleccione coordenadas en la lista Ubicación geográfica.
title: Invalidar la geolocalización con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 5e162d5591dec4013a899a16b0c56fd09d58610f
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564332"
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
# <a name="override-geolocation-with-microsoft-edge-devtools"></a><span data-ttu-id="477c7-104">Invalidar la geolocalización con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="477c7-104">Override geolocation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="477c7-105">Muchos sitios web aprovechan la ubicación del usuario para proporcionar una experiencia más relevante para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="477c7-105">Many websites take advantage of user location in order to provide a more relevant experience for the users.</span></span>  <span data-ttu-id="477c7-106">Por ejemplo, un sitio web meteorológico puede mostrar la previsión local en el área de un usuario, después de que el usuario haya concedido al sitio web permiso para tener acceso a la ubicación del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="477c7-106">For example, a weather website may show the local forecast in a user's area, after the user has granted the website permission to access the current user location.</span></span>  

<!--todo: add link to user location section when available -->  

<span data-ttu-id="477c7-107">Si vas a crear una interfaz de usuario que cambie en función de dónde se encuentra el usuario, probablemente quieras asegurarte de que el sitio se comporta correctamente en diferentes lugares del mundo.</span><span class="sxs-lookup"><span data-stu-id="477c7-107">If you are building a UI that changes depending on where the user is located, you probably want to make sure that the site behaves correctly in different places around the world.</span></span>  <span data-ttu-id="477c7-108">Para invalidar la geolocalización en Microsoft Edge DevTools, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="477c7-108">To override your geolocation in Microsoft Edge DevTools, complete the following actions.</span></span>  

1.  <span data-ttu-id="477c7-109">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para \*\*\*\* abrir el menú de comandos .</span><span class="sxs-lookup"><span data-stu-id="477c7-109">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menú comando" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="477c7-111">Menú **comando**</span><span class="sxs-lookup"><span data-stu-id="477c7-111">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c7-112">Escriba `sensors` , elija Mostrar **sensores**y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="477c7-112">Type `sensors`, choose **Show Sensors**, and select `Enter`.</span></span>  <span data-ttu-id="477c7-113">La **herramienta** Sensores se abre en la parte inferior de la ventana DevTools.</span><span class="sxs-lookup"><span data-stu-id="477c7-113">The **Sensors** tool opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="477c7-114">En la lista **Ubicación** geográfica, seleccione una de las ciudades preestablecidas, como , o elija Ubicación personalizada para especificar coordenadas de longitud y latitud personalizadas, o elija Ubicación no disponible para mostrar cómo se comporta el sitio cuando la ubicación del usuario no está `Tokyo` disponible. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="477c7-114">From the **Geolocation** list select one of the preset cities, like `Tokyo`, or choose **Custom location** to enter custom longitude and latitude coordinates, or choose **Location unavailable** to display how your site behaves when the user's location is not available.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Elegir Tokio en la lista De ubicación geográfica" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       <span data-ttu-id="477c7-116">Elegir `Tokyo` en la lista **Ubicación** geográfica</span><span class="sxs-lookup"><span data-stu-id="477c7-116">Choose `Tokyo` from the **Geolocation** list</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="477c7-117">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="477c7-117">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> <span data-ttu-id="477c7-118">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="477c7-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="477c7-119">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="477c7-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="477c7-121">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="477c7-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

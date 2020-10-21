---
description: Abra la ficha sensores y seleccione coordenadas de la lista ubicación geográfica.
title: Invalidar geolocalización con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f2bc395993ff59d88360a363b2c4bc12b570f1ab
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125016"
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

# <span data-ttu-id="501ff-104">Invalidar geolocalización con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="501ff-104">Override geolocation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="501ff-105">Muchos sitios web aprovechan la ubicación del usuario para proporcionar una experiencia más relevante a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="501ff-105">Many websites take advantage of user location in order to provide a more relevant experience for the users.</span></span>  <span data-ttu-id="501ff-106">Por ejemplo, un sitio web de Meteorología puede mostrar la previsión local en el área de un usuario, después de que el usuario haya concedido permiso al sitio web para acceder a la ubicación del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="501ff-106">For example, a weather website may show the local forecast in a user's area, after the user has granted the website permission to access the current user location.</span></span>  

<!--todo: add link to user location section when available -->  

<span data-ttu-id="501ff-107">Si estás creando una interfaz de usuario que varía según el lugar donde se encuentre el usuario, probablemente quieras asegurarte de que el sitio se comparará correctamente en diferentes lugares de todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="501ff-107">If you are building a UI that changes depending on where the user is located, you probably want to make sure that the site behaves correctly in different places around the world.</span></span>  <span data-ttu-id="501ff-108">Para invalidar su ubicación geográfica en Microsoft Edge DevTools, lleve a cabo las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="501ff-108">To override your geolocation in Microsoft Edge DevTools, complete the following actions.</span></span>  

1.  <span data-ttu-id="501ff-109">Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="501ff-109">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="El menú de comandos" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="501ff-111">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="501ff-111">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="501ff-112">Escriba `sensors` , seleccione **Mostrar sensores**y, a continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="501ff-112">Type `sensors`, choose **Show Sensors**, and select `Enter`.</span></span>  <span data-ttu-id="501ff-113">La ficha **sensores** se abre en la parte inferior de la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="501ff-113">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="501ff-114">En la lista **ubicación geográfica** , seleccione una de las ciudades preestablecidas, `Tokyo` o elija **ubicación personalizada** para especificar las coordenadas de longitud y latitud personalizadas, o elija **ubicación no disponible** para ver cómo se comporta su sitio cuando la ubicación del usuario no está disponible.</span><span class="sxs-lookup"><span data-stu-id="501ff-114">From the **Geolocation** list select one of the preset cities, like `Tokyo`, or choose **Custom location** to enter custom longitude and latitude coordinates, or choose **Location unavailable** to see how your site behaves when the user's location is not available.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="El menú de comandos" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       <span data-ttu-id="501ff-116">Seleccione `Tokyo` de la lista **ubicación geográfica**</span><span class="sxs-lookup"><span data-stu-id="501ff-116">Select `Tokyo` from the **Geolocation** list</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="501ff-117">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="501ff-117">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> <span data-ttu-id="501ff-118">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="501ff-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="501ff-119">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="501ff-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="501ff-121">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="501ff-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

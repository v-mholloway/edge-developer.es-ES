---
description: Abre la pestaña "Fotorrealismo" y selecciona "emular los medios CSS" > "Imprimir".
title: Forzar que Microsoft Edge DevTools al modo de vista previa de impresión (tipo de archivo CSS de impresión)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d4e8e06d60461ac4cdcab8686a18a0698d52f6e3
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125121"
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

# <span data-ttu-id="0a99d-104">Forzar que Microsoft Edge DevTools al modo de vista previa de impresión (tipo de archivo CSS de impresión)</span><span class="sxs-lookup"><span data-stu-id="0a99d-104">Force Microsoft Edge DevTools into Print Preview mode (CSS Print Media Type)</span></span>  

<span data-ttu-id="0a99d-105">La [consulta multimedia de impresión][MDNUsingMediaQueries] controla el aspecto que tendrá la página impresa.</span><span class="sxs-lookup"><span data-stu-id="0a99d-105">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="0a99d-106">Para forzar la página al modo de vista previa de impresión:</span><span class="sxs-lookup"><span data-stu-id="0a99d-106">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="0a99d-107">Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="0a99d-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="0a99d-109">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="0a99d-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0a99d-110">Escriba `rendering` , elija **Mostrar procesamiento**y, a continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="0a99d-110">Type `rendering`, choose **Show Rendering**, and then select `Enter`.</span></span>  
1.  <span data-ttu-id="0a99d-111">En **emular medios CSS** , seleccione **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="0a99d-111">Under **Emulate CSS media** choose **print**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="El menú de comandos" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       <span data-ttu-id="0a99d-113">Modo de vista previa de impresión</span><span class="sxs-lookup"><span data-stu-id="0a99d-113">Print preview mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0a99d-114">Desde aquí, puede ver y cambiar su CSS, como cualquier otra página web.</span><span class="sxs-lookup"><span data-stu-id="0a99d-114">From here, you can view and change your CSS, like any other web page.</span></span>  <span data-ttu-id="0a99d-115">Consulte Introducción [a la visualización y el cambio de CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="0a99d-115">See [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

## <span data-ttu-id="0a99d-116">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0a99d-116">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevToolsCSSGetStarted]: ./index.md "Introducción a la visualización y el cambio de CSS | Microsoft docs"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usar consultas multimedia | MDN"  

> [!NOTE]
> <span data-ttu-id="0a99d-120">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0a99d-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0a99d-121">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="0a99d-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0a99d-123">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0a99d-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

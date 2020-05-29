---
title: Forzar que Microsoft Edge DevTools al modo de vista previa de impresión (tipo de archivo CSS de impresión)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 659120414597273b15657377c33c800e0c83b7cb
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601841"
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





# <span data-ttu-id="b6d6c-103">Forzar que Microsoft Edge DevTools al modo de vista previa de impresión (tipo de archivo CSS de impresión)</span><span class="sxs-lookup"><span data-stu-id="b6d6c-103">Force Microsoft Edge DevTools Into Print Preview Mode (CSS Print Media Type)</span></span>   



<span data-ttu-id="b6d6c-104">La [consulta multimedia de impresión][MDNUsingMediaQueries] controla el aspecto que tendrá la página impresa.</span><span class="sxs-lookup"><span data-stu-id="b6d6c-104">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="b6d6c-105">Para forzar la página al modo de vista previa de impresión:</span><span class="sxs-lookup"><span data-stu-id="b6d6c-105">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="b6d6c-106">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="b6d6c-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="b6d6c-107">Figura 1</span><span class="sxs-lookup"><span data-stu-id="b6d6c-107">Figure 1</span></span>  
    > <span data-ttu-id="b6d6c-108">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="b6d6c-108">The **Command Menu**</span></span>  
    > ![El menú de comandos][ImageCommandMenu]  
    
1.  <span data-ttu-id="b6d6c-110">Escriba `rendering` , seleccione **Mostrar procesamiento**y, a continuación, presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b6d6c-110">Type `rendering`, select **Show Rendering**, and then press `Enter`.</span></span>  
1.  <span data-ttu-id="b6d6c-111">En **emular medios CSS** , seleccione **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="b6d6c-111">Under **Emulate CSS media** select **print**.</span></span>  
    
    > ##### <span data-ttu-id="b6d6c-112">Figura 2</span><span class="sxs-lookup"><span data-stu-id="b6d6c-112">Figure 2</span></span>  
    > <span data-ttu-id="b6d6c-113">Modo de vista previa de impresión</span><span class="sxs-lookup"><span data-stu-id="b6d6c-113">Print preview mode</span></span>  
    > ![Modo de vista previa de impresión][ImagePrintMode]  
    
<span data-ttu-id="b6d6c-115">Desde aquí, puede ver y cambiar su CSS, como cualquier otra página web.</span><span class="sxs-lookup"><span data-stu-id="b6d6c-115">From here, you can view and change your CSS, like any other web page.</span></span>  <span data-ttu-id="b6d6c-116">Consulte Introducción [a la visualización y el cambio de CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="b6d6c-116">See [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

 



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Ilustración 1: el menú de comandos"  
[ImagePrintMode]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png "Ilustración 2: modo de vista previa de impresión"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Introducción a la visualización y el cambio de CSS"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usar consultas multimedia | MDN"  

> [!NOTE]
> <span data-ttu-id="b6d6c-122">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b6d6c-122">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b6d6c-123">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="b6d6c-123">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b6d6c-125">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b6d6c-125">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

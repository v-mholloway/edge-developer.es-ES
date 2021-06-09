---
description: Probar la accesibilidad con Lighthouse desde DevTools.
title: Probar la accesibilidad con Lighthouse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: bb158085eb516c8d4ce37a22f6b612784db51461
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597720"
---
<!-- this article was created on 05/11/2021 by moving a section out from the "Accessibility reference" article (reference.md) -->
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

# <a name="test-accessibility-using-lighthouse"></a><span data-ttu-id="bd206-104">Probar la accesibilidad con Lighthouse</span><span class="sxs-lookup"><span data-stu-id="bd206-104">Test accessibility using Lighthouse</span></span>

<span data-ttu-id="bd206-105">Puede usar Lighthouse desde DevTools para auditar la accesibilidad de una página y generar un informe.</span><span class="sxs-lookup"><span data-stu-id="bd206-105">You can use Lighthouse from within DevTools to audit the accessibility of a page and generate a report.</span></span> <span data-ttu-id="bd206-106">Puede usar la herramienta Faro para determinar:</span><span class="sxs-lookup"><span data-stu-id="bd206-106">You can use the Lighthouse tool to determine:</span></span>

*   <span data-ttu-id="bd206-107">Si una página está correctamente marcada para lectores de pantalla.</span><span class="sxs-lookup"><span data-stu-id="bd206-107">Whether a page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="bd206-108">Si los elementos de texto de una página tienen suficientes relaciones de contraste con el Selector de colores.</span><span class="sxs-lookup"><span data-stu-id="bd206-108">Whether the text elements on a page have sufficient contrast ratios using the Color Picker.</span></span> <span data-ttu-id="bd206-109">Para obtener más información, vaya a Probar contraste [de color de texto con el Selector de colores](color-picker.md).</span><span class="sxs-lookup"><span data-stu-id="bd206-109">For more information, navigate to [Test text-color contrast using the Color Picker](color-picker.md).</span></span>   

> [!NOTE]
> <span data-ttu-id="bd206-110">La **herramienta Lighthouse** proporciona vínculos al contenido hospedado en sitios web de terceros.</span><span class="sxs-lookup"><span data-stu-id="bd206-110">The **Lighthouse** tool provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="bd206-111">Microsoft no es responsable y no tiene control sobre el contenido de estos sitios ni sobre los datos que se puedan recopilar.</span><span class="sxs-lookup"><span data-stu-id="bd206-111">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="bd206-112">Para auditar una página con la herramienta Faro, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="bd206-112">To audit a page using the Lighthouse tool, perform the following steps.</span></span>

1.  <span data-ttu-id="bd206-113">Vaya a la dirección URL que desea auditar.</span><span class="sxs-lookup"><span data-stu-id="bd206-113">Navigate to the URL that you want to audit.</span></span>
1.  <span data-ttu-id="bd206-114">En DevTools, seleccione la **herramienta Faro.**</span><span class="sxs-lookup"><span data-stu-id="bd206-114">In DevTools, select the **Lighthouse** tool.</span></span>  <span data-ttu-id="bd206-115">Se muestran las opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="bd206-115">Configuration options are displayed.</span></span>
    
    :::image type="complex" source="../media/accessibility-lighthouse.msft.png" alt-text="Opciones de configuración de Faro" lightbox="../media/accessibility-lighthouse.msft.png":::
       <span data-ttu-id="bd206-117">Opciones de configuración de Faro</span><span class="sxs-lookup"><span data-stu-id="bd206-117">Lighthouse configuration options</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="bd206-118">Para **Dispositivo**, selecciona **Móvil** si quieres simular un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="bd206-118">For **Device**, select **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="bd206-119">Esta opción cambia la cadena del agente de usuario y cambia el tamaño de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="bd206-119">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="bd206-120">Esta opción puede afectar a los resultados de auditoría.</span><span class="sxs-lookup"><span data-stu-id="bd206-120">This option can affect the audit results.</span></span>
1.  <span data-ttu-id="bd206-121">En la **sección Categorías,** seleccione **Accesibilidad**.</span><span class="sxs-lookup"><span data-stu-id="bd206-121">In the **Categories** section, select **Accessibility**.</span></span>
1.  <span data-ttu-id="bd206-122">Seleccione **Generar informe**.</span><span class="sxs-lookup"><span data-stu-id="bd206-122">Select **Generate report**.</span></span> <span data-ttu-id="bd206-123">Después de 10 a 30 segundos, DevTools muestra un informe.</span><span class="sxs-lookup"><span data-stu-id="bd206-123">After 10 to 30 seconds, DevTools displays a report.</span></span>  <span data-ttu-id="bd206-124">El informe ofrece sugerencias sobre cómo mejorar la accesibilidad de la página.</span><span class="sxs-lookup"><span data-stu-id="bd206-124">The report gives tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result.msft.png" alt-text="Un informe de Faro para la categoría Accesibilidad" lightbox="../media/accessibility-lighthouse-result.msft.png":::
       <span data-ttu-id="bd206-126">Un informe de Faro para la **categoría Accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="bd206-126">A Lighthouse report for the **Accessibility** category</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="bd206-127">Seleccione un elemento en el informe para obtener más información sobre él.</span><span class="sxs-lookup"><span data-stu-id="bd206-127">Select an item in the report to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result-issue-expanded.msft.png" alt-text="Un problema expandido en un informe de Faro" lightbox="../media/accessibility-lighthouse-result-issue-expanded.msft.png":::
       <span data-ttu-id="bd206-129">Un problema expandido en un informe de Faro</span><span class="sxs-lookup"><span data-stu-id="bd206-129">An expanded issue in a Lighthouse report</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="bd206-130">Seleccione el **vínculo Más información** para ver la documentación del problema.</span><span class="sxs-lookup"><span data-stu-id="bd206-130">Select the **Learn more** link to view the documentation of the issue.</span></span>
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Ver la documentación de un problema" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="bd206-132">Ver la documentación de un problema</span><span class="sxs-lookup"><span data-stu-id="bd206-132">View the documentation of an issue</span></span>
    :::image-end:::  

1.  <span data-ttu-id="bd206-133">Para volver a las opciones de configuración, en DevTools, seleccione **Realizar una auditoría** ( `+` ).</span><span class="sxs-lookup"><span data-stu-id="bd206-133">To return to the configuration options, in DevTools, select **Perform an audit** (`+`).</span></span>    


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="bd206-134">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bd206-134">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> <span data-ttu-id="bd206-135">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bd206-135">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bd206-136">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="bd206-136">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="bd206-138">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bd206-138">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- links -->  
[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe - Pruebas de accesibilidad web - Chrome Web Store"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

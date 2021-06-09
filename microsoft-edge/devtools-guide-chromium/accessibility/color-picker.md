---
description: Probar el contraste de color de texto con el Selector de colores.
title: Probar el contraste de color de texto con el Selector de colores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f4ba5f3706460c443ae06a393e5ef63e5d336229
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597722"
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
# <a name="test-text-color-contrast-using-the-color-picker"></a><span data-ttu-id="73f08-104">Probar el contraste de color de texto con el Selector de colores</span><span class="sxs-lookup"><span data-stu-id="73f08-104">Test text-color contrast using the Color Picker</span></span>

<span data-ttu-id="73f08-105">Es posible que las personas con visión baja no vean áreas muy brillantes o muy oscuras.</span><span class="sxs-lookup"><span data-stu-id="73f08-105">People with low vision may not see areas that are very bright or very dark.</span></span>  <span data-ttu-id="73f08-106">Todo tiende a aparecer en el mismo nivel de brillo, lo que hace que sea difícil distinguir contornos y bordes.</span><span class="sxs-lookup"><span data-stu-id="73f08-106">Everything tends to appear at about the same level of brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="73f08-107">La relación de contraste mide la diferencia de brillo entre el primer plano y el fondo del texto.</span><span class="sxs-lookup"><span data-stu-id="73f08-107">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="73f08-108">Si el texto tiene una relación de contraste baja, las personas con visión baja pueden experimentar el sitio como una pantalla en blanco.</span><span class="sxs-lookup"><span data-stu-id="73f08-108">If your text has a low contrast ratio, then people with low vision may experience your site as a blank screen.</span></span>  

<span data-ttu-id="73f08-109">En DevTools, una forma de ver la relación de contraste de un elemento de texto es usar el Selector de colores, desde la **pestaña Estilos.**  El Selector de colores te ayuda a comprobar que el texto cumple los niveles de relación de contraste recomendados.</span><span class="sxs-lookup"><span data-stu-id="73f08-109">In DevTools, one way to view the contrast ratio of a text element is to use the Color Picker, from the **Styles** tab.  The Color Picker helps you verify that your text meets recommended contrast ratio levels.</span></span>

**<span data-ttu-id="73f08-110">Para comprobar el contraste de color de texto con el Selector de colores:</span><span class="sxs-lookup"><span data-stu-id="73f08-110">To check the text-color contrast using the Color Picker:</span></span>**

1.  <span data-ttu-id="73f08-111">En DevTools, seleccione la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="73f08-111">In DevTools, select the **Elements** tool.</span></span>  
1.  <span data-ttu-id="73f08-112">En el **árbol DOM,** seleccione el elemento de texto que desea inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="73f08-112">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspeccionar un párrafo en el árbol DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="73f08-114">Inspeccionar un párrafo en el **árbol DOM**</span><span class="sxs-lookup"><span data-stu-id="73f08-114">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73f08-115">En la **pestaña Estilos,** busque la **propiedad color** que se aplica al elemento y, a continuación, seleccione el cuadrado de color junto a la **propiedad color.**</span><span class="sxs-lookup"><span data-stu-id="73f08-115">On the **Styles** tab, locate the **color** property that's applied to the element, and then select the color square next to the **color** property.</span></span>
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="La propiedad color del elemento" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="73f08-117">La `color` propiedad del elemento</span><span class="sxs-lookup"><span data-stu-id="73f08-117">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73f08-118">Examine la **sección Relación de contraste** del Selector de colores.</span><span class="sxs-lookup"><span data-stu-id="73f08-118">Examine the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="73f08-119">Una marca de verificación significa que el elemento cumple la [recomendación mínima][W3CContrastMinimum].</span><span class="sxs-lookup"><span data-stu-id="73f08-119">One check mark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="73f08-120">Dos marcas de verificación significan que cumple la [recomendación mejorada][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="73f08-120">Two check marks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="La sección Relación de contraste del selector de colores muestra 2 marcas de verificación y un valor de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="73f08-122">La **sección Relación de contraste** del selector de colores muestra 2 marcas de verificación y un valor de</span><span class="sxs-lookup"><span data-stu-id="73f08-122">The **Contrast Ratio** section of the Color Picker shows 2 check marks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="73f08-123">Para obtener más información, seleccione la **sección Relación de contraste** para expandirla.</span><span class="sxs-lookup"><span data-stu-id="73f08-123">For more information, select the **Contrast ratio** section to expand it.</span></span>  <span data-ttu-id="73f08-124">En el selector visual de la parte superior del Selector de colores, aparecen dos líneas que se ejecutan en el selector visual, junto con un círculo para el color actual.</span><span class="sxs-lookup"><span data-stu-id="73f08-124">In the visual picker at the top of the Color Picker, two lines appear, running across the visual picker, along with a circle for the current color.</span></span>  <span data-ttu-id="73f08-125">Si el color actual cumple las recomendaciones, cualquier cosa del mismo lado de la línea también cumple las recomendaciones.</span><span class="sxs-lookup"><span data-stu-id="73f08-125">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="73f08-126">Si el color actual no cumple las recomendaciones, cualquier cosa del mismo lado tampoco cumple las recomendaciones.</span><span class="sxs-lookup"><span data-stu-id="73f08-126">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  

    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Línea de relación de contraste en el selector visual" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="73f08-128">Línea **de relación de** contraste en el selector visual</span><span class="sxs-lookup"><span data-stu-id="73f08-128">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  

1. <span data-ttu-id="73f08-129">Para probar diferentes colores, seleccione dentro del selector visual o seleccione una muestra de color en la parte inferior del Selector de colores.</span><span class="sxs-lookup"><span data-stu-id="73f08-129">To try different colors, select within the visual picker, or select a color swatch at the bottom of the Color Picker.</span></span>
    

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="73f08-130">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="73f08-130">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> <span data-ttu-id="73f08-131">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="73f08-131">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="73f08-132">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="73f08-132">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="73f08-134">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="73f08-134">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- links -->  
[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contraste (mejorado) Nivel AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (mínimo) nivel AA | W3C"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

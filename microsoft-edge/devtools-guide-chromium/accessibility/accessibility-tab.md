---
description: Probar la accesibilidad mediante la pestaña Accesibilidad.
title: Probar la accesibilidad mediante la pestaña Accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 839feed56fc82af2b4d96a081c476696166075b9
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597726"
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
# <a name="test-accessibility-using-the-accessibility-tab"></a><span data-ttu-id="6a8b3-104">Probar la accesibilidad mediante la pestaña Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="6a8b3-104">Test accessibility using the Accessibility tab</span></span>

<span data-ttu-id="6a8b3-105">La **pestaña Accesibilidad** es donde se ve el árbol de accesibilidad, los atributos ARIA y las propiedades de accesibilidad calculada de los nodos DOM.</span><span class="sxs-lookup"><span data-stu-id="6a8b3-105">The **Accessibility** tab is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="6a8b3-106">Para abrir la **pestaña Accesibilidad:**</span><span class="sxs-lookup"><span data-stu-id="6a8b3-106">To open the **Accessibility** tab:</span></span>

1.  <span data-ttu-id="6a8b3-107">Seleccione la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="6a8b3-107">Select the **Elements** tool.</span></span>  
1.  <span data-ttu-id="6a8b3-108">En el **árbol DOM,** seleccione el elemento que desea inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="6a8b3-108">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="6a8b3-109">Seleccione la **pestaña Accesibilidad.**  Es posible que deba seleccionar primero el botón **Más pestañas** \( el botón Más pestañas \) a la derecha ![ de la ](../media/more-tabs-icon.msft.png) **pestaña** Estilos.</span><span class="sxs-lookup"><span data-stu-id="6a8b3-109">Select the **Accessibility** tab.  You might need to first select the **More tabs** \(![the More tabs button](../media/more-tabs-icon.msft.png)\) button to the right of the **Styles** tab.</span></span>

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspeccionar el elemento h1 de la página principal de DevTools en la pestaña Accesibilidad" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="6a8b3-111">Inspeccionar el `h1` elemento de la página principal de DevTools en la pestaña **Accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="6a8b3-111">Inspect the `h1` element of the DevTools homepage in the **Accessibility** tab</span></span>
:::image-end:::  


## <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a><span data-ttu-id="6a8b3-112">Ver la posición de un elemento en el árbol de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="6a8b3-112">View the position of an element in the Accessibility Tree</span></span>

<span data-ttu-id="6a8b3-113">El [árbol de accesibilidad][MDNAccessibilityTree] es un subconjunto del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="6a8b3-113">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="6a8b3-114">El árbol de accesibilidad solo contiene elementos del árbol DOM que son relevantes y útiles para mostrar el contenido de una página a través de tecnologías de asistencia, como lectores de pantalla.</span><span class="sxs-lookup"><span data-stu-id="6a8b3-114">The accessibility tree only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page through assistive technologies such as screen readers.</span></span>

<span data-ttu-id="6a8b3-115">Inspeccione la posición de un elemento en el árbol de accesibilidad desde la **pestaña Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="6a8b3-115">Inspect the position of an element in the accessibility tree from the **Accessibility** tab.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Sección Árbol de accesibilidad" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="6a8b3-117">Sección **Árbol de accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="6a8b3-117">The **Accessibility Tree** section</span></span>  
:::image-end:::  


## <a name="view-the-aria-attributes-of-an-element"></a><span data-ttu-id="6a8b3-118">Ver los atributos ARIA de un elemento</span><span class="sxs-lookup"><span data-stu-id="6a8b3-118">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="6a8b3-119">Los atributos ARIA garantizan que las tecnologías de asistencia, como los lectores de pantalla, tengan toda la información que necesitan para representar correctamente el contenido de una página.</span><span class="sxs-lookup"><span data-stu-id="6a8b3-119">ARIA attributes ensure that assistive technologies such as screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="6a8b3-120">Vea los atributos ARIA de un elemento en la **pestaña Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="6a8b3-120">View the ARIA attributes of an element in the **Accessibility** tab.</span></span>

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Sección Atributos de ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="6a8b3-122">Sección **Atributos de ARIA**</span><span class="sxs-lookup"><span data-stu-id="6a8b3-122">The **ARIA Attributes** section</span></span>  
:::image-end:::  


## <a name="view-the-computed-accessibility-properties-of-an-element"></a><span data-ttu-id="6a8b3-123">Ver las propiedades de accesibilidad calculadas de un elemento</span><span class="sxs-lookup"><span data-stu-id="6a8b3-123">View the computed accessibility properties of an element</span></span>  


<span data-ttu-id="6a8b3-124">El explorador calcula dinámicamente algunas propiedades de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="6a8b3-124">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="6a8b3-125">Estas propiedades se muestran en la **sección Propiedades calculadas** de la **pestaña Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="6a8b3-125">These properties are displayed in the **Computed Properties** section of the **Accessibility** tab.</span></span>  

<span data-ttu-id="6a8b3-126">Vea las propiedades de accesibilidad calculadas de un elemento en la **pestaña Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="6a8b3-126">View the computed accessibility properties of an element in the **Accessibility** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="6a8b3-127">Para las propiedades CSS calculadas, use la [pestaña Calculado.][DevtoolsCssReferenceViewActuallyAppliedElements]</span><span class="sxs-lookup"><span data-stu-id="6a8b3-127">For computed CSS properties, use the [Computed][DevtoolsCssReferenceViewActuallyAppliedElements] tab.</span></span>

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="La sección Propiedades calculadas de la pestaña Accesibilidad" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="6a8b3-129">La **sección Propiedades calculadas** de la **pestaña Accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="6a8b3-129">The **Computed Properties** section of the **Accessibility** tab</span></span>  
:::image-end:::  


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6a8b3-130">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6a8b3-130">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> <span data-ttu-id="6a8b3-131">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6a8b3-131">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6a8b3-132">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="6a8b3-132">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6a8b3-134">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6a8b3-134">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- links -->
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Ver solo el CSS que realmente se aplica a un elemento: referencia CSS | Microsoft Docs"  
[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árbol de accesibilidad (AOM) | MDN"  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  

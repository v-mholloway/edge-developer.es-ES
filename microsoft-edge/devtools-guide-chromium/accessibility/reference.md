---
description: Una referencia completa de las características de accesibilidad en Microsoft Edge DevTools.
title: Referencia de accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a82dec6ffd7e3fb44143ea103fc9756afcd1a161
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564577"
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
# <a name="accessibility-reference"></a><span data-ttu-id="4a5f7-104">Referencia de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="4a5f7-104">Accessibility reference</span></span>  

<span data-ttu-id="4a5f7-105">Esta página es una referencia completa de las características de accesibilidad en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-105">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="4a5f7-106">Está pensado para desarrolladores web que:</span><span class="sxs-lookup"><span data-stu-id="4a5f7-106">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="4a5f7-107">Tenga una comprensión básica de DevTools, como cómo abrirlo.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-107">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="4a5f7-108">Están familiarizados [con los principios de accesibilidad y los procedimientos recomendados.][MDNAccessibility]</span><span class="sxs-lookup"><span data-stu-id="4a5f7-108">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  
    
<span data-ttu-id="4a5f7-109">El propósito de esta referencia es ayudarle a descubrir todas las herramientas disponibles en DevTools que le ayudarán a examinar la accesibilidad de una página.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-109">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="4a5f7-110">Si está buscando ayuda para navegar por DevTools con una tecnología de asistencia como un lector de pantalla, vaya a Navegación Microsoft Edge [DevTools con][DevtoolsAccessibilityNavigation]tecnología de asistencia .</span><span class="sxs-lookup"><span data-stu-id="4a5f7-110">If you are looking for help on navigating DevTools with an assistive technology like a screen reader, navigate to [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation].</span></span>  

## <a name="overview-of-accessibility-features-in-microsoft-edge-devtools"></a><span data-ttu-id="4a5f7-111">Información general sobre las características de accesibilidad en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4a5f7-111">Overview of accessibility features in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="4a5f7-112">En esta sección se explica cómo DevTools se adapta a su kit de herramientas de accesibilidad general.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-112">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="4a5f7-113">Al determinar si una página es accesible, debe tener 2 preguntas generales en mente:</span><span class="sxs-lookup"><span data-stu-id="4a5f7-113">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="4a5f7-114">¿Puede navegar por la página con un teclado o un [lector de pantalla?][MDNScreenReader]</span><span class="sxs-lookup"><span data-stu-id="4a5f7-114">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="4a5f7-115">¿Los elementos de la página están correctamente marcados para los lectores de pantalla?</span><span class="sxs-lookup"><span data-stu-id="4a5f7-115">Are the elements of the page properly marked up for screen readers?</span></span>  
    
<span data-ttu-id="4a5f7-116">En general, DevTools debe ayudarle a corregir errores relacionados con la pregunta #2, ya que estos errores son fáciles de detectar de forma automatizada.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-116">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="4a5f7-117">La #1 preguntas es igual de importante, pero desafortunadamente DevTools no le ayuda allí.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-117">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="4a5f7-118">La única forma de encontrar errores relacionados con la pregunta #1 es intentar usar una página con un teclado o un lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-118">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--To learn more, navigate to [How To Do An Accessibility Review][AccessibilityReview].  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <a name="audit-the-accessibility-of-a-page"></a><span data-ttu-id="4a5f7-119">Auditar la accesibilidad de una página</span><span class="sxs-lookup"><span data-stu-id="4a5f7-119">Audit the accessibility of a page</span></span>  

> [!NOTE]
> <span data-ttu-id="4a5f7-120">La **herramienta Auditorías** proporciona vínculos al contenido hospedado en sitios web de terceros.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-120">The **Audits** tool provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="4a5f7-121">Microsoft no es responsable y no tiene control sobre el contenido de estos sitios ni sobre los datos que se puedan recopilar.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-121">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="4a5f7-122">En general, use el panel Auditorías para determinar si:</span><span class="sxs-lookup"><span data-stu-id="4a5f7-122">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="4a5f7-123">Una página está correctamente marcada para lectores de pantalla.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-123">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="4a5f7-124">Los elementos de texto de una página tienen suficientes relaciones de contraste.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-124">The text elements on a page have sufficient contrast ratios.</span></span>  <span data-ttu-id="4a5f7-125">Desplácese [hasta Ver la relación de contraste de un elemento de texto en el Selector de colores](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span><span class="sxs-lookup"><span data-stu-id="4a5f7-125">Navigate to [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="4a5f7-126">Para auditar una página:</span><span class="sxs-lookup"><span data-stu-id="4a5f7-126">To audit a page:</span></span>  

1.  <span data-ttu-id="4a5f7-127">Vaya a la dirección URL que desea auditar.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-127">Navigate to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="4a5f7-128">En DevTools, elija la **herramienta Auditorías.**</span><span class="sxs-lookup"><span data-stu-id="4a5f7-128">In DevTools, choose the **Audits** tool.</span></span>  <span data-ttu-id="4a5f7-129">DevTools muestra varias opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-129">DevTools shows you various configuration options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-audits-pane.msft.png":::
       <span data-ttu-id="4a5f7-131">Configurar auditorías</span><span class="sxs-lookup"><span data-stu-id="4a5f7-131">Configure audits</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="4a5f7-132">Las capturas de pantalla de esta sección se tomaron Microsoft Edge versión 79.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-132">The screenshots in this section were taken with Microsoft Edge version 79.</span></span>  <span data-ttu-id="4a5f7-133">Puede comprobar la versión que está ejecutando en `edge://version` .</span><span class="sxs-lookup"><span data-stu-id="4a5f7-133">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="4a5f7-134">La interfaz de usuario de la herramienta **Auditorías** tiene un aspecto diferente en versiones anteriores de Microsoft Edge, pero el flujo de trabajo general es el mismo.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-134">The **Audits** tool UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="4a5f7-135">Para **Dispositivo,** elija **Móvil** si desea simular un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-135">For **Device**, choose **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="4a5f7-136">Esta opción cambia la cadena del agente de usuario y cambia el tamaño de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-136">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="4a5f7-137">Si la versión móvil de la página se muestra de forma diferente a la versión de escritorio, esta opción puede tener un efecto significativo en los resultados de la auditoría.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-137">If the mobile version of the page displays differently than the desktop version, this option may have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="4a5f7-138">En la **sección Auditorías,** asegúrese de que **la accesibilidad** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-138">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="4a5f7-139">Deshabilite las otras categorías si desea excluirlas del informe.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-139">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="4a5f7-140">Déjelos habilitados si desea descubrir otras formas de mejorar la calidad de la página.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-140">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="4a5f7-141">La **sección Limitación permite** limitar la red y la CPU, lo que resulta útil al analizar el rendimiento de la carga.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-141">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="4a5f7-142">Esta opción debe ser irrelevante para la puntuación de accesibilidad, por lo que puedes usar lo que prefieras.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-142">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="4a5f7-143">La **casilla Borrar Storage** permite borrar todo el almacenamiento antes de cargar la página o conservar el almacenamiento entre cargas de página.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-143">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="4a5f7-144">Esta opción también es probablemente irrelevante para la puntuación de accesibilidad, por lo que puede usar lo que prefiera.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-144">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="4a5f7-145">Elija **Ejecutar auditorías**.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-145">Choose **Run Audits**.</span></span> <span data-ttu-id="4a5f7-146">Después de 10 a 30 segundos, DevTools proporciona un informe.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-146">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="4a5f7-147">El informe le ofrece varias sugerencias sobre cómo mejorar la accesibilidad de la página.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-147">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Un informe" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       <span data-ttu-id="4a5f7-149">Un informe</span><span class="sxs-lookup"><span data-stu-id="4a5f7-149">A report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4a5f7-150">Elija una auditoría para obtener más información sobre ella.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-150">Choose an audit to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Más información sobre una auditoría" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       <span data-ttu-id="4a5f7-152">Más información sobre una auditoría</span><span class="sxs-lookup"><span data-stu-id="4a5f7-152">More information about an audit</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4a5f7-153">Elija **Obtener más información** para ver la documentación de esa auditoría.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-153">Choose **Learn More** to view the documentation of that audit.</span></span>  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Ver la documentación de una auditoría" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="4a5f7-155">Ver la documentación de una auditoría</span><span class="sxs-lookup"><span data-stu-id="4a5f7-155">View the documentation of an audit</span></span>  
    :::image-end:::  
    
### <a name="see-also-axe-extension"></a><span data-ttu-id="4a5f7-156">Vea también: extensión aXe</span><span class="sxs-lookup"><span data-stu-id="4a5f7-156">See also: aXe extension</span></span>  

<span data-ttu-id="4a5f7-157">Es posible que prefiera usar la [extensión aXe en][ChromeWebStoreAxe] lugar de la **herramienta Auditorías.**</span><span class="sxs-lookup"><span data-stu-id="4a5f7-157">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** tool.</span></span>  
<span data-ttu-id="4a5f7-158">La extensión aXe generalmente proporciona la misma información, ya que es el motor subyacente el que impulsa el panel Auditorías.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-158">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="4a5f7-159">La extensión aXe tiene una interfaz de usuario diferente y describe las auditorías de forma ligeramente diferente.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-159">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="4a5f7-160">Una ventaja que la extensión aXe tiene sobre la herramienta **Auditorías** es que le permite inspeccionar y resaltar nodos con errores.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-160">One advantage that the aXe extension has over the **Audits** tool is that it enables you to inspect and highlight failing nodes.</span></span>  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="La extensión aXe" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   <span data-ttu-id="4a5f7-162">La extensión aXe</span><span class="sxs-lookup"><span data-stu-id="4a5f7-162">The aXe extension</span></span>  
:::image-end:::  

## <a name="the-accessibility-panel"></a><span data-ttu-id="4a5f7-163">Panel accesibilidad</span><span class="sxs-lookup"><span data-stu-id="4a5f7-163">The Accessibility panel</span></span>  

<span data-ttu-id="4a5f7-164">El **panel Accesibilidad** es donde se ve el árbol de accesibilidad, los atributos ARIA y las propiedades de accesibilidad calculada de los nodos DOM.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-164">The **Accessibility** panel is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="4a5f7-165">Para abrir el panel **Accesibilidad:**</span><span class="sxs-lookup"><span data-stu-id="4a5f7-165">To open the **Accessibility** panel:</span></span>  

1.  <span data-ttu-id="4a5f7-166">Elija la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-166">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="4a5f7-167">En el **árbol DOM,** seleccione el elemento que desea inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-167">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="4a5f7-168">Elija el panel **Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="4a5f7-168">Choose the **Accessibility** panel.</span></span>  <span data-ttu-id="4a5f7-169">Este panel puede estar oculto detrás del **botón Más pestañas** \( ![ Más pestañas ](../media/more-tabs-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="4a5f7-169">This panel may be hidden behind the **More Tabs** \(![More Tabs](../media/more-tabs-icon.msft.png)\) button.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspeccionar el elemento h1 de la página principal de DevTools en el panel Accesibilidad" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="4a5f7-171">Inspeccionar el `h1` elemento de la página principal de DevTools en el panel **Accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="4a5f7-171">Inspect the `h1` element of the DevTools homepage in the **Accessibility** panel</span></span>  
:::image-end:::  

### <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a><span data-ttu-id="4a5f7-172">Ver la posición de un elemento en el árbol de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="4a5f7-172">View the position of an element in the accessibility tree</span></span>  

<span data-ttu-id="4a5f7-173">El [árbol de accesibilidad][MDNAccessibilityTree] es un subconjunto del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-173">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="4a5f7-174">Solo contiene elementos del árbol DOM que son relevantes y útiles para mostrar el contenido de una página en un lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-174">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="4a5f7-175">Inspeccione la posición de un elemento en el árbol de accesibilidad desde el panel [Accesibilidad.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="4a5f7-175">Inspect the position of an element in the accessibility tree from the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Sección Árbol de accesibilidad" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="4a5f7-177">Sección **Árbol de accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="4a5f7-177">The **Accessibility Tree** section</span></span>  
:::image-end:::  

### <a name="view-the-aria-attributes-of-an-element"></a><span data-ttu-id="4a5f7-178">Ver los atributos ARIA de un elemento</span><span class="sxs-lookup"><span data-stu-id="4a5f7-178">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="4a5f7-179">Los atributos ARIA garantizan que los lectores de pantalla tengan toda la información que necesitan para representar correctamente el contenido de una página.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-179">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="4a5f7-180">Vea los atributos ARIA de un elemento en el panel [Accesibilidad.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="4a5f7-180">View the ARIA attributes of an element in the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Sección Atributos de ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="4a5f7-182">Sección **Atributos de ARIA**</span><span class="sxs-lookup"><span data-stu-id="4a5f7-182">The **ARIA Attributes** section</span></span>  
:::image-end:::  

### <a name="view-the-computed-accessibility-properties-of-an-element"></a><span data-ttu-id="4a5f7-183">Ver las propiedades de accesibilidad calculadas de un elemento</span><span class="sxs-lookup"><span data-stu-id="4a5f7-183">View the computed accessibility properties of an element</span></span>  

> [!NOTE]
> <span data-ttu-id="4a5f7-184">Si está buscando propiedades CSS calculadas, vaya al panel [Calculado.][DevtoolsCssReferenceViewActuallyAppliedElements]</span><span class="sxs-lookup"><span data-stu-id="4a5f7-184">If you are looking for computed CSS properties, navigate to [Computed][DevtoolsCssReferenceViewActuallyAppliedElements] panel.</span></span>  

<span data-ttu-id="4a5f7-185">El explorador calcula dinámicamente algunas propiedades de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-185">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="4a5f7-186">Estas propiedades se muestran en la **sección Propiedades calculadas** del panel **Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="4a5f7-186">These properties are displayed in the **Computed Properties** section of the **Accessibility** panel.</span></span>  

<span data-ttu-id="4a5f7-187">Vea las propiedades de accesibilidad calculadas de un elemento en el panel [Accesibilidad.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="4a5f7-187">View the computed accessibility properties of an element in the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Sección Propiedades calculadas del panel Accesibilidad" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="4a5f7-189">Sección **Propiedades calculadas** del panel **Accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="4a5f7-189">The **Computed Properties** section of the **Accessibility** panel</span></span>  
:::image-end:::  

## <a name="view-the-contrast-ratio-of-a-text-element-in-the-color-picker"></a><span data-ttu-id="4a5f7-190">Ver la relación de contraste de un elemento de texto en el Selector de colores</span><span class="sxs-lookup"><span data-stu-id="4a5f7-190">View the contrast ratio of a text element in the Color Picker</span></span>  

<span data-ttu-id="4a5f7-191">Algunas personas con visión baja no ven áreas como muy brillantes o muy oscuras.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-191">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="4a5f7-192">Todo tiende a aparecer con aproximadamente el mismo brillo, lo que hace que sea difícil distinguir contornos y bordes.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-192">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="4a5f7-193">La relación de contraste mide la diferencia de brillo entre el primer plano y el fondo del texto.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-193">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="4a5f7-194">Si el texto tiene una relación de contraste baja, estos usuarios de visión baja pueden experimentar literalmente el sitio como una pantalla en blanco.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-194">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="4a5f7-195">El Selector de colores te ayuda a comprobar que el texto cumple los niveles de relación de contraste recomendados:</span><span class="sxs-lookup"><span data-stu-id="4a5f7-195">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="4a5f7-196">Elija la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-196">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="4a5f7-197">En el **árbol DOM,** seleccione el elemento de texto que desea inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-197">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspeccionar un párrafo en el árbol DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="4a5f7-199">Inspeccionar un párrafo en el **árbol DOM**</span><span class="sxs-lookup"><span data-stu-id="4a5f7-199">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4a5f7-200">En el panel **Estilos,** elija el cuadrado de color junto al `color` valor del elemento.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-200">In the **Styles** panel, choose the color square next to the `color` value of the element.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="La propiedad color del elemento" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="4a5f7-202">La `color` propiedad del elemento</span><span class="sxs-lookup"><span data-stu-id="4a5f7-202">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4a5f7-203">Compruebe la **sección Relación de contraste** del Selector de colores.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-203">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="4a5f7-204">Una marca de verificación significa que el elemento cumple la [recomendación mínima][W3CContrastMinimum].</span><span class="sxs-lookup"><span data-stu-id="4a5f7-204">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="4a5f7-205">Dos marcas de verificación significa que cumple la [recomendación mejorada][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="4a5f7-205">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="La sección Relación de contraste del Selector de colores muestra 2 marcas de verificación y un valor de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="4a5f7-207">La **sección Relación de contraste** del selector de colores muestra 2 marcas de verificación y un valor de</span><span class="sxs-lookup"><span data-stu-id="4a5f7-207">The **Contrast Ratio** section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="4a5f7-208">Para obtener más información, elija la **sección Relación de** contraste.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-208">For more information, choose the **Contrast Ratio** section.</span></span>  <span data-ttu-id="4a5f7-209">Aparece una línea en el selector visual en la parte superior del Selector de colores.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-209">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="4a5f7-210">Si el color actual cumple las recomendaciones, cualquier cosa del mismo lado de la línea también cumple las recomendaciones.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-210">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="4a5f7-211">Si el color actual no cumple las recomendaciones, cualquier cosa del mismo lado tampoco cumple las recomendaciones.</span><span class="sxs-lookup"><span data-stu-id="4a5f7-211">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Línea de relación de contraste en el selector visual" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="4a5f7-213">Línea **de relación de** contraste en el selector visual</span><span class="sxs-lookup"><span data-stu-id="4a5f7-213">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4a5f7-214">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4a5f7-214">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Navegue Microsoft Edge DevTools con tecnología de asistencia | Microsoft Docs"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Ver solo el CSS que realmente se aplica a un elemento: referencia CSS | Microsoft Docs"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe - Pruebas de accesibilidad web - Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árbol de accesibilidad (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Accesibilidad | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Lector de pantalla | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contraste (mejorado) Nivel AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (mínimo) nivel AA | W3C"  

> [!NOTE]
> <span data-ttu-id="4a5f7-223">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4a5f7-223">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4a5f7-224">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="4a5f7-224">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4a5f7-226">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4a5f7-226">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

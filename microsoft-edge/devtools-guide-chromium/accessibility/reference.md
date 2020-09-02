---
title: Referencia de accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a338e78957d664a4552e5882f1ae7882f0eee89a
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986090"
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

# <span data-ttu-id="3a02e-103">Referencia de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="3a02e-103">Accessibility reference</span></span>  

<span data-ttu-id="3a02e-104">Esta página es una referencia completa de las características de accesibilidad en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="3a02e-104">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="3a02e-105">Está destinada a los programadores web que:</span><span class="sxs-lookup"><span data-stu-id="3a02e-105">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="3a02e-106">Tener un conocimiento básico de DevTools, como, por ejemplo, cómo abrirlo.</span><span class="sxs-lookup"><span data-stu-id="3a02e-106">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="3a02e-107">Está familiarizado con los [principios de accesibilidad y los procedimientos recomendados][MDNAccessibility].</span><span class="sxs-lookup"><span data-stu-id="3a02e-107">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  
    
<span data-ttu-id="3a02e-108">El propósito de esta referencia es ayudarle a descubrir todas las herramientas disponibles en DevTools que le ayudan a examinar la accesibilidad de una página.</span><span class="sxs-lookup"><span data-stu-id="3a02e-108">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="3a02e-109">Consulte [navegar por Microsoft Edge DevTools con tecnología de asistencia][DevtoolsAccessibilityNavigation] si necesita ayuda para navegar por DevTools con una tecnología de asistencia, como un lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="3a02e-109">See [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation] if you are looking for help on navigating DevTools with an assistive technology like a screen reader.</span></span>  

## <span data-ttu-id="3a02e-110">Información general sobre las características de accesibilidad en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3a02e-110">Overview of accessibility features in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="3a02e-111">En esta sección se explica cómo DevTools encaja en el conjunto de herramientas general de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="3a02e-111">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="3a02e-112">Al determinar si una página es accesible, debe tener en cuenta dos preguntas generales:</span><span class="sxs-lookup"><span data-stu-id="3a02e-112">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="3a02e-113">¿Puede navegar por la página con un teclado o un [lector de pantalla][MDNScreenReader]?</span><span class="sxs-lookup"><span data-stu-id="3a02e-113">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="3a02e-114">¿Están los elementos de la página correctamente marcados para los lectores de pantalla?</span><span class="sxs-lookup"><span data-stu-id="3a02e-114">Are the elements of the page properly marked up for screen readers?</span></span>  
    
<span data-ttu-id="3a02e-115">En general, DevTools debería ayudarle a corregir los errores relacionados con preguntas #2, porque estos errores son fáciles de detectar de forma automática.</span><span class="sxs-lookup"><span data-stu-id="3a02e-115">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="3a02e-116">La pregunta #1 es tan importante, pero lamentablemente DevTools no le ayuda a usted.</span><span class="sxs-lookup"><span data-stu-id="3a02e-116">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="3a02e-117">La única forma de buscar errores relacionados con la pregunta #1 es intentar usar una página con un teclado o lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="3a02e-117">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <span data-ttu-id="3a02e-118">Auditar la accesibilidad de una página</span><span class="sxs-lookup"><span data-stu-id="3a02e-118">Audit the accessibility of a page</span></span>  

> [!NOTE]
> <span data-ttu-id="3a02e-119">El panel **Auditoría** proporciona vínculos a contenido hospedado en sitios web de terceros.</span><span class="sxs-lookup"><span data-stu-id="3a02e-119">The **Audits** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="3a02e-120">Microsoft no se responsabiliza y no tiene ningún control sobre el contenido de estos sitios y los datos que se pueden recopilar.</span><span class="sxs-lookup"><span data-stu-id="3a02e-120">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="3a02e-121">En general, use el panel auditorías para determinar si:</span><span class="sxs-lookup"><span data-stu-id="3a02e-121">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="3a02e-122">Una página se marcó correctamente para los lectores de pantalla.</span><span class="sxs-lookup"><span data-stu-id="3a02e-122">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="3a02e-123">Los elementos de texto de una página tienen relaciones de contraste suficientes.</span><span class="sxs-lookup"><span data-stu-id="3a02e-123">The text elements on a page have sufficient contrast ratios.</span></span>  <span data-ttu-id="3a02e-124">Consulte [ver la relación de contraste de un elemento de texto en el selector de colores](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span><span class="sxs-lookup"><span data-stu-id="3a02e-124">See [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="3a02e-125">Para auditar una página:</span><span class="sxs-lookup"><span data-stu-id="3a02e-125">To audit a page:</span></span>  

1.  <span data-ttu-id="3a02e-126">Vaya a la dirección URL que desea auditar.</span><span class="sxs-lookup"><span data-stu-id="3a02e-126">Go to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="3a02e-127">En DevTools, haga clic en la pestaña **auditorías** .  En DevTools se muestran varias opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="3a02e-127">In DevTools, click the **Audits** tab.  DevTools shows you various configuration options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Configurar auditorías" lightbox="../media/accessibility-audits-pane.msft.png":::
       <span data-ttu-id="3a02e-129">Configurar auditorías</span><span class="sxs-lookup"><span data-stu-id="3a02e-129">Configure audits</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="3a02e-130">Las capturas de pantallas de esta sección se han tomado con la versión 79 de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3a02e-130">The screenshots in this section were taken with version 79 of Microsoft Edge.</span></span>  <span data-ttu-id="3a02e-131">Puede consultar qué versión está ejecutando `edge://version` .</span><span class="sxs-lookup"><span data-stu-id="3a02e-131">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="3a02e-132">La interfaz de usuario del panel **auditorías** tiene un aspecto diferente en versiones anteriores de Microsoft Edge, pero el flujo de trabajo general es el mismo.</span><span class="sxs-lookup"><span data-stu-id="3a02e-132">The **Audits** panel UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="3a02e-133">En **dispositivo**, seleccione **móvil** si desea simular un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="3a02e-133">For **Device**, select **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="3a02e-134">Esta opción cambia la cadena de agente de usuario y cambia el tamaño de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="3a02e-134">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="3a02e-135">Si la versión móvil de la página se muestra de forma diferente a la de la versión de escritorio, esta opción podría tener un efecto significativo en los resultados de la auditoría.</span><span class="sxs-lookup"><span data-stu-id="3a02e-135">If the mobile version of the page displays differently than the desktop version, this option could have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="3a02e-136">En la sección **auditorías** , asegúrese de que **accesibilidad** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="3a02e-136">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="3a02e-137">Deshabilite las otras categorías si desea excluirlas de su informe.</span><span class="sxs-lookup"><span data-stu-id="3a02e-137">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="3a02e-138">Déjelas habilitadas si deseas descubrir otras formas de mejorar la calidad de la página.</span><span class="sxs-lookup"><span data-stu-id="3a02e-138">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="3a02e-139">La sección de **limitación** le permite limitar la red y la CPU, lo cual es útil al analizar el rendimiento de la carga.</span><span class="sxs-lookup"><span data-stu-id="3a02e-139">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="3a02e-140">Esta opción no debe ser relevante para la puntuación de accesibilidad, por lo que puede usar lo que prefiera.</span><span class="sxs-lookup"><span data-stu-id="3a02e-140">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="3a02e-141">La casilla **Borrar almacenamiento** le permite borrar todo el almacenamiento antes de cargar la página o conservar el almacenamiento entre cargas de páginas.</span><span class="sxs-lookup"><span data-stu-id="3a02e-141">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="3a02e-142">Esta opción también probablemente es irrelevante para la puntuación de accesibilidad, por lo que puede usar lo que prefiera.</span><span class="sxs-lookup"><span data-stu-id="3a02e-142">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="3a02e-143">Haga clic en **Ejecutar Auditorías**.</span><span class="sxs-lookup"><span data-stu-id="3a02e-143">Click **Run Audits**.</span></span> <span data-ttu-id="3a02e-144">Después de 10 a 30 segundos, DevTools proporciona un informe.</span><span class="sxs-lookup"><span data-stu-id="3a02e-144">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="3a02e-145">El informe le ofrece varias sugerencias para mejorar la accesibilidad de la página.</span><span class="sxs-lookup"><span data-stu-id="3a02e-145">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Un informe" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       <span data-ttu-id="3a02e-147">Un informe</span><span class="sxs-lookup"><span data-stu-id="3a02e-147">A report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3a02e-148">Haga clic en una auditoría para obtener más información sobre ella.</span><span class="sxs-lookup"><span data-stu-id="3a02e-148">Click an audit to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Más información sobre una auditoría" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       <span data-ttu-id="3a02e-150">Más información sobre una auditoría</span><span class="sxs-lookup"><span data-stu-id="3a02e-150">More information about an audit</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3a02e-151">Haga clic en más **información** para ver la documentación de esa auditoría.</span><span class="sxs-lookup"><span data-stu-id="3a02e-151">Click **Learn More** to view the documentation of that audit.</span></span>  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Ver la documentación de una auditoría" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="3a02e-153">Ver la documentación de una auditoría</span><span class="sxs-lookup"><span data-stu-id="3a02e-153">View the documentation of an audit</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="3a02e-154">Vea también: extensión aXe</span><span class="sxs-lookup"><span data-stu-id="3a02e-154">See also: aXe extension</span></span>  

<span data-ttu-id="3a02e-155">Es posible que prefiera usar la [extensión de aXe][ChromeWebStoreAxe] en lugar del panel **auditorías** .</span><span class="sxs-lookup"><span data-stu-id="3a02e-155">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** panel.</span></span>  
<span data-ttu-id="3a02e-156">La extensión aXe generalmente proporciona la misma información, ya que es el motor subyacente que alimenta el panel auditorías.</span><span class="sxs-lookup"><span data-stu-id="3a02e-156">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="3a02e-157">La extensión de aXe tiene una interfaz de usuario diferente y describe las auditorías de forma ligeramente distinta.</span><span class="sxs-lookup"><span data-stu-id="3a02e-157">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="3a02e-158">Una de las ventajas de que la extensión aXe está en el panel **Auditoría** es que le permite inspeccionar y resaltar los nodos con errores.</span><span class="sxs-lookup"><span data-stu-id="3a02e-158">One advantage that the aXe extension has over the **Audits** panel is that it enables you to inspect and highlight failing nodes.</span></span>  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="La extensión de aXe" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   <span data-ttu-id="3a02e-160">La extensión de aXe</span><span class="sxs-lookup"><span data-stu-id="3a02e-160">The aXe extension</span></span>  
:::image-end:::  

## <span data-ttu-id="3a02e-161">El panel Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="3a02e-161">The Accessibility pane</span></span>  

<span data-ttu-id="3a02e-162">El panel de **accesibilidad** es el lugar donde se ve el árbol de accesibilidad, los atributos de Aria y las propiedades de accesibilidad calculadas de los nodos DOM.</span><span class="sxs-lookup"><span data-stu-id="3a02e-162">The **Accessibility** pane is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="3a02e-163">Para abrir el panel **accesibilidad** :</span><span class="sxs-lookup"><span data-stu-id="3a02e-163">To open the **Accessibility** pane:</span></span>  

1.  <span data-ttu-id="3a02e-164">Haga clic en la pestaña **elementos** .</span><span class="sxs-lookup"><span data-stu-id="3a02e-164">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="3a02e-165">En el **árbol DOM**, seleccione el elemento que desea inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="3a02e-165">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="3a02e-166">Haga clic en la pestaña **accesibilidad** .  Es posible que esta pestaña esté oculta detrás del botón **más pestañas** \ ( ![ más pestañas ][ImageMoreTabsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3a02e-166">Click the **Accessibility** tab.  This tab may be hidden behind the **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) button.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspeccionar el elemento H1 de la Página principal de DevTools en el panel Accesibilidad" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="3a02e-168">Inspeccionar el `h1` elemento de la Página principal de DevTools en el panel **accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="3a02e-168">Inspect the `h1` element of the DevTools homepage in the **Accessibility** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="3a02e-169">Ver la posición de un elemento en el árbol de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="3a02e-169">View the position of an element in the accessibility tree</span></span>  

<span data-ttu-id="3a02e-170">El [árbol de accesibilidad][MDNAccessibilityTree] es un subconjunto del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="3a02e-170">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="3a02e-171">Solo contiene elementos del árbol DOM que son relevantes y útiles para mostrar el contenido de una página en un lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="3a02e-171">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="3a02e-172">Inspeccione la posición de un elemento en el árbol de accesibilidad en el [panel Accesibilidad](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="3a02e-172">Inspect the position of an element in the accessibility tree from the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Sección de árbol de accesibilidad" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="3a02e-174">Sección de **árbol de accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="3a02e-174">The **Accessibility Tree** section</span></span>  
:::image-end:::  

### <span data-ttu-id="3a02e-175">Ver los atributos de ARIA de un elemento</span><span class="sxs-lookup"><span data-stu-id="3a02e-175">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="3a02e-176">Los atributos de ARIA garantizan que los lectores de pantalla tengan toda la información que necesitan para representar correctamente el contenido de una página.</span><span class="sxs-lookup"><span data-stu-id="3a02e-176">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="3a02e-177">Ver los atributos de ARIA de un elemento en el [Panel de accesibilidad](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="3a02e-177">View the ARIA attributes of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="La sección de atributos de ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="3a02e-179">La sección de **atributos de Aria**</span><span class="sxs-lookup"><span data-stu-id="3a02e-179">The **ARIA Attributes** section</span></span>  
:::image-end:::  

### <span data-ttu-id="3a02e-180">Ver las propiedades de accesibilidad calculadas de un elemento</span><span class="sxs-lookup"><span data-stu-id="3a02e-180">View the computed accessibility properties of an element</span></span>  

> [!NOTE]
> <span data-ttu-id="3a02e-181">Si está buscando propiedades calculadas de CSS, consulte la [pestaña calculada][DevtoolsCssReferenceViewActuallyAppliedElements].</span><span class="sxs-lookup"><span data-stu-id="3a02e-181">If you are looking for computed CSS properties, see the [Computed tab][DevtoolsCssReferenceViewActuallyAppliedElements].</span></span>  

<span data-ttu-id="3a02e-182">El explorador calcula dinámicamente algunas propiedades de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="3a02e-182">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="3a02e-183">Estas propiedades se muestran en la sección **propiedades calculadas** del panel **accesibilidad** .</span><span class="sxs-lookup"><span data-stu-id="3a02e-183">These properties are displayed in the **Computed Properties** section of the **Accessibility** pane.</span></span>  

<span data-ttu-id="3a02e-184">Ver las propiedades de accesibilidad calculadas de un elemento en el [Panel de accesibilidad](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="3a02e-184">View the computed accessibility properties of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Sección propiedades calculadas del panel Accesibilidad" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="3a02e-186">Sección **propiedades calculadas** del panel **accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="3a02e-186">The **Computed Properties** section of the **Accessibility** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="3a02e-187">Ver la relación de contraste de un elemento de texto en el selector de colores</span><span class="sxs-lookup"><span data-stu-id="3a02e-187">View the contrast ratio of a text element in the Color Picker</span></span>  

<span data-ttu-id="3a02e-188">Algunas personas con deficiencias visuales no ven las áreas muy claras o muy oscuras.</span><span class="sxs-lookup"><span data-stu-id="3a02e-188">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="3a02e-189">Todo tiende a aparecer sobre el mismo brillo, lo que hace que sea difícil distinguir los esquemas y los bordes.</span><span class="sxs-lookup"><span data-stu-id="3a02e-189">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="3a02e-190">La relación de contraste mide la diferencia de brillo entre el primer plano y el fondo del texto.</span><span class="sxs-lookup"><span data-stu-id="3a02e-190">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="3a02e-191">Si el texto tiene una relación de contraste baja, es posible que los usuarios de estas deficiencias experimenten literalmente su sitio como pantalla en blanco.</span><span class="sxs-lookup"><span data-stu-id="3a02e-191">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="3a02e-192">El selector de colores le ayuda a comprobar que el texto cumple los niveles de proporción de contraste recomendados:</span><span class="sxs-lookup"><span data-stu-id="3a02e-192">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="3a02e-193">Haga clic en la pestaña **elementos** .</span><span class="sxs-lookup"><span data-stu-id="3a02e-193">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="3a02e-194">En el **árbol DOM**, seleccione el elemento de texto que desea inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="3a02e-194">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspeccionar un párrafo del árbol DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="3a02e-196">Inspeccionar un párrafo del **árbol DOM**</span><span class="sxs-lookup"><span data-stu-id="3a02e-196">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3a02e-197">En el panel **estilos** , haga clic en el cuadrado de color situado junto al `color` valor del elemento.</span><span class="sxs-lookup"><span data-stu-id="3a02e-197">In the **Styles** pane, click the color square next to the `color` value of the element.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Propiedad color del elemento" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="3a02e-199">La `color` propiedad del elemento</span><span class="sxs-lookup"><span data-stu-id="3a02e-199">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3a02e-200">Compruebe la sección **relación de contraste** del selector de colores.</span><span class="sxs-lookup"><span data-stu-id="3a02e-200">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="3a02e-201">Una marca de verificación significa que el elemento cumple con la [recomendación mínima][W3CContrastMinimum].</span><span class="sxs-lookup"><span data-stu-id="3a02e-201">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="3a02e-202">Dos marcas de verificación significa que cumple con la [Recomendación mejorada][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="3a02e-202">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="La sección relación de contraste del selector de color muestra 2 marcas de verificación y un valor de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="3a02e-204">La sección de **relación de contraste** del selector de color muestra 2 marcas de verificación y un valor de</span><span class="sxs-lookup"><span data-stu-id="3a02e-204">The **Contrast Ratio** section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="3a02e-205">Haga clic en la sección **relación de contraste** para ver más información.</span><span class="sxs-lookup"><span data-stu-id="3a02e-205">Click the **Contrast Ratio** section to see more information.</span></span>  <span data-ttu-id="3a02e-206">Aparece una línea en el selector visual en la parte superior del selector de colores.</span><span class="sxs-lookup"><span data-stu-id="3a02e-206">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="3a02e-207">Si el color actual cumple con las recomendaciones, cualquier cosa en el mismo lado de la línea también se ajusta a las recomendaciones.</span><span class="sxs-lookup"><span data-stu-id="3a02e-207">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="3a02e-208">Si el color actual no cumple con las recomendaciones, entonces cualquier cosa en el mismo lado no cumple con las recomendaciones.</span><span class="sxs-lookup"><span data-stu-id="3a02e-208">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="La línea de proporción de contraste en el selector visual" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="3a02e-210">La línea de **proporción de contraste** en el selector visual</span><span class="sxs-lookup"><span data-stu-id="3a02e-210">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  
    
<!--## Feedback   -->  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Navegar por Microsoft Edge DevTools con tecnología de asistencia | Microsoft docs"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Ver solo la CSS que se aplica realmente a una referencia CSS de elemento | Microsoft docs"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "Axe-pruebas de accesibilidad web-tienda web de Chrome"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árbol de accesibilidad (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Accesibilidad | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Lector de pantalla | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Nivel de contraste (mejorado) AAA AAA | RELATIVA"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (mínimo) nivel AA | RELATIVA"  

> [!NOTE]
> <span data-ttu-id="3a02e-219">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3a02e-219">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3a02e-220">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="3a02e-220">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3a02e-222">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3a02e-222">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

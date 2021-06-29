---
description: Use la herramienta Problemas para identificar y solucionar problemas con la página web actual.
title: Buscar y corregir problemas con la herramienta Problemas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/24/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 86277c509aa4b67635661ba3a316fb5b1e3b9d14
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624727"
---
<!-- Copyright Sam Dutton

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="find-and-fix-problems-using-the-issues-tool"></a><span data-ttu-id="856c2-104">Buscar y corregir problemas con la herramienta Problemas</span><span class="sxs-lookup"><span data-stu-id="856c2-104">Find and fix problems using the Issues tool</span></span>

<span data-ttu-id="856c2-105">En Microsoft Edge DevTools, la \*\*\*\* herramienta Problemas analiza automáticamente la página web actual, informa de los problemas agrupados por tipo y proporciona documentación para ayudar a explicar y resolver los problemas.</span><span class="sxs-lookup"><span data-stu-id="856c2-105">In Microsoft Edge DevTools, the **Issues** tool automatically analyzes the current webpage, reports issues grouped by type, and provides documentation to help explain and resolve the issues.</span></span>

<span data-ttu-id="856c2-106">La **herramienta Problemas** proporciona comentarios en las siguientes categorías:</span><span class="sxs-lookup"><span data-stu-id="856c2-106">The **Issues** tool provides feedback in the following categories:</span></span>
*  <span data-ttu-id="856c2-107">Accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="856c2-107">Accessibility.</span></span>
*  <span data-ttu-id="856c2-108">Compatibilidad entre exploradores.</span><span class="sxs-lookup"><span data-stu-id="856c2-108">Compatibility across browsers.</span></span>
*  <span data-ttu-id="856c2-109">Rendimiento.</span><span class="sxs-lookup"><span data-stu-id="856c2-109">Performance.</span></span>
*  <span data-ttu-id="856c2-110">Aplicaciones web progresivas.</span><span class="sxs-lookup"><span data-stu-id="856c2-110">Progressive Web Apps.</span></span>
*  <span data-ttu-id="856c2-111">Security.</span><span class="sxs-lookup"><span data-stu-id="856c2-111">Security.</span></span>
*  <span data-ttu-id="856c2-112">Otros.</span><span class="sxs-lookup"><span data-stu-id="856c2-112">Other.</span></span>

<span data-ttu-id="856c2-113">Varios orígenes **proporcionan** comentarios en la herramienta Problemas, como la plataforma Chromium, El eje Deque, los datos de compatibilidad del explorador MDN y la webhint.</span><span class="sxs-lookup"><span data-stu-id="856c2-113">Feedback in the **Issues** tool is provided by several sources, including the Chromium platform, Deque axe, MDN browser compatibility data, and webhint.</span></span>  <span data-ttu-id="856c2-114">Para obtener información sobre estos orígenes de comentarios que rellenan la **herramienta Problemas,** vaya a:</span><span class="sxs-lookup"><span data-stu-id="856c2-114">For information about these sources of feedback that populate the **Issues** tool, navigate to:</span></span>
*  [<span data-ttu-id="856c2-115">Introducción a axe Tools</span><span class="sxs-lookup"><span data-stu-id="856c2-115">axe Tools Overview</span></span>][DequeAxe]
*  [<span data-ttu-id="856c2-116">repositorio browser-compat-data</span><span class="sxs-lookup"><span data-stu-id="856c2-116">browser-compat-data repo</span></span>][MDNCompat]
*  [<span data-ttu-id="856c2-117">webhint</span><span class="sxs-lookup"><span data-stu-id="856c2-117">webhint</span></span>][webhintIo]


## <a name="open-the-issues-tool"></a><span data-ttu-id="856c2-118">Abrir la herramienta Problemas</span><span class="sxs-lookup"><span data-stu-id="856c2-118">Open the Issues tool</span></span>

<span data-ttu-id="856c2-119">Realice los pasos siguientes para abrir la **herramienta Problemas** mediante una página de demostración.</span><span class="sxs-lookup"><span data-stu-id="856c2-119">Perform the following steps to open the **Issues** tool using a demo page.</span></span>


1.  <span data-ttu-id="856c2-120">Navegue a una página web que contenga problemas que corregir.</span><span class="sxs-lookup"><span data-stu-id="856c2-120">Navigate to a webpage that contains issues to fix.</span></span>  <span data-ttu-id="856c2-121">Por ejemplo, abra la página de demostración [de pruebas de accesibilidad][A11ytestingPagewitherrors] en una nueva pestaña o ventana.</span><span class="sxs-lookup"><span data-stu-id="856c2-121">For example, open the [accessibility-testing demo page][A11ytestingPagewitherrors] in a new tab or window.</span></span>

1.  <span data-ttu-id="856c2-122">Abra DevTools.</span><span class="sxs-lookup"><span data-stu-id="856c2-122">Open DevTools.</span></span>  <span data-ttu-id="856c2-123">Después de unos segundos, aparece el **contador de** problemas \( Contador de problemas \) en la esquina superior derecha ![ de ](../media/issues-counter-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="856c2-123">After a few seconds, the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\) appears, in the upper right corner of DevTools.</span></span>  <span data-ttu-id="856c2-124">El número de problemas en el contador de problemas puede ser diferente.</span><span class="sxs-lookup"><span data-stu-id="856c2-124">The number of issues in your Issues counter might be different.</span></span>

1.  <span data-ttu-id="856c2-125">Seleccione el **contador Problemas**.</span><span class="sxs-lookup"><span data-stu-id="856c2-125">Select the **Issues counter**.</span></span>  <span data-ttu-id="856c2-126">La **herramienta Problemas** se abre con problemas agrupados en distintas categorías.</span><span class="sxs-lookup"><span data-stu-id="856c2-126">The **Issues** tool opens with issues grouped into different categories.</span></span>

    :::image type="complex" source="../media/issues-tool-categories.msft.png" alt-text="Categorías de problemas en la herramienta Problemas de la página de demostración" lightbox="../media/issues-tool-categories.msft.png":::
       <span data-ttu-id="856c2-128">Categorías de problemas en la herramienta Problemas de la página de demostración</span><span class="sxs-lookup"><span data-stu-id="856c2-128">Categories of issues in the Issues tool on the demo page</span></span>
    :::image-end:::

### <a name="other-ways-to-open-the-issues-tool"></a><span data-ttu-id="856c2-129">Otras formas de abrir la herramienta Problemas</span><span class="sxs-lookup"><span data-stu-id="856c2-129">Other ways to open the Issues tool</span></span>

<span data-ttu-id="856c2-130">Hay varias formas adicionales de abrir la **herramienta Problemas:**</span><span class="sxs-lookup"><span data-stu-id="856c2-130">There are several additional ways to open the **Issues** tool:</span></span>
*  <span data-ttu-id="856c2-131">Seleccione el **menú Más herramientas** ( ) en el panel principal o en el cajón y, a continuación, seleccione **+** \*\*\*\* **Problemas**.</span><span class="sxs-lookup"><span data-stu-id="856c2-131">Select the **More Tools** (**+**) menu in the main panel or the **Drawer**, and then select **Issues**.</span></span>
*  <span data-ttu-id="856c2-132">Seleccione **Personalizar y controlar DevTools**Más  >  **herramientas**  >  **Problemas**.</span><span class="sxs-lookup"><span data-stu-id="856c2-132">Select **Customize and control DevTools** > **More tools** > **Issues**.</span></span>
*  <span data-ttu-id="856c2-133">En el árbol DOM de la **herramienta Elementos,** seleccione y, a continuación, haga clic en un nombre de elemento `Shift` ondulado subrayado.</span><span class="sxs-lookup"><span data-stu-id="856c2-133">In the DOM tree in the **Elements** tool, select `Shift` and then click a wavy-underlined element name.</span></span>  <span data-ttu-id="856c2-134">O bien, abra el menú contextual en un elemento ondulado subrayado y, a continuación, **seleccione Ver problemas**.</span><span class="sxs-lookup"><span data-stu-id="856c2-134">Or, open the context menu on a wavy-underlined element and then select **View issues**.</span></span>

### <a name="issues-are-automatically-ordered-by-severity"></a><span data-ttu-id="856c2-135">Los problemas se ordenan automáticamente por gravedad</span><span class="sxs-lookup"><span data-stu-id="856c2-135">Issues are automatically ordered by severity</span></span>

<span data-ttu-id="856c2-136">Dentro de cada categoría de problemas, primero se enumeran los errores, después las advertencias y, a continuación, las sugerencias.</span><span class="sxs-lookup"><span data-stu-id="856c2-136">Within each category of issues, first the errors are listed, then warnings, and then tips.</span></span>

:::image type="complex" source="../media/issues-ordered-by-severity.msft.png" alt-text="La herramienta Problemas muestra problemas de rendimiento ordenados por gravedad" lightbox="../media/issues-ordered-by-severity.msft.png":::
   <span data-ttu-id="856c2-138">La **herramienta Problemas** muestra problemas de rendimiento ordenados por gravedad</span><span class="sxs-lookup"><span data-stu-id="856c2-138">The **Issues** tool displays Performance issues sorted by severity</span></span>
:::image-end:::

### <a name="include-third-party-issues"></a><span data-ttu-id="856c2-139">Incluir problemas de terceros</span><span class="sxs-lookup"><span data-stu-id="856c2-139">Include third-party issues</span></span>

<span data-ttu-id="856c2-140">Para incluir problemas causados por sitios de terceros, \*\*\*\* en la parte superior de la herramienta Problemas, active la casilla Incluir problemas **de** terceros.</span><span class="sxs-lookup"><span data-stu-id="856c2-140">To include issues that are caused by third-party sites, at the top of the **Issues** tool, select the **Include third-party issues** checkbox.</span></span>


## <a name="expand-entries-in-the-issues-tool"></a><span data-ttu-id="856c2-141">Expandir entradas en la herramienta Problemas</span><span class="sxs-lookup"><span data-stu-id="856c2-141">Expand entries in the Issues tool</span></span>

<span data-ttu-id="856c2-142">La **herramienta Problemas** presenta documentación adicional y correcciones recomendadas para aplicar a cada problema.</span><span class="sxs-lookup"><span data-stu-id="856c2-142">The **Issues** tool presents additional documentation and recommended fixes to apply to each issue.</span></span>  <span data-ttu-id="856c2-143">Para expandir un problema para obtener esta información adicional, seleccione un problema, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="856c2-143">To expand an issue to get this additional information, select an issue, as follows.</span></span>

1.  <span data-ttu-id="856c2-144">Abra la [página de demostración][A11ytestingPagewitherrors] en una nueva ventana o pestaña y, a continuación, abra DevTools.</span><span class="sxs-lookup"><span data-stu-id="856c2-144">Open the [demo page][A11ytestingPagewitherrors] in a new window or tab, and then open DevTools.</span></span>

1.  <span data-ttu-id="856c2-145">Abra la **herramienta Problemas** seleccionando el **contador Problemas** \( Contador de ![ problemas ](../media/issues-counter-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="856c2-145">Open the **Issues** tool by selecting the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\).</span></span>

1.  <span data-ttu-id="856c2-146">Seleccione un problema para expandir el problema.</span><span class="sxs-lookup"><span data-stu-id="856c2-146">Select an issue to expand the issue.</span></span>

    :::image type="complex" source="../media/issues-tool-initial-view-accessibility-page.msft.png" alt-text="La herramienta Problemas que muestra información adicional sobre cómo solucionar el problema" lightbox="../media/issues-tool-initial-view-accessibility-page.msft.png":::
       <span data-ttu-id="856c2-148">La **herramienta Problemas** que muestra información adicional sobre cómo solucionar el problema</span><span class="sxs-lookup"><span data-stu-id="856c2-148">The **Issues** tool displaying additional information on how to fix the issue</span></span>
    :::image-end:::

<span data-ttu-id="856c2-149">Cada problema mostrado tiene los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="856c2-149">Each displayed issue has the following components:</span></span>
*   <span data-ttu-id="856c2-150">Un titular que describe el problema.</span><span class="sxs-lookup"><span data-stu-id="856c2-150">A headline describing the issue.</span></span>
*   <span data-ttu-id="856c2-151">Una descripción que proporciona más contexto y soluciones propuestas.</span><span class="sxs-lookup"><span data-stu-id="856c2-151">A description providing more context and proposed solutions.</span></span>
*   <span data-ttu-id="856c2-152">Sección **RECURSOS AFECTADOS que** se vincula a recursos de DevTools, como la herramienta **Elementos,** **Orígenes** **o** Red.</span><span class="sxs-lookup"><span data-stu-id="856c2-152">An **AFFECTED RESOURCES** section that links to resources in DevTools, such as the **Elements**, **Sources**, or **Network** tool.</span></span>
*   <span data-ttu-id="856c2-153">Vínculos a documentación adicional.</span><span class="sxs-lookup"><span data-stu-id="856c2-153">Links to further documentation.</span></span>


## <a name="view-issues-in-context-of-an-associated-tool"></a><span data-ttu-id="856c2-154">Ver problemas en el contexto de una herramienta asociada</span><span class="sxs-lookup"><span data-stu-id="856c2-154">View issues in context of an associated tool</span></span>

<span data-ttu-id="856c2-155">Un problema en la **herramienta Problemas** puede incluir uno o más vínculos que abran distintas herramientas, como la **herramienta Elementos,** **Orígenes** **o** Red.</span><span class="sxs-lookup"><span data-stu-id="856c2-155">An issue in the **Issues** tool may include one or more links that open different tools, such as the **Elements**, **Sources**, or **Network** tool.</span></span> <span data-ttu-id="856c2-156">Puede abrir una de estas herramientas para realizar pasos de solución de problemas adicionales.</span><span class="sxs-lookup"><span data-stu-id="856c2-156">You can open one of these tools to perform additional troubleshooting steps.</span></span> <span data-ttu-id="856c2-157">Para abrir una herramienta vinculada desde la **herramienta Problemas,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="856c2-157">To open a linked tool from the **Issues** tool, perform the following steps.</span></span>

1.  <span data-ttu-id="856c2-158">Como se describe en la sección anterior, abra la página de demostración y, a continuación, expanda un problema en la **herramienta** Problemas.</span><span class="sxs-lookup"><span data-stu-id="856c2-158">As described in the previous section, open the demo page and then expand an issue in the **Issues** tool.</span></span>

1.  <span data-ttu-id="856c2-159">En **RECURSOS AFECTADOS**Abra  >  **en**, seleccione el nombre de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="856c2-159">In **AFFECTED RESOURCES** > **Open in**, select the tool name.</span></span>  <span data-ttu-id="856c2-160">El recurso afectado se muestra en la herramienta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="856c2-160">The affected resource is displayed in the selected tool.</span></span>

    :::image type="complex" source="../media/issues-tool-affected-resource-opens-elements-tool.msft.png" alt-text="Seleccionar una herramienta para abrir un recurso afectado desde dentro de la herramienta Problemas" lightbox="../media/issues-tool-affected-resource-opens-elements-tool.msft.png":::
       <span data-ttu-id="856c2-162">Seleccionar una herramienta para abrir un recurso afectado desde dentro de la herramienta Problemas</span><span class="sxs-lookup"><span data-stu-id="856c2-162">Select a tool to open an affected resource from within the Issues tool</span></span>
    :::image-end:::

    <span data-ttu-id="856c2-163">Un problema expandido puede tener un **vínculo Red** para mostrar el recurso afectado en la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="856c2-163">An expanded issue may have a **Network** link, to display the affected resource in the **Network** tool.</span></span>

    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="La herramienta Red se abre al seleccionar un vínculo de recurso Red" lightbox="../media/issues-tab-view-issue.msft.png":::
    <span data-ttu-id="856c2-165">La **herramienta Red** se abre al seleccionar un vínculo de **recurso** Red</span><span class="sxs-lookup"><span data-stu-id="856c2-165">The **Network** tool opens when you select a **Network** resource link</span></span>
    :::image-end:::


## <a name="open-issues-from-the-dom-tree"></a><span data-ttu-id="856c2-166">Abrir problemas desde el árbol DOM</span><span class="sxs-lookup"><span data-stu-id="856c2-166">Open issues from the DOM tree</span></span>

<span data-ttu-id="856c2-167">Si un elemento tiene un problema asociado, el árbol DOM de la **herramienta Elementos** muestra un subrayado ondulado bajo el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="856c2-167">If an element has an associated issue, the DOM tree in the **Elements** tool shows a wavy underline under the element name.</span></span>  <span data-ttu-id="856c2-168">Puede abrir el menú contextual (hacer clic con el botón secundario) en el elemento y, a continuación, seleccionar Ver problemas **o**seleccionar y hacer clic izquierdo en el elemento con el `Shift` subrayado ondulado.</span><span class="sxs-lookup"><span data-stu-id="856c2-168">You can open the context menu (right-click) on the element and then select **View issues**, or select `Shift` and left-click the element with the wavy underline.</span></span>

<span data-ttu-id="856c2-169">Para mostrar un problema para los elementos con subrayados ondulados en el árbol DOM, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="856c2-169">To display an issue for elements with wavy underlines in the DOM tree, perform the following steps.</span></span>

1.  <span data-ttu-id="856c2-170">Abra una página, como la página [de demostración,][A11ytestingPagewitherrors]en una nueva pestaña o ventana.</span><span class="sxs-lookup"><span data-stu-id="856c2-170">Open a page, such as the [demo page][A11ytestingPagewitherrors], in a new tab or window.</span></span>

1.  <span data-ttu-id="856c2-171">Abra DevTools y, a continuación, seleccione la **pestaña** Elementos.</span><span class="sxs-lookup"><span data-stu-id="856c2-171">Open DevTools and then select the **Elements** tab.</span></span>

1.  <span data-ttu-id="856c2-172">En el árbol DOM, expanda `<body>`  >  `<header>`  >  `<form>` .</span><span class="sxs-lookup"><span data-stu-id="856c2-172">In the DOM tree, expand `<body>` > `<header>` > `<form>`.</span></span>  <span data-ttu-id="856c2-173">Observe que el `<input>` elemento tiene un subrayado ondulado.</span><span class="sxs-lookup"><span data-stu-id="856c2-173">Notice that the `<input>` element has a wavy underline.</span></span>

    :::image type="complex" source="../media/issues-wavy-underlines-dom-tree.msft.png" alt-text="Problemas con subrayado ondulado en el árbol DOM de la herramienta Elementos" lightbox="../media/issues-wavy-underlines-dom-tree.msft.png":::
       <span data-ttu-id="856c2-175">Problemas con subrayado ondulado en el **árbol DOM** de la **herramienta** Elementos</span><span class="sxs-lookup"><span data-stu-id="856c2-175">Wavy-underlined issues in the **DOM tree** in the **Elements** tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="856c2-176">Mantenga el mouse sobre el `<input>` elemento.</span><span class="sxs-lookup"><span data-stu-id="856c2-176">Hover over the `<input>` element.</span></span>  <span data-ttu-id="856c2-177">Una información sobre herramientas muestra información sobre el problema.</span><span class="sxs-lookup"><span data-stu-id="856c2-177">A tooltip displays information about the issue.</span></span>

1.  <span data-ttu-id="856c2-178">Abra el menú contextual del elemento con el subrayado ondulado y, a continuación, **seleccione Ver problemas**.</span><span class="sxs-lookup"><span data-stu-id="856c2-178">Open the context menu on the element with the wavy underline, and then select **View issues**.</span></span>  <span data-ttu-id="856c2-179">La **herramienta** Problemas se abre y muestra el problema asociado con ese elemento.</span><span class="sxs-lookup"><span data-stu-id="856c2-179">The **Issues** tool opens and displays the issue that's associated with that element.</span></span>

    :::image type="complex" source="../media/issues-opened-from-dom-tree-wavy-underline.msft.png" alt-text="Detalles sobre los problemas de un elemento ondulado subrayado en el árbol DOM" lightbox="../media/issues-opened-from-dom-tree-wavy-underline.msft.png":::
       <span data-ttu-id="856c2-181">Detalles sobre los problemas de un elemento ondulado subrayado en el **árbol DOM**</span><span class="sxs-lookup"><span data-stu-id="856c2-181">Details about issues on a wavy-underlined element in the **DOM tree**</span></span>
    :::image-end:::


## <a name="see-also"></a><span data-ttu-id="856c2-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="856c2-182">See also</span></span>

* [<span data-ttu-id="856c2-183">Probar automáticamente una página web para problemas de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="856c2-183">Automatically test a webpage for accessibility issues</span></span>](../accessibility/test-issues-tool.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="856c2-184">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="856c2-184">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]

<!-- links -->
[DevtoolsOpenIndex]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"
<!-- external links -->
[A11ytestingPagewitherrors]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página de demostración de pruebas de accesibilidad | Microsoft Docs"
[DequeAxe]: https://www.deque.com/axe "Axe Tools Overview | Deque"
[MDNCompat]: https://github.com/mdn/browser-compat-data "Datos de compatibilidad del explorador MDN | GitHub"
[webhintIo]: https://webhint.io "webhint.io"

> [!NOTE]
> <span data-ttu-id="856c2-190">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="856c2-190">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>
> <span data-ttu-id="856c2-191">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/issues/index) y es creado por [Sam Dutton][SamDutton] \(Developer Advocate\).</span><span class="sxs-lookup"><span data-stu-id="856c2-191">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>
<span data-ttu-id="856c2-192">[ ![ Creative Commons License][CCby4Image]][CCA4IL] Este trabajo se concede bajo una licencia de Creative Commons [Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="856c2-192">[![Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton

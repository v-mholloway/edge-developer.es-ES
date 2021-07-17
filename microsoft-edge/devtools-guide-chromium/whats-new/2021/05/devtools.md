---
description: El botón Más herramientas, documentación en contexto para empezar a usar la extensión DevTools, mayor compatibilidad para lectores de pantalla en la consola y mucho más.
title: Novedades de DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 09e1438ae7fd6547a7dd14757f54f370c9008773
ms.sourcegitcommit: 1dd6376784c394087fe2938acaa069212cf7656e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2021
ms.locfileid: "11659431"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a><span data-ttu-id="f83a4-104">Novedades de DevTools (Microsoft Edge 92)</span><span class="sxs-lookup"><span data-stu-id="f83a4-104">What's New In DevTools (Microsoft Edge 92)</span></span>

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]

> [!TIP]
> <span data-ttu-id="f83a4-105">La **conferencia de Microsoft Build 2021** fue del 25 al 27 de mayo.</span><span class="sxs-lookup"><span data-stu-id="f83a4-105">The **Microsoft Build 2021** conference was on May 25-27.</span></span>  <span data-ttu-id="f83a4-106">Este es un vídeo de Build about the updates to DevTools: [Microsoft Edge | Estado de la plataforma:][YoutubeEdgeStateOfThePlatform] Microsoft Edge una plataforma atractiva y coherente con herramientas para desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="f83a4-106">Here's a video from Build about the updates to DevTools: [Microsoft Edge | State of the Platform][YoutubeEdgeStateOfThePlatform] - Microsoft Edge brings a compelling and consistent platform with tools for developers.</span></span>  <span data-ttu-id="f83a4-107">A medida que nuestros exploradores heredados no sean compatibles, Edge pronto será el único explorador compatible de Microsoft en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f83a4-107">As our legacy browsers phase out of support, Edge will soon be the only supported browser from Microsoft on Windows 10.</span></span>  <span data-ttu-id="f83a4-108">Únase a nosotros para obtener información sobre lo último en la plataforma perimetral, las herramientas y las aplicaciones web.</span><span class="sxs-lookup"><span data-stu-id="f83a4-108">Join us to learn about the latest across the Edge platform, tools, and web apps.</span></span>


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a><span data-ttu-id="f83a4-109">El botón Cerrar ya no está oculto cuando DevTools es estrecho</span><span class="sxs-lookup"><span data-stu-id="f83a4-109">The Close button is no longer hidden when DevTools is narrow</span></span>

<!-- Title: DevTools is now easier to close -->
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->

<span data-ttu-id="f83a4-110">En Microsoft Edge versión 91 o anterior, el botón Cerrar para cerrar DevTools no se muestra cuando la ventanilla de DevTools es estrecha. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f83a4-110">In Microsoft Edge version 91 or earlier, the **Close** button to close DevTools isn't displayed when the DevTools viewport is narrow.</span></span>  <span data-ttu-id="f83a4-111">En Microsoft Edge versión 92, \*\*\*\* el botón Cerrar de DevTools siempre está presente, independientemente del ancho de la ventanilla de DevTools.</span><span class="sxs-lookup"><span data-stu-id="f83a4-111">In Microsoft Edge version 92, the **Close** button in the DevTools is always present, regardless of the DevTools viewport width.</span></span>

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="El botón Cerrar DevTools ahora está presente incluso cuando la ventanilla es estrecha" lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   <span data-ttu-id="f83a4-113">El **botón Cerrar** DevTools ahora está presente incluso cuando la ventanilla es estrecha</span><span class="sxs-lookup"><span data-stu-id="f83a4-113">The **Close** DevTools button is now present even when the viewport is narrow</span></span>
:::image-end:::


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a><span data-ttu-id="f83a4-114">Agregar herramientas rápidamente con el nuevo botón Más herramientas</span><span class="sxs-lookup"><span data-stu-id="f83a4-114">Add tools quickly with the new More Tools button</span></span>

<!-- Title: Add tools quickly with the new More Tools button -->
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->

<span data-ttu-id="f83a4-115">Hay una nueva forma de abrir más herramientas en Microsoft Edge DevTools: el **menú Más herramientas** ( ) `+` .</span><span class="sxs-lookup"><span data-stu-id="f83a4-115">There's a new way to open more tools in Microsoft Edge DevTools: the **More Tools** (`+`) menu.</span></span> <span data-ttu-id="f83a4-116">El **menú Más herramientas** aparece en la barra de herramientas del panel principal y en la barra de herramientas del cajón.</span><span class="sxs-lookup"><span data-stu-id="f83a4-116">The **More Tools** menu appears on the toolbar in the main panel and on the toolbar of the drawer.</span></span> <span data-ttu-id="f83a4-117">Al seleccionar una herramienta en el **menú Más herramientas,** se agrega la herramienta a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f83a4-117">Selecting a tool from the **More Tools** menu adds the tool to the toolbar.</span></span>

<span data-ttu-id="f83a4-118">Para reordenar las pestañas de cualquiera de las barras de herramientas, seleccione y arrastre las pestañas.</span><span class="sxs-lookup"><span data-stu-id="f83a4-118">To reorder the tabs on either toolbar, select and drag the tabs.</span></span>

<span data-ttu-id="f83a4-119">El **menú Más herramientas** estaba disponible como un experimento en Microsoft Edge versión 89 y ahora siempre está presente.</span><span class="sxs-lookup"><span data-stu-id="f83a4-119">The **More Tools** menu was available as an experiment in Microsoft Edge version 89, and is now always present.</span></span>

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="El botón Más herramientas de la barra de herramientas superior y la barra de herramientas del cajón" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   <span data-ttu-id="f83a4-121">El **botón Más herramientas** de la barra de herramientas superior y la barra de herramientas del cajón</span><span class="sxs-lookup"><span data-stu-id="f83a4-121">The **More Tools** button on the upper toolbar and drawer toolbar</span></span>
:::image-end:::

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="Menú Más herramientas" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   <span data-ttu-id="f83a4-123">Menú **Más** herramientas</span><span class="sxs-lookup"><span data-stu-id="f83a4-123">The **More Tools** menu</span></span>
:::image-end:::


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a><span data-ttu-id="f83a4-124">Mejoras para activar, seleccionar y cerrar herramientas</span><span class="sxs-lookup"><span data-stu-id="f83a4-124">Improvements for hovering, selecting, and closing tools</span></span>

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

<span data-ttu-id="f83a4-125">Las pestañas de cada herramienta se han reformateado para reducir la posibilidad de cerrar accidentalmente una herramienta.</span><span class="sxs-lookup"><span data-stu-id="f83a4-125">Tabs for each tool have been reformatted to reduce the chance of accidentally closing a tool.</span></span>  <span data-ttu-id="f83a4-126">En cada pestaña de la barra de herramientas principal y en la barra de herramientas del cajón, agregamos:</span><span class="sxs-lookup"><span data-stu-id="f83a4-126">On each tab in the main toolbar and in the toolbar of the drawer, we added:</span></span>
*  <span data-ttu-id="f83a4-127">Espaciado alrededor de la pestaña.</span><span class="sxs-lookup"><span data-stu-id="f83a4-127">Spacing around the tab.</span></span>
*  <span data-ttu-id="f83a4-128">Espaciado alrededor del botón cerrar ( `x` ) de la ficha.</span><span class="sxs-lookup"><span data-stu-id="f83a4-128">Spacing around the close (`x`) button in the tab.</span></span>
*  <span data-ttu-id="f83a4-129">Color de fondo al pasar el mouse sobre la pestaña.</span><span class="sxs-lookup"><span data-stu-id="f83a4-129">A background color when hovering over the tab.</span></span>
*  <span data-ttu-id="f83a4-130">Información sobre herramientas para el botón cerrar ( `x` ) de la pestaña.</span><span class="sxs-lookup"><span data-stu-id="f83a4-130">A tooltip for the close (`x`) button of the tab.</span></span>
*  <span data-ttu-id="f83a4-131">Contraste superior para el botón cerrar ( `x` ) de la ficha.</span><span class="sxs-lookup"><span data-stu-id="f83a4-131">Higher contrast for the close (`x`) button of the tab.</span></span>

<span data-ttu-id="f83a4-132">Por ejemplo, cuando estás \*\*\*\* en la herramienta \*\*\*\* Rendimiento y mantienes el mouse sobre la pestaña de la herramienta Red, estas mejoras ayudan a evitar el cierre accidental de la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="f83a4-132">For example, when you are in the **Performance** tool and you hover over the **Network** tool's tab, these improvements help prevent accidentally closing the **Network** tool.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Pestañas antes de reformatear" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           <span data-ttu-id="f83a4-134">Pestañas antes de reformatear</span><span class="sxs-lookup"><span data-stu-id="f83a4-134">Tabs before reformatting</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Pestañas después de la reformateado" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           <span data-ttu-id="f83a4-136">Pestañas después de la reformateado</span><span class="sxs-lookup"><span data-stu-id="f83a4-136">Tabs after reformatting</span></span> :::image-end:::
    :::column-end:::
:::row-end:::

<span data-ttu-id="f83a4-137">Estas mejoras son especialmente relevantes para los usuarios de DevTools localizados, en los que las pestañas pueden ser más estrechas y fáciles de cerrar accidentalmente.</span><span class="sxs-lookup"><span data-stu-id="f83a4-137">These improvements are especially relevant for users of localized DevTools, in which the tabs may be narrower and easier to accidentally close.</span></span>

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="Localized DevTools con pestañas estrechas" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   <span data-ttu-id="f83a4-139">Localized DevTools con pestañas estrechas</span><span class="sxs-lookup"><span data-stu-id="f83a4-139">Localized DevTools with narrow tabs</span></span>
:::image-end:::

<span data-ttu-id="f83a4-140">También facilitamos volver a agregar una herramienta que ha cerrado agregando un menú Más herramientas [a](#add-tools-quickly-with-the-new-more-tools-button) la barra de herramientas principal y la barra de herramientas del cajón.</span><span class="sxs-lookup"><span data-stu-id="f83a4-140">We also made it easier to re-add a tool that you closed by adding a [More Tools menu](#add-tools-quickly-with-the-new-more-tools-button) to the main toolbar and drawer toolbar.</span></span>


## <a name="better-support-for-screen-readers-in-the-console"></a><span data-ttu-id="f83a4-141">Mejor compatibilidad con lectores de pantalla en la consola</span><span class="sxs-lookup"><span data-stu-id="f83a4-141">Better support for screen readers in the Console</span></span>

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

<span data-ttu-id="f83a4-142">Antes de Microsoft Edge versión 92, en la **Consola,** las tecnologías de asistencia, como los lectores de pantalla, no anunciaban sugerencias de autocompletar ni los resultados de las expresiones evaluadas.</span><span class="sxs-lookup"><span data-stu-id="f83a4-142">Prior to Microsoft Edge version 92, in the **Console**, assistive technologies such as screen readers didn't announce autocomplete suggestions or the results of evaluated expressions.</span></span> <span data-ttu-id="f83a4-143">Esto se ha corregido ahora.</span><span class="sxs-lookup"><span data-stu-id="f83a4-143">This has been fixed now.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="En la consola, los lectores de pantalla ahora anuncian la sugerencia de autocompletar seleccionada actualmente" lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           <span data-ttu-id="f83a4-145">En la **Consola,** los lectores de pantalla ahora anuncian la sugerencia de autocompletar seleccionada actualmente</span><span class="sxs-lookup"><span data-stu-id="f83a4-145">In the **Console**, screen readers now announce the currently selected autocomplete suggestion</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="En la consola, los lectores de pantalla ahora anuncian el resultado de una expresión evaluada" lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           <span data-ttu-id="f83a4-147">En la **consola,** ahora los lectores de pantalla anuncian el resultado de una expresión evaluada</span><span class="sxs-lookup"><span data-stu-id="f83a4-147">In the **Console**, screen readers now announce the result of an evaluated expression</span></span> :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="source-order-viewer"></a><span data-ttu-id="f83a4-148">Visor de pedidos de origen</span><span class="sxs-lookup"><span data-stu-id="f83a4-148">Source Order Viewer</span></span>

<!--  Title: Source Order Viewer -->
<!--  Subtitle: The new Source Order Viewer displays numbers on the webpage indicating the order of page elements in the source file, independently of how the page sections are positioned by CSS. -->

<span data-ttu-id="f83a4-149">Ahora puede ver el orden de los elementos de origen sobrelaidos en la página web representada, para una mejor inspección de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="f83a4-149">You can now view the order of source elements overlaid on the rendered webpage, for better accessibility inspection.</span></span>

<span data-ttu-id="f83a4-150">El orden del contenido de un documento HTML es importante para la optimización y accesibilidad del motor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f83a4-150">The order of content in an HTML document is important for search engine optimization and accessibility.</span></span>  <span data-ttu-id="f83a4-151">CSS permite a los desarrolladores crear contenido que tiene un aspecto diferente en su orden en pantalla que el orden en el documento de origen HTML.</span><span class="sxs-lookup"><span data-stu-id="f83a4-151">CSS allows developers to create content that looks different in its on-screen order than the order in the HTML source document.</span></span>  <span data-ttu-id="f83a4-152">Se trata de un problema de accesibilidad, ya que los usuarios lectores de pantalla podrían obtener una experiencia confusa.</span><span class="sxs-lookup"><span data-stu-id="f83a4-152">This is an accessibility problem, because screen-reader users could get a confusing experience.</span></span>

:::image type="complex" source="../../media/2021/05/source-order-viewer.msft.png" alt-text="Al activar el Visor de pedidos de origen, se muestra el orden de los elementos del origen como superposiciones en la página" lightbox="../../media/2021/05/source-order-viewer.msft.png":::
   <span data-ttu-id="f83a4-154">Al activar el **Visor de pedidos de origen,** se muestra el orden de los elementos del origen como superposiciones en la página</span><span class="sxs-lookup"><span data-stu-id="f83a4-154">Activating the **Source Order Viewer** shows the order of the elements in the source as overlays on the page</span></span>
:::image-end:::

<span data-ttu-id="f83a4-155">Para obtener más información, vaya a Probar compatibilidad [con teclado mediante el Visor de pedidos de origen](../../../accessibility/test-tab-key-source-order-viewer.md).</span><span class="sxs-lookup"><span data-stu-id="f83a4-155">For more information, navigate to [Test keyboard support using the Source Order Viewer](../../../accessibility/test-tab-key-source-order-viewer.md).</span></span>

<span data-ttu-id="f83a4-156">Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1094406][CR1094406].</span><span class="sxs-lookup"><span data-stu-id="f83a4-156">To review the history of this feature in the Chromium open-source project, navigate to Issue [1094406][CR1094406].</span></span>


## <a name="user-agent-client-hints-for-devices-in-the-network-conditions-tab"></a><span data-ttu-id="f83a4-157">User-Agent sugerencias de cliente para dispositivos en la pestaña Condiciones de red</span><span class="sxs-lookup"><span data-stu-id="f83a4-157">User-Agent Client Hints for devices in the Network conditions tab</span></span>

<!--  Title: User-Agent Client Hints -->
<!--  Subtitle: Access information about a user's browser in an ergonomic way that preserves privacy. -->

<span data-ttu-id="f83a4-158">User-Agent sugerencias de cliente se aplican ahora para dispositivos en el **campo Agente** de usuario de la herramienta **Condiciones de** red.</span><span class="sxs-lookup"><span data-stu-id="f83a4-158">User-Agent Client Hints are now applied for devices in the **User agent** field in the **Network conditions** tool.</span></span>  <span data-ttu-id="f83a4-159">User-Agent sugerencias de cliente son una nueva expansión de la API de sugerencias de cliente que le permite tener acceso a información sobre el explorador de un usuario de una forma ergonómica que preserva la privacidad.</span><span class="sxs-lookup"><span data-stu-id="f83a4-159">User-Agent Client Hints are a new expansion to the Client Hints API that enables you to access information about a user's browser in an ergonomic way that preserves privacy.</span></span>

:::image type="complex" source="../../media/2021/05/user-agent.msft.png" alt-text="Agente de usuario" lightbox="../../media/2021/05/user-agent.msft.png":::
   <span data-ttu-id="f83a4-161">Agente de usuario</span><span class="sxs-lookup"><span data-stu-id="f83a4-161">User agent</span></span>
:::image-end:::

<span data-ttu-id="f83a4-162">Para obtener más información, vaya a [Sugerencias de cliente de agente de usuario](../../../../web-platform/user-agent-guidance.md#user-agent-client-hints).</span><span class="sxs-lookup"><span data-stu-id="f83a4-162">For more information, navigate to [User-Agent Client Hints](../../../../web-platform/user-agent-guidance.md#user-agent-client-hints).</span></span>

<span data-ttu-id="f83a4-163">Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya a Problema [1174299][CR1174299].</span><span class="sxs-lookup"><span data-stu-id="f83a4-163">To review the history of this feature in the Chromium open-source project, navigate to Issue [1174299][CR1174299].</span></span>


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a><span data-ttu-id="f83a4-164">Microsoft Edge Developer Tools para Visual Studio Code versión 1.1.8</span><span class="sxs-lookup"><span data-stu-id="f83a4-164">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.8</span></span>

<span data-ttu-id="f83a4-165">El [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.8 for Microsoft Visual Studio Code tiene los siguientes cambios desde la versión anterior.</span><span class="sxs-lookup"><span data-stu-id="f83a4-165">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.8 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="f83a4-166">Microsoft Visual Studio Code actualiza las extensiones automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f83a4-166">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="f83a4-167">Para actualizar manualmente a la versión 1.1.8, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="f83a4-167">To manually update to version 1.1.8, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>

<span data-ttu-id="f83a4-168">Puede presentar problemas y contribuir a la extensión en [vscode-edge-devtools GitHub repositorio][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="f83a4-168">You can file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a><span data-ttu-id="f83a4-169">Documentación e interfaz de usuario en contexto para facilitar el uso de la extensión DevTools</span><span class="sxs-lookup"><span data-stu-id="f83a4-169">In-context documentation and UI to make it easier to use the DevTools extension</span></span>

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->

<span data-ttu-id="f83a4-170">La versión 1.1.8 de la extensión [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] ahora presenta una forma más sencilla de iniciar una nueva instancia de Microsoft Edge, presentando instrucciones, botones, vínculos y una página de documentación que le guiará.</span><span class="sxs-lookup"><span data-stu-id="f83a4-170">Version 1.1.8 of the [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension now features a simpler way to start a new instance of Microsoft Edge, by presenting instructions, buttons, links, and a documentation page to guide you.</span></span>

*  <span data-ttu-id="f83a4-171">Cuando selecciona el botón herramientas de \*\*\*\* **Microsoft Edge** en la barra de actividades de Visual Studio Code, el panel Herramientas de **Microsoft Edge:** Destinos ahora presenta texto explicativo, botones y vínculos para guiarlo, en lugar de un panel en blanco.</span><span class="sxs-lookup"><span data-stu-id="f83a4-171">When you select the **Microsoft Edge Tools** button in the **Activity Bar** of Visual Studio Code, the **Microsoft Edge Tools: Targets** panel now presents explanatory text, buttons, and links to guide you, instead of a blank panel.</span></span>

*  <span data-ttu-id="f83a4-172">Al abrir una nueva instancia de Microsoft Edge desde dentro de Visual Studio Code, Microsoft Edge muestra ahora una página de inicio que explica cómo usar la extensión Herramientas de desarrollo, en lugar de una página en blanco.</span><span class="sxs-lookup"><span data-stu-id="f83a4-172">When you open a new instance of Microsoft Edge from within Visual Studio Code, Microsoft Edge now shows a start page that explains how to use the Developer Tools extension, instead of a blank page.</span></span>

*  <span data-ttu-id="f83a4-173">El **panel herramientas Microsoft Edge:** destinos ahora tiene un botón Generar **launch.jsen** y las instrucciones, para ayudar a iniciar el proyecto para la depuración en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f83a4-173">The **Microsoft Edge Tools: Targets** panel now has a **Generate launch.json** button and instructions, to help launch your project for debugging in Microsoft Edge.</span></span>

<span data-ttu-id="f83a4-174">Para obtener más información, vaya [a Uso de las herramientas][GithubIoDevToolsUsing].</span><span class="sxs-lookup"><span data-stu-id="f83a4-174">For more information, navigate to [Using the tools][GithubIoDevToolsUsing].</span></span>


## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="f83a4-175">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="f83a4-175">Announcements from the Chromium project</span></span>

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]


### <a name="css-grid-editor"></a><span data-ttu-id="f83a4-176">Editor de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="f83a4-176">CSS Grid editor</span></span>

<span data-ttu-id="f83a4-177">Ahora puede obtener una vista previa y crear diseños de cuadrícula CSS con el nuevo editor de cuadrícula CSS.</span><span class="sxs-lookup"><span data-stu-id="f83a4-177">You can now preview and author CSS Grid layouts, using the new CSS Grid editor.</span></span>

<span data-ttu-id="f83a4-178">Cuando un elemento HTML de la página tiene o se ha aplicado, se muestra un icono de cuadrícula junto a él en la pestaña Estilos. Haga clic en el icono de cuadrícula para mostrar u ocultar el editor de cuadrícula `display: grid` `display: inline-grid` CSS. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f83a4-178">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a grid icon is displayed next to it in the **Styles** tab. Click the grid icon to display or hide the CSS grid editor.</span></span> <span data-ttu-id="f83a4-179">En el editor de cuadrículas CSS, seleccione cualquiera de los iconos (por ejemplo) para obtener una vista previa del `justify-content: space-around` diseño en la página representada.</span><span class="sxs-lookup"><span data-stu-id="f83a4-179">In the CSS grid editor, select any of the icons (such as `justify-content: space-around`) to preview the layout in the rendered page.</span></span>  <span data-ttu-id="f83a4-180">El diseño de Flex funciona de forma similar.</span><span class="sxs-lookup"><span data-stu-id="f83a4-180">Flex layout works similarly.</span></span>

:::image type="complex" source="../../media/2021/05/css-grid-editor.msft.png" alt-text="Editor de cuadrícula CSS" lightbox="../../media/2021/05/css-grid-editor.msft.png":::
   <span data-ttu-id="f83a4-182">Editor de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="f83a4-182">CSS Grid editor</span></span>
:::image-end:::

<!-- screenshot uses https://jec.fyi -->

<span data-ttu-id="f83a4-183">Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1203241][CR1203241].</span><span class="sxs-lookup"><span data-stu-id="f83a4-183">To review the history of this feature in the Chromium open-source project, navigate to Issue [1203241][CR1203241].</span></span>


### <a name="support-for-const-redeclarations-in-the-console"></a><span data-ttu-id="f83a4-184">Compatibilidad con las declaraciones de const en la consola</span><span class="sxs-lookup"><span data-stu-id="f83a4-184">Support for const redeclarations in the Console</span></span>

<span data-ttu-id="f83a4-185">La consola ahora admite la reeclaración de variables en scripts REPL independientes (por ejemplo, cuando se ejecuta una instrucción en la consola), además de las `const` `let` declaraciones existentes y `class` redeclarations.</span><span class="sxs-lookup"><span data-stu-id="f83a4-185">The Console now supports redeclaration of `const` variables across separate REPL scripts (such as when you run a statement in the Console), in addition to the existing `let` and `class` redeclarations.</span></span>  <span data-ttu-id="f83a4-186">Esta compatibilidad permite experimentar con diferentes declaraciones para `const` variables sin actualizar la página.</span><span class="sxs-lookup"><span data-stu-id="f83a4-186">This support allows you to experiment with different declarations for `const` variables without refreshing the page.</span></span>  <span data-ttu-id="f83a4-187">Anteriormente, DevTools generaba un error de sintaxis si se declaraba de nuevo un `const` enlace.</span><span class="sxs-lookup"><span data-stu-id="f83a4-187">Previously, DevTools threw a syntax error if you redeclared a `const` binding.</span></span>

<span data-ttu-id="f83a4-188">Consulte el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="f83a4-188">Refer to the example below.</span></span> `const` <span data-ttu-id="f83a4-189">La nueva declaración se admite en scripts REPL independientes (consulte variable `a` ).</span><span class="sxs-lookup"><span data-stu-id="f83a4-189">redeclaration is supported across separate REPL scripts (refer to variable `a`).</span></span>  <span data-ttu-id="f83a4-190">Tenga en cuenta que los siguientes escenarios no son compatibles con el diseño:</span><span class="sxs-lookup"><span data-stu-id="f83a4-190">Note that the following scenarios are not supported, by design:</span></span>

*  `const` <span data-ttu-id="f83a4-191">No se permite la reeclaración de scripts de página en scripts REPL.</span><span class="sxs-lookup"><span data-stu-id="f83a4-191">redeclaration of page scripts is not allowed in REPL scripts.</span></span>
*  `const` <span data-ttu-id="f83a4-192">No se permite la reeclaración dentro del mismo script REPL (consulte variable `b` ).</span><span class="sxs-lookup"><span data-stu-id="f83a4-192">redeclaration within the same REPL script is not allowed (refer to variable `b`).</span></span>

:::image type="complex" source="../../media/2021/05/support-for-const-redeclaration.msft.png" alt-text="Se permite la declaración de una variable const en la consola" lightbox="../../media/2021/05/support-for-const-redeclaration.msft.png":::
   <span data-ttu-id="f83a4-194">Se permite la declaración de una variable const en la consola</span><span class="sxs-lookup"><span data-stu-id="f83a4-194">Redeclaring a const variable is allowed in the console</span></span>
:::image-end:::

<span data-ttu-id="f83a4-195">Para obtener información sobre cómo ejecutar un solo script REPL o un script REPL de varias líneas, vaya a La consola como [un entorno JavaScript](../../../console/console-javascript.md).</span><span class="sxs-lookup"><span data-stu-id="f83a4-195">To learn how to run a single REPL script or a multi-line REPL script, navigate to [The Console as a JavaScript environment](../../../console/console-javascript.md).</span></span>
    
<span data-ttu-id="f83a4-196">Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1076427][CR1076427].</span><span class="sxs-lookup"><span data-stu-id="f83a4-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1076427][CR1076427].</span></span>


### <a name="new-shortcut-to-view-iframe-details"></a><span data-ttu-id="f83a4-197">Nuevo acceso directo para ver detalles de iframe</span><span class="sxs-lookup"><span data-stu-id="f83a4-197">New shortcut to view iframe details</span></span>

<span data-ttu-id="f83a4-198">Para ver rápidamente los detalles, ahora puede hacer clic con el botón secundario en un elemento de la herramienta Elementos y, a `iframe` continuación, seleccionar Mostrar detalles de `iframe` **iframe** \*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="f83a4-198">To quickly view `iframe` details, you can now right-click an `iframe` element in the **Elements** tool, and then select **Show iframe details**.</span></span>

:::image type="complex" source="../../media/2021/05/show-iframe-details.msft.png" alt-text="Vista de detalles de iframe" lightbox="../../media/2021/05/show-iframe-details.msft.png":::
   <span data-ttu-id="f83a4-200">Vista de detalles de iframe</span><span class="sxs-lookup"><span data-stu-id="f83a4-200">iframe details view</span></span>
:::image-end:::

<span data-ttu-id="f83a4-201">Esto muestra los detalles acerca de `iframe` la herramienta **Aplicación.**</span><span class="sxs-lookup"><span data-stu-id="f83a4-201">This displays the details about the `iframe` in the **Application** tool.</span></span>  <span data-ttu-id="f83a4-202">En la **herramienta Aplicación,** puede examinar los detalles del documento, el estado de seguridad y aislamiento, la directiva de permisos y mucho más para depurar posibles problemas.</span><span class="sxs-lookup"><span data-stu-id="f83a4-202">In the **Application** tool, you can examine document details, security and isolation status, permissions policy, and more, to debug potential issues.</span></span>

:::image type="complex" source="../../media/2021/05/show-iframe-details-application-tool.msft.png" alt-text="Detalles del marco en la herramienta Aplicación" lightbox="../../media/2021/05/show-iframe-details-application-tool.msft.png":::
   <span data-ttu-id="f83a4-204">Detalles del marco en la **herramienta Aplicación**</span><span class="sxs-lookup"><span data-stu-id="f83a4-204">Frame details in the **Application** tool</span></span>
:::image-end:::

<!-- demo page: https://wolfib.github.io/web-demos/ esp https://wolfib.github.io/web-demos/jsIframe.html -->

<span data-ttu-id="f83a4-205">Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1192084][CR1192084].</span><span class="sxs-lookup"><span data-stu-id="f83a4-205">To review the history of this feature in the Chromium open-source project, navigate to Issue [1192084][CR1192084].</span></span>


### <a name="enhanced-cors-debugging-support"></a><span data-ttu-id="f83a4-206">Compatibilidad con depuración CORS mejorada</span><span class="sxs-lookup"><span data-stu-id="f83a4-206">Enhanced CORS debugging support</span></span>

<span data-ttu-id="f83a4-207">Los errores de uso compartido de recursos entre orígenes (CORS) ahora se encuentran en la **pestaña** Problemas.  Existen varias causas potenciales de errores CORS.</span><span class="sxs-lookup"><span data-stu-id="f83a4-207">Cross-origin resource sharing (CORS) errors are now surfaced in the **Issues** tab.  There are various potential causes of CORS errors.</span></span>  <span data-ttu-id="f83a4-208">Haga clic para expandir cada problema para comprender las posibles causas y soluciones.</span><span class="sxs-lookup"><span data-stu-id="f83a4-208">Click to expand each issue to understand the potential causes and solutions.</span></span>

:::image type="complex" source="../../media/2021/05/cors-debugging-support.msft.png" alt-text="Problemas de CORS en la pestaña Problemas" lightbox="../../media/2021/05/cors-debugging-support.msft.png":::
   <span data-ttu-id="f83a4-210">Problemas de CORS en la pestaña Problemas</span><span class="sxs-lookup"><span data-stu-id="f83a4-210">CORS issues in the Issues tab</span></span>
:::image-end:::

<!-- screenshot uses http://cors-errors.glitch.me -->

<span data-ttu-id="f83a4-211">Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1141824][CR1141824].</span><span class="sxs-lookup"><span data-stu-id="f83a4-211">To review the history of this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>


### <a name="renamed-xhr-filter-to-fetchxhr"></a><span data-ttu-id="f83a4-212">Filtro XHR con nombre a Fetch\/XHR</span><span class="sxs-lookup"><span data-stu-id="f83a4-212">Renamed XHR filter to Fetch\/XHR</span></span>

<span data-ttu-id="f83a4-213">En la **herramienta Red,** el filtro **XHR** ahora se cambia a **Fetch/XHR**.</span><span class="sxs-lookup"><span data-stu-id="f83a4-213">In the **Network** tool, the **XHR** filter is now renamed to **Fetch/XHR**.</span></span> <span data-ttu-id="f83a4-214">Este cambio hace que sea más claro que este filtro incluye tanto solicitudes de red `XMLHttpRequest` de API como de `Fetch` API.</span><span class="sxs-lookup"><span data-stu-id="f83a4-214">This change makes it clearer that this filter includes both `XMLHttpRequest` and `Fetch` API network requests.</span></span>

:::image type="complex" source="../../media/2021/05/fetch-xhr.msft.png" alt-text="La herramienta Red ahora muestra Fetch/XHR en lugar de XHR" lightbox="../../media/2021/05/fetch-xhr.msft.png":::
   <span data-ttu-id="f83a4-216">La **herramienta Red** ahora muestra **Fetch/XHR en** lugar de **XHR**</span><span class="sxs-lookup"><span data-stu-id="f83a4-216">The **Network** tool now shows **Fetch/XHR** instead of **XHR**</span></span>
:::image-end:::

<span data-ttu-id="f83a4-217">Para obtener más información, vaya a:</span><span class="sxs-lookup"><span data-stu-id="f83a4-217">For more information, navigate to:</span></span>
*  [<span data-ttu-id="f83a4-218">Especificación XMLHttpRequest</span><span class="sxs-lookup"><span data-stu-id="f83a4-218">XMLHttpRequest spec</span></span>][XhrSpecWhatwgOrg]
*  [<span data-ttu-id="f83a4-219">Especificaciones de captura</span><span class="sxs-lookup"><span data-stu-id="f83a4-219">Fetch spec</span></span>][FetchSpecWhatwgOrg]

<span data-ttu-id="f83a4-220">Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1201398][CR1201398].</span><span class="sxs-lookup"><span data-stu-id="f83a4-220">To review the history of this feature in the Chromium open-source project, navigate to Issue [1201398][CR1201398].</span></span>


### <a name="filter-wasm-resource-type-in-the-network-tool"></a><span data-ttu-id="f83a4-221">Tipo de recurso Filter Wasm en la herramienta Red</span><span class="sxs-lookup"><span data-stu-id="f83a4-221">Filter Wasm resource type in the Network tool</span></span>

<span data-ttu-id="f83a4-222">En la **herramienta Red,** ahora puede seleccionar el nuevo filtro **Wasm** para filtrar las solicitudes de red WebAssembly.</span><span class="sxs-lookup"><span data-stu-id="f83a4-222">In the **Network** tool, you can now select the new **Wasm** filter to filter the WebAssembly network requests.</span></span>

:::image type="complex" source="../../media/2021/05/wasm-network-requests.msft.png" alt-text="Filter by Wasm" lightbox="../../media/2021/05/wasm-network-requests.msft.png":::
   <span data-ttu-id="f83a4-224">Filter by Wasm</span><span class="sxs-lookup"><span data-stu-id="f83a4-224">Filter by Wasm</span></span>
:::image-end:::

<!-- screenshot uses http://memory-inspector.glitch.me/demo-wasm.html -->

<span data-ttu-id="f83a4-225">Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1103638][CR1103638].</span><span class="sxs-lookup"><span data-stu-id="f83a4-225">To review the history of this feature in the Chromium open-source project, navigate to Issue [1103638][CR1103638].</span></span>


### <a name="compute-intersections-are-now-included-in-the-performance-tool"></a><span data-ttu-id="f83a4-226">Las intersecciones de proceso ahora se incluyen en la herramienta Rendimiento</span><span class="sxs-lookup"><span data-stu-id="f83a4-226">Compute Intersections are now included in the Performance tool</span></span>

<span data-ttu-id="f83a4-227">En la **herramienta Rendimiento,** DevTools ahora muestra **Intersecciones de proceso** en el gráfico de llamas.</span><span class="sxs-lookup"><span data-stu-id="f83a4-227">In the **Performance** tool, DevTools now displays **Compute Intersections** in the flame chart.</span></span> <span data-ttu-id="f83a4-228">Estos cambios le ayudan a identificar eventos de observadores de intersección y a depurar la sobrecarga de rendimiento potencial de los observadores de intersección.</span><span class="sxs-lookup"><span data-stu-id="f83a4-228">These changes help you identify intersection observers events and debug the potential performance overhead of intersection observers.</span></span>

:::image type="complex" source="../../media/2021/05/compute-intersections-in-perf-tool.msft.png" alt-text="Calcular intersecciones en la herramienta Rendimiento" lightbox="../../media/2021/05/compute-intersections-in-perf-tool.msft.png":::
   <span data-ttu-id="f83a4-230">Calcular intersecciones en la **herramienta Rendimiento**</span><span class="sxs-lookup"><span data-stu-id="f83a4-230">Compute Intersections in the **Performance** tool</span></span>
:::image-end:::

<!-- screenshot uses https://googlechrome.github.io/samples/intersectionobserver -->

<span data-ttu-id="f83a4-231">Para obtener más información sobre los observadores de intersección, vaya a Confianza es [bueno, la observación es mejor: Intersection Observer v2][WebDevIntersectionObserverV2].</span><span class="sxs-lookup"><span data-stu-id="f83a4-231">For more about intersection observers, navigate to [Trust is good, observation is better: Intersection Observer v2][WebDevIntersectionObserverV2].</span></span>  <span data-ttu-id="f83a4-232">Para obtener información sobre cómo usar el gráfico de llamas, vaya [a Analizar una grabación de rendimiento.][DevtoolsEvaluatePerfRefAnalyzeAPerfRecording]</span><span class="sxs-lookup"><span data-stu-id="f83a4-232">For information about using the flame chart, navigate to [Analyze a performance recording][DevtoolsEvaluatePerfRefAnalyzeAPerfRecording].</span></span>  <span data-ttu-id="f83a4-233">Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [1199137][CR1199137].</span><span class="sxs-lookup"><span data-stu-id="f83a4-233">To review the history of this feature in the Chromium open-source project, navigate to Issue [1199137][CR1199137].</span></span>


## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="f83a4-234">Descargar los canales de vista previa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f83a4-234">Download the Microsoft Edge preview channels</span></span>

<span data-ttu-id="f83a4-235">Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f83a4-235">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="f83a4-236">Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="f83a4-236">The preview channels give you access to the latest DevTools features.</span></span>


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="f83a4-237">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f83a4-237">Getting in touch with Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]


<!-- links -->
[DevtoolsEvaluatePerfRefAnalyzeAPerfRecording]: ../../../evaluate-performance/reference.md#analyze-a-performance-recording "Analizar una grabación de rendimiento | Microsoft Docs"
<!-- external links -->
[XhrSpecWhatwgOrg]: https://xhr.spec.whatwg.org "Especificación XMLHttpRequest | WHATWG"
[FetchSpecWhatwgOrg]: https://fetch.spec.whatwg.org "Capturar especificaciones | WHATWG"

[WebDevIntersectionObserverV2]: https://web.dev/intersectionobserver-v2 "La confianza es buena, la observación es mejor: Intersection Observer v2 | web.dev"

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Uso de las herramientas | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Marketplace de extensiones | Visual Studio Code"

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Herramientas de desarrollador para Visual Studio Code | Visual Studio Marketplace"

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge: Estado de la plataforma | YouTube"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"
[CR1094406]: https://crbug.com/1094406 "Problema 1094406: los desarrolladores desean un visor de pedidos de origen | Chromium errores"
[CR1174299]: https://crbug.com/1174299 "Problema 1174299: Sugerencias de cliente ua se descartaron al reemplazar la cadena UA a través de la pestaña Condiciones de red de Chrome DevTools | Chromium errores"
[CR1203241]: https://crbug.com/1203241 "Problema 1203241: editor de cuadrícula CSS | Chromium errores"
[CR1076427]: https://crbug.com/1076427 "Problema 1076427: DevTools Console debe admitir la nueva declaración de const | Chromium errores"
[CR1192084]: https://crbug.com/1192084 "Problema 1192084: agregar la opción &quot;Mostrar detalles del marco&quot; con el botón derecho para crear etiquetas iframe/html en la vista de elementos | Chromium errores"
[CR1141824]: https://crbug.com/1141824 "Problema 1141824: mejorar el informe de errores de CORS en DevTools | Errores de Chromium"
[CR1201398]: https://crbug.com/1201398 "Problema 1201398: Solicitud de característica: cambiar el nombre del filtro de tipo XHR en panel de red | Chromium errores"
[CR1103638]: https://crbug.com/1103638 "Problema 1103638: Panel de red para mostrar recursos de WebAssembly | Chromium errores"
[CR1199137]: https://crbug.com/1199137 "Problema 1199137: Mostrar el costo de IntersectionObserver en el panel por | Chromium errores"

> [!NOTE]
> <span data-ttu-id="f83a4-258">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f83a4-258">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>
> <span data-ttu-id="f83a4-259">La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-xx) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="f83a4-259">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-xx) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>

<span data-ttu-id="f83a4-260">[ ![ Creative Commons License][CCby4Image]][CCA4IL] Este trabajo se concede bajo una licencia de Creative Commons [Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f83a4-260">[![Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

---
description: El botón Más herramientas, documentación en contexto para empezar a usar la extensión DevTools, mayor compatibilidad para lectores de pantalla en la consola y mucho más.
title: Novedades de DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ebd512800b8e55b5e9c0001c314a7c08fd242d5d
ms.sourcegitcommit: 30817cd9ae187a716d14d06962eb23b32dd54548
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "11590897"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a><span data-ttu-id="dcf16-104">Novedades de DevTools (Microsoft Edge 92)</span><span class="sxs-lookup"><span data-stu-id="dcf16-104">What's New In DevTools (Microsoft Edge 92)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

> [!TIP]
> <span data-ttu-id="dcf16-105">La **conferencia de Microsoft Build 2021** fue del 25 al 27 de mayo.</span><span class="sxs-lookup"><span data-stu-id="dcf16-105">The **Microsoft Build 2021** conference was on May 25-27.</span></span>  <span data-ttu-id="dcf16-106">Este es un vídeo de Build about the updates to DevTools: [Microsoft Edge | Estado de la plataforma:][YoutubeEdgeStateOfThePlatform] Microsoft Edge una plataforma atractiva y coherente con herramientas para desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="dcf16-106">Here's a video from Build about the updates to DevTools: [Microsoft Edge | State of the Platform][YoutubeEdgeStateOfThePlatform] - Microsoft Edge brings a compelling and consistent platform with tools for developers.</span></span>  <span data-ttu-id="dcf16-107">A medida que nuestros exploradores heredados no sean compatibles, Edge pronto será el único explorador compatible de Microsoft en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dcf16-107">As our legacy browsers phase out of support, Edge will soon be the only supported browser from Microsoft on Windows 10.</span></span>  <span data-ttu-id="dcf16-108">Únase a nosotros para obtener información sobre lo último en la plataforma perimetral, las herramientas y las aplicaciones web.</span><span class="sxs-lookup"><span data-stu-id="dcf16-108">Join us to learn about the latest across the Edge platform, tools, and web apps.</span></span>


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a><span data-ttu-id="dcf16-109">El botón Cerrar ya no está oculto cuando DevTools es estrecho</span><span class="sxs-lookup"><span data-stu-id="dcf16-109">The Close button is no longer hidden when DevTools is narrow</span></span>

<!-- Title: DevTools is now easier to close -->  
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->  

<span data-ttu-id="dcf16-110">En Microsoft Edge versión 91 o anterior, el botón Cerrar para cerrar DevTools no se muestra cuando la ventanilla de DevTools es estrecha. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="dcf16-110">In Microsoft Edge version 91 or earlier, the **Close** button to close DevTools isn't displayed when the DevTools viewport is narrow.</span></span>  <span data-ttu-id="dcf16-111">En Microsoft Edge versión 92, \*\*\*\* el botón Cerrar de DevTools siempre está presente, independientemente del ancho de la ventanilla de DevTools.</span><span class="sxs-lookup"><span data-stu-id="dcf16-111">In Microsoft Edge version 92, the **Close** button in the DevTools is always present, regardless of the DevTools viewport width.</span></span>

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="El botón Cerrar DevTools ahora está presente incluso cuando la ventanilla es estrecha" lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   <span data-ttu-id="dcf16-113">El **botón Cerrar** DevTools ahora está presente incluso cuando la ventanilla es estrecha</span><span class="sxs-lookup"><span data-stu-id="dcf16-113">The **Close** DevTools button is now present even when the viewport is narrow</span></span>  
:::image-end:::  


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a><span data-ttu-id="dcf16-114">Agregar herramientas rápidamente con el nuevo botón Más herramientas</span><span class="sxs-lookup"><span data-stu-id="dcf16-114">Add tools quickly with the new More Tools button</span></span>

<!-- Title: Add tools quickly with the new More Tools button -->  
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->  

<span data-ttu-id="dcf16-115">Hay una nueva forma de abrir más herramientas en Microsoft Edge DevTools: el **menú Más herramientas** ( ) `+` .</span><span class="sxs-lookup"><span data-stu-id="dcf16-115">There's a new way to open more tools in Microsoft Edge DevTools: the **More Tools** (`+`) menu.</span></span> <span data-ttu-id="dcf16-116">El **menú Más herramientas** aparece en la barra de herramientas del panel principal y en la barra de herramientas del cajón.</span><span class="sxs-lookup"><span data-stu-id="dcf16-116">The **More Tools** menu appears on the toolbar in the main panel and on the toolbar of the drawer.</span></span> <span data-ttu-id="dcf16-117">Al seleccionar una herramienta en el **menú Más herramientas,** se agrega la herramienta a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="dcf16-117">Selecting a tool from the **More Tools** menu adds the tool to the toolbar.</span></span>

<span data-ttu-id="dcf16-118">Para reordenar las pestañas de cualquiera de las barras de herramientas, seleccione y arrastre las pestañas.</span><span class="sxs-lookup"><span data-stu-id="dcf16-118">To reorder the tabs on either toolbar, select and drag the tabs.</span></span>  

<span data-ttu-id="dcf16-119">El **menú Más herramientas** estaba disponible como un experimento en Microsoft Edge versión 89 y ahora siempre está presente.</span><span class="sxs-lookup"><span data-stu-id="dcf16-119">The **More Tools** menu was available as an experiment in Microsoft Edge version 89, and is now always present.</span></span>

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="El botón Más herramientas de la barra de herramientas superior y la barra de herramientas del cajón" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   <span data-ttu-id="dcf16-121">El **botón Más herramientas** de la barra de herramientas superior y la barra de herramientas del cajón</span><span class="sxs-lookup"><span data-stu-id="dcf16-121">The **More Tools** button on the upper toolbar and drawer toolbar</span></span>
:::image-end:::  

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="Menú Más herramientas" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   <span data-ttu-id="dcf16-123">Menú **Más** herramientas</span><span class="sxs-lookup"><span data-stu-id="dcf16-123">The **More Tools** menu</span></span>
:::image-end:::  


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a><span data-ttu-id="dcf16-124">Mejoras para activar, seleccionar y cerrar herramientas</span><span class="sxs-lookup"><span data-stu-id="dcf16-124">Improvements for hovering, selecting, and closing tools</span></span>

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

<span data-ttu-id="dcf16-125">Las pestañas de cada herramienta se han reformateado para reducir la posibilidad de cerrar accidentalmente una herramienta.</span><span class="sxs-lookup"><span data-stu-id="dcf16-125">Tabs for each tool have been reformatted to reduce the chance of accidentally closing a tool.</span></span>  <span data-ttu-id="dcf16-126">En cada pestaña de la barra de herramientas principal y en la barra de herramientas del cajón, agregamos:</span><span class="sxs-lookup"><span data-stu-id="dcf16-126">On each tab in the main toolbar and in the toolbar of the drawer, we added:</span></span>
*  <span data-ttu-id="dcf16-127">Espaciado alrededor de la pestaña.</span><span class="sxs-lookup"><span data-stu-id="dcf16-127">Spacing around the tab.</span></span>
*  <span data-ttu-id="dcf16-128">Espaciado alrededor del botón cerrar ( `x` ) de la ficha.</span><span class="sxs-lookup"><span data-stu-id="dcf16-128">Spacing around the close (`x`) button in the tab.</span></span>
*  <span data-ttu-id="dcf16-129">Color de fondo al pasar el mouse sobre la pestaña.</span><span class="sxs-lookup"><span data-stu-id="dcf16-129">A background color when hovering over the tab.</span></span>
*  <span data-ttu-id="dcf16-130">Información sobre herramientas para el botón cerrar ( `x` ) de la pestaña.</span><span class="sxs-lookup"><span data-stu-id="dcf16-130">A tooltip for the close (`x`) button of the tab.</span></span>
*  <span data-ttu-id="dcf16-131">Contraste superior para el botón cerrar ( `x` ) de la ficha.</span><span class="sxs-lookup"><span data-stu-id="dcf16-131">Higher contrast for the close (`x`) button of the tab.</span></span>

<span data-ttu-id="dcf16-132">Por ejemplo, cuando estás \*\*\*\* en la herramienta \*\*\*\* Rendimiento y mantienes el mouse sobre la pestaña de la herramienta Red, estas mejoras ayudan a evitar el cierre accidental de la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="dcf16-132">For example, when you are in the **Performance** tool and you hover over the **Network** tool's tab, these improvements help prevent accidentally closing the **Network** tool.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Pestañas antes de reformatear" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           <span data-ttu-id="dcf16-134">Pestañas antes de reformatear</span><span class="sxs-lookup"><span data-stu-id="dcf16-134">Tabs before reformatting</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Pestañas después de la reformateado" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           <span data-ttu-id="dcf16-136">Pestañas después de la reformateado</span><span class="sxs-lookup"><span data-stu-id="dcf16-136">Tabs after reformatting</span></span> :::image-end:::
    :::column-end:::
:::row-end:::

<span data-ttu-id="dcf16-137">Estas mejoras son especialmente relevantes para los usuarios de DevTools localizados, en los que las pestañas pueden ser más estrechas y fáciles de cerrar accidentalmente.</span><span class="sxs-lookup"><span data-stu-id="dcf16-137">These improvements are especially relevant for users of localized DevTools, in which the tabs may be narrower and easier to accidentally close.</span></span>

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="Localized DevTools con pestañas estrechas" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   <span data-ttu-id="dcf16-139">Localized DevTools con pestañas estrechas</span><span class="sxs-lookup"><span data-stu-id="dcf16-139">Localized DevTools with narrow tabs</span></span>
:::image-end:::

<span data-ttu-id="dcf16-140">También facilitamos volver a agregar una herramienta que ha cerrado agregando un menú Más herramientas [a](#add-tools-quickly-with-the-new-more-tools-button) la barra de herramientas principal y la barra de herramientas del cajón.</span><span class="sxs-lookup"><span data-stu-id="dcf16-140">We also made it easier to re-add a tool that you closed by adding a [More Tools menu](#add-tools-quickly-with-the-new-more-tools-button) to the main toolbar and drawer toolbar.</span></span>


## <a name="better-support-for-screen-readers-in-the-console"></a><span data-ttu-id="dcf16-141">Mejor compatibilidad con lectores de pantalla en la consola</span><span class="sxs-lookup"><span data-stu-id="dcf16-141">Better support for screen readers in the Console</span></span>

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

<span data-ttu-id="dcf16-142">Antes de Microsoft Edge versión 92, en la **Consola,** las tecnologías de asistencia, como los lectores de pantalla, no anunciaban sugerencias de autocompletar ni los resultados de las expresiones evaluadas.</span><span class="sxs-lookup"><span data-stu-id="dcf16-142">Prior to Microsoft Edge version 92, in the **Console**, assistive technologies such as screen readers didn't announce autocomplete suggestions or the results of evaluated expressions.</span></span> <span data-ttu-id="dcf16-143">Esto se ha corregido ahora.</span><span class="sxs-lookup"><span data-stu-id="dcf16-143">This has been fixed now.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="En la consola, los lectores de pantalla ahora anuncian la sugerencia de autocompletar seleccionada actualmente" lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           <span data-ttu-id="dcf16-145">En la **Consola,** los lectores de pantalla ahora anuncian la sugerencia de autocompletar seleccionada actualmente</span><span class="sxs-lookup"><span data-stu-id="dcf16-145">In the **Console**, screen readers now announce the currently selected autocomplete suggestion</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="En la consola, los lectores de pantalla ahora anuncian el resultado de una expresión evaluada" lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           <span data-ttu-id="dcf16-147">En la **consola,** ahora los lectores de pantalla anuncian el resultado de una expresión evaluada</span><span class="sxs-lookup"><span data-stu-id="dcf16-147">In the **Console**, screen readers now announce the result of an evaluated expression</span></span> :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a><span data-ttu-id="dcf16-148">Microsoft Edge Developer Tools para Visual Studio Code versión 1.1.8</span><span class="sxs-lookup"><span data-stu-id="dcf16-148">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.8</span></span>

<span data-ttu-id="dcf16-149">El [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.8 for Microsoft Visual Studio Code tiene los siguientes cambios desde la versión anterior.</span><span class="sxs-lookup"><span data-stu-id="dcf16-149">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.8 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="dcf16-150">Microsoft Visual Studio Code actualiza las extensiones automáticamente.</span><span class="sxs-lookup"><span data-stu-id="dcf16-150">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="dcf16-151">Para actualizar manualmente a la versión 1.1.8, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="dcf16-151">To manually update to version 1.1.8, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  

<span data-ttu-id="dcf16-152">Puede presentar problemas y contribuir a la extensión en [vscode-edge-devtools GitHub repositorio][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="dcf16-152">You can file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a><span data-ttu-id="dcf16-153">Documentación e interfaz de usuario en contexto para facilitar el uso de la extensión DevTools</span><span class="sxs-lookup"><span data-stu-id="dcf16-153">In-context documentation and UI to make it easier to use the DevTools extension</span></span>

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->  
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->  

<span data-ttu-id="dcf16-154">La versión 1.1.8 de la extensión [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] ahora presenta una forma más sencilla de iniciar una nueva instancia de Microsoft Edge, presentando instrucciones, botones, vínculos y una página de documentación que le guiará.</span><span class="sxs-lookup"><span data-stu-id="dcf16-154">Version 1.1.8 of the [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension now features a simpler way to start a new instance of Microsoft Edge, by presenting instructions, buttons, links, and a documentation page to guide you.</span></span>

*  <span data-ttu-id="dcf16-155">Cuando selecciona el botón herramientas de \*\*\*\* **Microsoft Edge** en la barra de actividades de Visual Studio Code, el panel Herramientas de **Microsoft Edge:** Destinos ahora presenta texto explicativo, botones y vínculos para guiarlo, en lugar de un panel en blanco.</span><span class="sxs-lookup"><span data-stu-id="dcf16-155">When you select the **Microsoft Edge Tools** button in the **Activity Bar** of Visual Studio Code, the **Microsoft Edge Tools: Targets** panel now presents explanatory text, buttons, and links to guide you, instead of a blank panel.</span></span>

*  <span data-ttu-id="dcf16-156">Al abrir una nueva instancia de Microsoft Edge desde dentro de Visual Studio Code, Microsoft Edge muestra ahora una página de inicio que explica cómo usar la extensión Herramientas de desarrollo, en lugar de una página en blanco.</span><span class="sxs-lookup"><span data-stu-id="dcf16-156">When you open a new instance of Microsoft Edge from within Visual Studio Code, Microsoft Edge now shows a start page that explains how to use the Developer Tools extension, instead of a blank page.</span></span>

*  <span data-ttu-id="dcf16-157">El **panel herramientas Microsoft Edge:** destinos ahora tiene un botón Generar **launch.jsen** y las instrucciones, para ayudar a iniciar el proyecto para la depuración en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dcf16-157">The **Microsoft Edge Tools: Targets** panel now has a **Generate launch.json** button and instructions, to help launch your project for debugging in Microsoft Edge.</span></span>

<span data-ttu-id="dcf16-158">Para obtener más información, vaya [a Uso de las herramientas][GithubIoDevToolsUsing].</span><span class="sxs-lookup"><span data-stu-id="dcf16-158">For more information, navigate to [Using the tools][GithubIoDevToolsUsing].</span></span>


## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="dcf16-159">Descargar los canales de vista previa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dcf16-159">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="dcf16-160">Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dcf16-160">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="dcf16-161">Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="dcf16-161">The preview channels give you access to the latest DevTools features.</span></span>  


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="dcf16-162">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="dcf16-162">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Uso de las herramientas | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de versiones preliminares de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Marketplace de extensiones | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Herramientas de desarrollador para Visual Studio Code | Visual Studio Marketplace"  

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge: Estado de la plataforma | YouTube"

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="dcf16-170">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dcf16-170">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  

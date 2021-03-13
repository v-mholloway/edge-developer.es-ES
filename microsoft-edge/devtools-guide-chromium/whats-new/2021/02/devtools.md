---
description: Compatibilidad con depuración para CSS Flexbox, presentación de actualizaciones de rendimiento en la página web, problemas de actualizaciones de herramientas y mucho más
title: Novedades de DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 4222bcf7284b69269691ec9fb78094e5efb95793
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408587"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-90"></a><span data-ttu-id="3c336-104">Novedades de DevTools (Microsoft Edge 90)</span><span class="sxs-lookup"><span data-stu-id="3c336-104">What's New In DevTools (Microsoft Edge 90)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a><span data-ttu-id="3c336-105">Agrupar herramientas en modo de foco</span><span class="sxs-lookup"><span data-stu-id="3c336-105">Group tools together in Focus Mode</span></span>  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

<span data-ttu-id="3c336-106">El modo de enfoque es una interfaz experimental que permite agrupar distintas herramientas en función de sus propios escenarios de depuración.</span><span class="sxs-lookup"><span data-stu-id="3c336-106">Focus Mode is an experimental interface that allows you to group different tools together based on your own debugging scenarios.</span></span>  <span data-ttu-id="3c336-107">La nueva **barra de actividades** que se muestra a la izquierda incluye grupos de herramientas predefinidos, como **Diseño** y **depuración.**</span><span class="sxs-lookup"><span data-stu-id="3c336-107">The new **Activity Bar** displayed on the left includes predefined tool groups such as **Layout** and **Debugging**.</span></span>  <span data-ttu-id="3c336-108">Para personalizar cada grupo de herramientas, cierre las herramientas con el icono **Cerrar** \( \) o agregue nuevas herramientas con el icono Más herramientas `X` \( \*\*\*\* `+` \).</span><span class="sxs-lookup"><span data-stu-id="3c336-108">To customize each tool group, close tools with the **Close** \(`X`\) icon or add new tools with the **More tools** \(`+`\) icon.</span></span>  

<span data-ttu-id="3c336-109">Para activar el experimento, vaya a Activar características [experimentales][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] y seleccione las casillas situadas junto a Modo de foco y Información sobre herramientas **de DevTools** y **Habilitar + menús**de pestañas de botón para abrir más herramientas.</span><span class="sxs-lookup"><span data-stu-id="3c336-109">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="3c336-110">Para obtener más información sobre esta característica o comentar con preguntas e ideas, vaya [a DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="3c336-110">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Mostrar la barra de actividades" lightbox="../../media/2021/02/focus-mode.msft.png":::
   <span data-ttu-id="3c336-112">Mostrar la **barra de actividades**</span><span class="sxs-lookup"><span data-stu-id="3c336-112">Display the **Activity Bar**</span></span>  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="3c336-113">Obtenga información sobre DevTools con información sobre herramientas informativas</span><span class="sxs-lookup"><span data-stu-id="3c336-113">Learn about DevTools with informative tooltips</span></span>  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

<span data-ttu-id="3c336-114">La característica DevTools Tooltips le ayuda a obtener información sobre todas las diferentes herramientas y paneles.</span><span class="sxs-lookup"><span data-stu-id="3c336-114">The DevTools Tooltips feature helps you learn about all the different tools and panes.</span></span>  <span data-ttu-id="3c336-115">Elija el icono Ayuda \( \) situado en la parte inferior de la barra de actividades para alternar la información sobre `?` herramientas en \*\*\*\* DevTools.</span><span class="sxs-lookup"><span data-stu-id="3c336-115">Choose the Help \(`?`\) icon at the bottom of the **Activity Bar** to toggle tooltips in the DevTools.</span></span>  <span data-ttu-id="3c336-116">Cuando haya información sobre herramientas, mantenga el mouse sobre cada región de DevTools descrita para obtener más información sobre cómo usar la herramienta.</span><span class="sxs-lookup"><span data-stu-id="3c336-116">When tooltips are on, hover over each outlined region of DevTools to learn more about how to use the tool.</span></span>  <span data-ttu-id="3c336-117">Para activar el experimento, vaya a Activar características [experimentales][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] y seleccione las casillas situadas junto a Modo de foco y Información sobre herramientas **de DevTools** y **Habilitar + menús**de pestañas de botón para abrir más herramientas.</span><span class="sxs-lookup"><span data-stu-id="3c336-117">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="3c336-118">Para obtener más información sobre esta característica o comentar con preguntas e ideas, vaya [a DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="3c336-118">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Elija el icono ayuda (?) de la barra de actividades para mostrar información sobre herramientas" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   <span data-ttu-id="3c336-120">Elija el icono Ayuda \( `?` \) de la barra **de actividades** para mostrar información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="3c336-120">Choose the Help \(`?`\) icon in the **Activity Bar** to display tooltips</span></span>  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a><span data-ttu-id="3c336-121">Personalizar métodos abreviados de teclado en Configuración</span><span class="sxs-lookup"><span data-stu-id="3c336-121">Customize keyboard shortcuts in Settings</span></span>  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

<span data-ttu-id="3c336-122">Ahora puede personalizar el método abreviado de teclado para cualquier acción en DevTools.</span><span class="sxs-lookup"><span data-stu-id="3c336-122">You may now customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="3c336-123">Para editar un método abreviado de teclado, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="3c336-123">To edit a keyboard shortcut, complete the following actions.</span></span>  

1.  <span data-ttu-id="3c336-124">Abra DevTools y, \*\*\*\* a continuación, elija  >  **Métodos abreviados de configuración**.</span><span class="sxs-lookup"><span data-stu-id="3c336-124">Open the DevTools, and then choose **Settings** > **Shortcuts**.</span></span>  
1.  <span data-ttu-id="3c336-125">Elija la acción que desea personalizar.</span><span class="sxs-lookup"><span data-stu-id="3c336-125">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="3c336-126">Elija la opción Editar \(</span><span class="sxs-lookup"><span data-stu-id="3c336-126">Choose the Edit \(</span></span>![Editar icono de método abreviado de teclado](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)<span data-ttu-id="3c336-128">\) icono.</span><span class="sxs-lookup"><span data-stu-id="3c336-128">\) icon.</span></span>  
1.  <span data-ttu-id="3c336-129">Seleccione las claves que desea enlazar a la acción.</span><span class="sxs-lookup"><span data-stu-id="3c336-129">Select the keys you want to bind to the action.</span></span>  
1.  <span data-ttu-id="3c336-130">Elija la marca de verificación \(</span><span class="sxs-lookup"><span data-stu-id="3c336-130">Choose the checkmark \(</span></span>![Icono de método abreviado de teclado Marca de verificación](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="3c336-132">\) icono.</span><span class="sxs-lookup"><span data-stu-id="3c336-132">\) icon.</span></span>  
    
<span data-ttu-id="3c336-133">Para obtener más información acerca de la personalización y edición de accesos directos, vaya a [Personalizar métodos abreviados de teclado en Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="3c336-133">For more information about customizing and editing shortcuts, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="3c336-134">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto Chromium, vaya al problema [174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="3c336-134">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Personalizar los métodos abreviados de teclado en la configuración de DevTools en accesos directos con un acceso directo en modo de edición" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   <span data-ttu-id="3c336-136">Personalizar los métodos abreviados de teclado en [la configuración de DevTools][DevtoolsCustomizeIndexSettings] en accesos directos con un acceso directo en modo de edición</span><span class="sxs-lookup"><span data-stu-id="3c336-136">Customize keyboard shortcuts in the [DevTools Settings][DevtoolsCustomizeIndexSettings] on Shortcuts with a shortcut in edit mode</span></span>  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a><span data-ttu-id="3c336-137">Microsoft Edge DevTools para Visual Studio de extensión de código 1.1.4</span><span class="sxs-lookup"><span data-stu-id="3c336-137">Microsoft Edge DevTools for Visual Studio Code extension update 1.1.4</span></span>  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

<span data-ttu-id="3c336-138">Microsoft [Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.4 for Microsoft Visual Studio Code ahora muestra un icono de favoritos junto a cada una de las instancias de DevTools.</span><span class="sxs-lookup"><span data-stu-id="3c336-138">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.4 for Microsoft Visual Studio Code now displays a favicon next to each of the DevTools instances.</span></span>  <span data-ttu-id="3c336-139">Los mensajes de consola de Microsoft Edge ahora se muestran en **la Consola de DevTools** en **Salida** de Microsoft Visual Studio código.</span><span class="sxs-lookup"><span data-stu-id="3c336-139">Console messages from Microsoft Edge now display in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  <span data-ttu-id="3c336-140">Microsoft Visual Studio código actualiza las extensiones automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3c336-140">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="3c336-141">Para actualizar manualmente a la versión 1.1.4, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="3c336-141">To manually update to version 1.1.4, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="3c336-142">Puede presentar problemas y contribuir a la extensión en el repositorio de GitHub [vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]</span><span class="sxs-lookup"><span data-stu-id="3c336-142">You may file issues and contribute to the extension on the [vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools] GitHub repo.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="3c336-143">En la siguiente figura se muestran los mensajes de una página web de ejemplo registrada en la **herramienta consola** en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3c336-143">The following figure displays messages from an example webpage logged in the **Console** tool in Microsoft Edge.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="3c336-144">En la siguiente figura se muestran los mismos mensajes de la página web de ejemplo registrada en la Consola **de DevTools** en **Salida** de Microsoft Visual Studio código.</span><span class="sxs-lookup"><span data-stu-id="3c336-144">The following figure displays the same messages from the example webpage logged in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Mostrar un mensaje en consola en Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         <span data-ttu-id="3c336-146">Mostrar un mensaje en consola en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3c336-146">Display a message in Console in Microsoft Edge DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Mostrar el mismo mensaje en la consola de DevTools en Salida de Microsoft Visual Studio código" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         <span data-ttu-id="3c336-148">Mostrar el mismo mensaje en la consola de DevTools en Salida de Microsoft Visual Studio código</span><span class="sxs-lookup"><span data-stu-id="3c336-148">Display the same message in the DevTools Console under Output of Microsoft Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a><span data-ttu-id="3c336-149">Edición mejorada de flexbox CSS con editor de flexbox visual y varias superposiciones</span><span class="sxs-lookup"><span data-stu-id="3c336-149">Improved CSS flexbox editing with visual flexbox editor and multiple overlays</span></span>  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

<span data-ttu-id="3c336-150">DevTools ahora tiene herramientas de depuración de flexbox CSS dedicadas.</span><span class="sxs-lookup"><span data-stu-id="3c336-150">DevTools now has dedicated CSS flexbox debugging tools.</span></span>  <span data-ttu-id="3c336-151">Si el estilo o CSS se aplica a un elemento HTML, se muestra un icono junto `display: flex` a ese elemento en la `display: inline-flex` `flex` **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="3c336-151">If the `display: flex` or `display: inline-flex` CSS style is applied to an HTML element, a `flex` icon displays next to that element in the **Elements** tool.</span></span>  <span data-ttu-id="3c336-152">Para mostrar \(u hide\) una superposición de flex en la página web, elija el `flex` icono.</span><span class="sxs-lookup"><span data-stu-id="3c336-152">To display \(or hide\) a flex overlay on the webpage, choose the `flex` icon.</span></span>  <span data-ttu-id="3c336-153">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a Los problemas [1166710][CR1166710] y [1175699][CR1175699].</span><span class="sxs-lookup"><span data-stu-id="3c336-153">To review the history of this feature in the Chromium open-source project, navigate to Issues [1166710][CR1166710] and [1175699][CR1175699].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="3c336-154">Para abrir el editor **de Flexbox,** vaya al panel **Estilos** y elija el nuevo icono junto al `display: flex` estilo `display: inline-flex` or.</span><span class="sxs-lookup"><span data-stu-id="3c336-154">To open the **Flexbox** editor, navigate to the **Styles** pane and choose the new icon next to the `display: flex` or `display: inline-flex` style.</span></span>  <span data-ttu-id="3c336-155">El editor **de Flexbox** proporciona una forma rápida de editar las propiedades de flexbox.</span><span class="sxs-lookup"><span data-stu-id="3c336-155">The **Flexbox** editor provides a quick way to edit the flexbox properties.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="3c336-156">Además, la sección **Flexbox** del panel **Diseño** muestra todos los elementos de flexbox en la página web.</span><span class="sxs-lookup"><span data-stu-id="3c336-156">In addition, the **Flexbox** section in the **Layout** pane displays all of the flexbox elements on the webpage.</span></span>  <span data-ttu-id="3c336-157">Puede alternar la superposición de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="3c336-157">You may toggle the overlay of each element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="Herramientas de depuración de flexbox CSS" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         <span data-ttu-id="3c336-159">Herramientas de depuración de flexbox CSS</span><span class="sxs-lookup"><span data-stu-id="3c336-159">CSS flexbox debugging tools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Sección Flexbox en el panel Diseño" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         <span data-ttu-id="3c336-161">**Sección Flexbox** en el **panel Diseño**</span><span class="sxs-lookup"><span data-stu-id="3c336-161">**Flexbox** section in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a><span data-ttu-id="3c336-162">Mejoras de navegación con teclado para solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="3c336-162">Keyboard navigation improvements for network requests</span></span>  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

<span data-ttu-id="3c336-163">Anteriormente, no podía expandir o contraer la cadena de solicitudes con las teclas de flecha del teclado en el panel **Iniciador,** a diferencia del DOM de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="3c336-163">Previously, you were not able to expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane, unlike the DOM in the **Elements** tool.</span></span>  <span data-ttu-id="3c336-164">Cuando se selecciona una solicitud de red en la **herramienta** Red, el panel **Iniciador** muestra la cadena de solicitudes que inició la solicitud seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="3c336-164">When a network request is selected in the **Network** tool, the **Initiator** pane displays the chain of requests that initiated the currently selected request.</span></span>  

<span data-ttu-id="3c336-165">En Microsoft Edge versión 90, puede expandir o contraer la cadena de solicitudes mediante las teclas de flecha del teclado en el **panel Iniciador.**</span><span class="sxs-lookup"><span data-stu-id="3c336-165">In Microsoft Edge version 90, you may expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane.</span></span>  <span data-ttu-id="3c336-166">Ahora también se resalta la solicitud de red centrada en la cadena.</span><span class="sxs-lookup"><span data-stu-id="3c336-166">The focused network request in the chain is also now highlighted.</span></span>  <span data-ttu-id="3c336-167">Para obtener más información sobre los iniciadores en la **herramienta Red,** vaya [a Mostrar iniciadores y dependencias][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="3c336-167">To learn more about initiators in the **Network** tool, navigate to [Display initiators and dependencies][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].</span></span>  <span data-ttu-id="3c336-168">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a Los problemas [1158276][CR1158276] y [1160637][CR1160637].</span><span class="sxs-lookup"><span data-stu-id="3c336-168">To review the history of this feature in the Chromium open-source project, navigate to Issues [1158276][CR1158276] and [1160637][CR1160637].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Elija una solicitud de red y elija el panel Iniciador" lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         <span data-ttu-id="3c336-170">Elija una solicitud de red y elija el **panel Iniciador**</span><span class="sxs-lookup"><span data-stu-id="3c336-170">Choose a Network request and choose the **Initiator** pane</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Expandir o contraer la cadena de iniciador de solicitudes y seguir la fila resaltada" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         <span data-ttu-id="3c336-172">Expandir o contraer la cadena de iniciador de solicitudes y seguir la fila resaltada</span><span class="sxs-lookup"><span data-stu-id="3c336-172">Expand or collapse the request initiator chain and follow the highlighted row</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a><span data-ttu-id="3c336-173">El filtrado en la consola es más coherente</span><span class="sxs-lookup"><span data-stu-id="3c336-173">Filtering in the Console is more consistent</span></span>  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

<span data-ttu-id="3c336-174">Mientras filtra con la barra lateral [de la][DevtoolsConsoleReferenceOpenConsoleSidebar]consola, los filtros de la lista desplegable [Niveles de][DevtoolsConsoleReferenceFilterByLogLevel] registro no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="3c336-174">While you filter with the [Console Sidebar][DevtoolsConsoleReferenceOpenConsoleSidebar], the filters in the [Log Levels][DevtoolsConsoleReferenceFilterByLogLevel] dropdown are not available.</span></span>  <span data-ttu-id="3c336-175">Anteriormente, la lista desplegable **Niveles de** registro se resaltaba al mantener el mouse sobre él, incluso mientras se seleccionaba un filtro de **la** barra lateral de la consola.</span><span class="sxs-lookup"><span data-stu-id="3c336-175">Previously, the **Log Levels** dropdown highlighted when you hovered on it, even while a filter from the **Console Sidebar** was chosen.</span></span>  <span data-ttu-id="3c336-176">En la versión 90 de Microsoft Edge, el desplegable **Niveles** de registro ya no se resalta al mantener el mouse sobre él mientras se elige un filtro de la barra **lateral** de consola.</span><span class="sxs-lookup"><span data-stu-id="3c336-176">In Microsoft Edge version 90, the **Log Levels** dropdown no longer highlights when you hover on it while a filter from the **Console Sidebar** is chosen.</span></span>  <span data-ttu-id="3c336-177">Para obtener más información sobre el filtrado en la **consola,** vaya a [Filtrar mensajes][DevtoolsConsoleReferenceFilterMessages].</span><span class="sxs-lookup"><span data-stu-id="3c336-177">To learn more about filtering in the **Console**, navigate to [Filter Messages][DevtoolsConsoleReferenceFilterMessages].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Anteriormente, si abres la barra lateral de consola y mantienes el mouse en niveles predeterminados, se resaltó." lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         <span data-ttu-id="3c336-179">Anteriormente, si abres la **barra** lateral de consola y mantienes el mouse en **niveles predeterminados,** se resaltó.</span><span class="sxs-lookup"><span data-stu-id="3c336-179">Previously, if you open the **Console sidebar** and hover on **Default levels** it was highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="A partir de Microsoft Edge 90, si eliges la barra lateral de consola y mantienes el mouse en Niveles predeterminados, no se resalta" lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         <span data-ttu-id="3c336-181">A partir de Microsoft Edge 90, si eliges la barra lateral de consola y mantienes el mouse en **Niveles**predeterminados, no se resalta \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3c336-181">Starting in Microsoft Edge 90, if you choose the **Console sidebar** and hover on **Default levels**, it does not highlight</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="3c336-182">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="3c336-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a><span data-ttu-id="3c336-183">La consola ahora se escape de caracteres de comilla doble</span><span class="sxs-lookup"><span data-stu-id="3c336-183">The Console now escapes double quote characters</span></span>  

<span data-ttu-id="3c336-184">Anteriormente, la **consola no** generaba caracteres válidos de comilla doble \( `"` \) en cadenas javascript.</span><span class="sxs-lookup"><span data-stu-id="3c336-184">Previously, the **Console** did not output valid double quote \(`"`\) characters in JavaScript strings.</span></span>  <span data-ttu-id="3c336-185">A partir de la versión \*\*\*\* 90 de Microsoft Edge, la consola genera cadenas de JavaScript con caracteres de comilla doble de escape \( `"` \).</span><span class="sxs-lookup"><span data-stu-id="3c336-185">Starting in Microsoft Edge version 90, the **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters.</span></span>  <span data-ttu-id="3c336-186">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1178530][CR1178530].</span><span class="sxs-lookup"><span data-stu-id="3c336-186">To review the history of this feature in the Chromium open-source project, navigate to Issue [1178530][CR1178530].</span></span>  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="La consola genera cadenas de JavaScript con caracteres de comilla doble de escape (&#0022;)" lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   <span data-ttu-id="3c336-188">La **consola genera** cadenas de JavaScript con caracteres de comilla doble de escape \( `"` \)</span><span class="sxs-lookup"><span data-stu-id="3c336-188">The **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters</span></span>  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a><span data-ttu-id="3c336-189">Emular la característica multimedia de gama de colores CSS</span><span class="sxs-lookup"><span data-stu-id="3c336-189">Emulate the CSS color-gamut media feature</span></span>  

<span data-ttu-id="3c336-190">La [consulta multimedia de gama][ChromestatusFeature5354410980933632] de colores emula el intervalo aproximado de colores admitido por el explorador y el dispositivo que estás probando.</span><span class="sxs-lookup"><span data-stu-id="3c336-190">The [color-gamut][ChromestatusFeature5354410980933632] media query emulates the approximate range of colors supported by the browser and the device you are testing.</span></span>  <span data-ttu-id="3c336-191">El desplegable de **emular la** gama de colores de la característica multimedia CSS contiene espacios de color que DevTools puede emular.</span><span class="sxs-lookup"><span data-stu-id="3c336-191">The dropdown under **Emulate CSS media feature color-gamut** contains color spaces that DevTools may emulate.</span></span>  <span data-ttu-id="3c336-192">Por ejemplo, para desencadenar una consulta `color-gamut: p3` multimedia, elija **color-gamut: p3** en el desplegable.</span><span class="sxs-lookup"><span data-stu-id="3c336-192">For example, to trigger a `color-gamut: p3` media query, choose **color-gamut: p3** from the dropdown.</span></span>  

<span data-ttu-id="3c336-193">Para emular la característica multimedia de gama de colores CSS, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="3c336-193">To emulate the CSS color-gamut media feature, complete the following actions.</span></span>  

1.  <span data-ttu-id="3c336-194">Abra el [menú de comandos][DevtoolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="3c336-194">Open the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
1.  <span data-ttu-id="3c336-195">Escribe `Rendering`.</span><span class="sxs-lookup"><span data-stu-id="3c336-195">Type `Rendering`.</span></span>  
1.  <span data-ttu-id="3c336-196">Ejecute el **comando Mostrar representación.**</span><span class="sxs-lookup"><span data-stu-id="3c336-196">Run the **Show Rendering** command.</span></span>  
1.  <span data-ttu-id="3c336-197">Vaya a **Emular la gama de colores de** la característica multimedia CSS y elija una opción.</span><span class="sxs-lookup"><span data-stu-id="3c336-197">Navigate to **Emulate CSS media feature color-gamut** and choose an option.</span></span>  

<span data-ttu-id="3c336-198">Para obtener más información sobre la `color-gamut` característica, vaya [a Color Display Quality: the 'color-gamut' feature][CsswgDraftsMediaqueries4ColorGamut].</span><span class="sxs-lookup"><span data-stu-id="3c336-198">To learn more about the `color-gamut` feature, navigate to [Color Display Quality: the 'color-gamut' feature][CsswgDraftsMediaqueries4ColorGamut].</span></span>  <span data-ttu-id="3c336-199">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1073887][CR1073887].</span><span class="sxs-lookup"><span data-stu-id="3c336-199">To review the history of this feature in the Chromium open-source project, navigate to Issue [1073887][CR1073887].</span></span>  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Emular la característica multimedia de gama de colores CSS" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   <span data-ttu-id="3c336-201">Emular la característica multimedia de gama de colores CSS</span><span class="sxs-lookup"><span data-stu-id="3c336-201">Emulate the CSS color-gamut media feature</span></span>  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a><span data-ttu-id="3c336-202">Herramientas mejoradas de aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="3c336-202">Improved Progressive Web Apps tooling</span></span>  

#### <a name="pwa-installability-warning-in-the-console"></a><span data-ttu-id="3c336-203">Advertencia de instalación de PWA en la consola</span><span class="sxs-lookup"><span data-stu-id="3c336-203">PWA installability warning in the Console</span></span>  

<span data-ttu-id="3c336-204">La **consola** ahora muestra un mensaje de advertencia de instalación de Aplicaciones web progresivas [(PWA)][ProgressiveWebAppsIndex] más detallado con un vínculo a Mejorar la detección de compatibilidad sin conexión de [Progressive Web App][ChromeDeveloperBlogImprovedPwaOfflineDetection].</span><span class="sxs-lookup"><span data-stu-id="3c336-204">The **Console** now displays a more detailed [Progressive Web Apps (PWA)][ProgressiveWebAppsIndex] installability warning message with a link to [Improving Progressive Web App offline support detection][ChromeDeveloperBlogImprovedPwaOfflineDetection].</span></span>  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Advertencia de instalación de PWA en la herramienta consola" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   <span data-ttu-id="3c336-206">Advertencia de instalación de PWA en **la herramienta consola**</span><span class="sxs-lookup"><span data-stu-id="3c336-206">PWA installability warning in **Console** tool</span></span>  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a><span data-ttu-id="3c336-207">Advertencia de longitud de descripción de PWA en el panel Manifiesto</span><span class="sxs-lookup"><span data-stu-id="3c336-207">PWA description length warning in the Manifest pane</span></span>

<span data-ttu-id="3c336-208">El **panel** Manifiesto ahora muestra un mensaje de advertencia si la descripción del manifiesto supera los 324 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3c336-208">The **Manifest** pane now displays a warning message if the manifest description exceeds 324 characters.</span></span>  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Advertencia truncada de descripción de PWA" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   <span data-ttu-id="3c336-210">Advertencia truncada de descripción de PWA</span><span class="sxs-lookup"><span data-stu-id="3c336-210">PWA description truncate warning</span></span>  
:::image-end:::  

<span data-ttu-id="3c336-211">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a Los problemas [965802][CR965802], [1146450][CR1146450]y [1169689][CR1169689].</span><span class="sxs-lookup"><span data-stu-id="3c336-211">To review the history of this feature in the Chromium open-source project, navigate to Issues [965802][CR965802], [1146450][CR1146450], and [1169689][CR1169689].</span></span>  

### <a name="new-remote-address-space-column-in-the-network-tool"></a><span data-ttu-id="3c336-212">Nueva columna Espacio de direcciones remotas en la herramienta Red</span><span class="sxs-lookup"><span data-stu-id="3c336-212">New Remote Address Space column in the Network tool</span></span>  

<!-- does not work in canary 90.0.813.0 -->  
<span data-ttu-id="3c336-213">La nueva **columna Espacio de direcciones remotas** muestra el espacio de direcciones IP de red de cada recurso de red.</span><span class="sxs-lookup"><span data-stu-id="3c336-213">The new **Remote Address Space** column displays the network IP address space of each network resource.</span></span>  <span data-ttu-id="3c336-214">Para mostrar la nueva columna Espacio de direcciones remotas, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="3c336-214">To display the new Remote Address Space column, complete the following actions.</span></span>  

1.  <span data-ttu-id="3c336-215">Vaya a la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="3c336-215">Navigate to the **Network** tool.</span></span>  
1.  <span data-ttu-id="3c336-216">En la tabla Solicitudes, mantenga el mouse en la fila de encabezado y abra el menú contextual \(hacer clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="3c336-216">In the Requests table, hover on the header row, and open the contextual menu \(right-click\).</span></span>  <span data-ttu-id="3c336-217">Para obtener información sobre cómo agregar o quitar columnas de la tabla Solicitudes, vaya a [Agregar o quitar columnas.][DevtoolsNetworkReferenceAddRemoveColumns]</span><span class="sxs-lookup"><span data-stu-id="3c336-217">To learn how to add or remove columns from the Requests table, navigate to [Add or remove columns][DevtoolsNetworkReferenceAddRemoveColumns].</span></span>  
1.  <span data-ttu-id="3c336-218">Elija **Espacio de direcciones remotas**.</span><span class="sxs-lookup"><span data-stu-id="3c336-218">Choose **Remote Address Space**.</span></span>  
    
<span data-ttu-id="3c336-219">La tabla Solicitudes ahora muestra una nueva columna con el encabezado denominado **Espacio de direcciones remotas**.</span><span class="sxs-lookup"><span data-stu-id="3c336-219">The Requests table now displays a new column with the header named **Remote Address Space**.</span></span>  <span data-ttu-id="3c336-220">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1128885][CR1128885].</span><span class="sxs-lookup"><span data-stu-id="3c336-220">To review the history of this feature in the Chromium open-source project, navigate to Issue [1128885][CR1128885].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="En el menú contextual, elija Espacio de direcciones remotas" lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         <span data-ttu-id="3c336-222">En el menú contextual, elija el **espacio de direcciones remotas**</span><span class="sxs-lookup"><span data-stu-id="3c336-222">In the contextual menu, choose the **Remote Address Space**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="La tabla Solicitudes ahora muestra la columna Espacio de direcciones remotas" lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         <span data-ttu-id="3c336-224">La tabla Solicitudes ahora muestra la **columna Espacio de direcciones** remotas</span><span class="sxs-lookup"><span data-stu-id="3c336-224">The Requests table now displays the **Remote Address Space** column</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a><span data-ttu-id="3c336-225">Mostrar características permitidas y no permitidas en la vista Detalles del marco</span><span class="sxs-lookup"><span data-stu-id="3c336-225">Display allowed and disallowed features in the Frame details view</span></span>  

<span data-ttu-id="3c336-226">La vista Detalles del marco ahora muestra una lista de características de explorador permitidas y no [permitidas controladas][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]por la directiva de permisos .</span><span class="sxs-lookup"><span data-stu-id="3c336-226">The Frame details view now displays a list of allowed and disallowed browser features controlled by the [Permissions Policy][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer].</span></span>  <span data-ttu-id="3c336-227">Directiva de permisos es una API de plataforma web que permite \(o bloques\) una página web el uso de características del explorador en un marco individual o en iframes que inserta.</span><span class="sxs-lookup"><span data-stu-id="3c336-227">Permissions Policy is a web platform API that allows \(or blocks\) a webpage the use of browser features in an individual frame or in iframes that it embeds.</span></span>  <span data-ttu-id="3c336-228">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1158827][CR1158827].</span><span class="sxs-lookup"><span data-stu-id="3c336-228">To review the history of this feature in the Chromium open-source project, navigate to Issue [1158827][CR1158827].</span></span>  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Características permitidas y no permitidas basadas en la directiva de permisos" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   <span data-ttu-id="3c336-230">Características permitidas y no permitidas basadas en la directiva de permisos</span><span class="sxs-lookup"><span data-stu-id="3c336-230">Allowed and disallowed features based on the Permission Policy</span></span>  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a><span data-ttu-id="3c336-231">Nueva columna SameParty en el panel Cookies</span><span class="sxs-lookup"><span data-stu-id="3c336-231">New SameParty column in the Cookies pane</span></span>  

<span data-ttu-id="3c336-232">El **panel Cookies** de la herramienta **Aplicación** ahora muestra el atributo de `SameParty` cada cookie.</span><span class="sxs-lookup"><span data-stu-id="3c336-232">The **Cookies** pane in the **Application** tool now displays the `SameParty` attribute for each cookie.</span></span>  <span data-ttu-id="3c336-233">El `SameParty` atributo es un nuevo atributo booleano para indicar si una cookie se incluye en las solicitudes a los orígenes de los mismos conjuntos de [terceros][GithubPrivacycgFirstPartySets].</span><span class="sxs-lookup"><span data-stu-id="3c336-233">The `SameParty` attribute is a new boolean attribute to indicate whether a cookie is included in requests to origins of the same [First-Party Sets][GithubPrivacycgFirstPartySets].</span></span>  <span data-ttu-id="3c336-234">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1161427][CR1161427].</span><span class="sxs-lookup"><span data-stu-id="3c336-234">To review the history of this feature in the Chromium open-source project, navigate to Issue [1161427][CR1161427].</span></span>  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Columna SameParty en el panel Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   <span data-ttu-id="3c336-236">**Columna SameParty** en el **panel Cookies**</span><span class="sxs-lookup"><span data-stu-id="3c336-236">**SameParty** column in the **Cookies** pane</span></span>  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a><span data-ttu-id="3c336-237">La propiedad fn.displayName de la herramienta Consola ya está en desuso</span><span class="sxs-lookup"><span data-stu-id="3c336-237">fn.displayName property in the Console tool is now deprecated</span></span>  

<span data-ttu-id="3c336-238">Anteriormente, la propiedad le permitía controlar los nombres de depuración de las funciones que se muestran en y en los seguimientos de pila `fn.displayName` `error.stack` de DevTools.</span><span class="sxs-lookup"><span data-stu-id="3c336-238">Previously, the `fn.displayName` property allowed you to control debug names for functions to display in `error.stack` and in DevTools stack traces.</span></span>  <span data-ttu-id="3c336-239">A partir de la versión 90 de Microsoft Edge, la propiedad ahora está en `fn.displayName` desuso y reemplazada por la `fn.name` propiedad.</span><span class="sxs-lookup"><span data-stu-id="3c336-239">Starting in Microsoft Edge version 90, the `fn.displayName` property is now deprecated, and replaced by the `fn.name` property.</span></span>  <span data-ttu-id="3c336-240">Use el método `Object.defineProperty` estándar para definir la `fn.name` propiedad.</span><span class="sxs-lookup"><span data-stu-id="3c336-240">Use the standard `Object.defineProperty` method to define the `fn.name` property.</span></span>  <span data-ttu-id="3c336-241">Para obtener más `fn.name` información, vaya [a Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span><span class="sxs-lookup"><span data-stu-id="3c336-241">To learn more about `fn.name`, navigate to [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span></span>  <span data-ttu-id="3c336-242">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [1177685][CR1177685].</span><span class="sxs-lookup"><span data-stu-id="3c336-242">To review the history of this feature in the Chromium open-source project, navigate to Issue [1177685][CR1177685].</span></span>  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Un ejemplo de la propiedad fn.name para controlar los nombres de depuración de las funciones" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   <span data-ttu-id="3c336-244">Un ejemplo de la `fn.name` propiedad para controlar los nombres de depuración de las funciones</span><span class="sxs-lookup"><span data-stu-id="3c336-244">An example of the `fn.name` property to control debug names for functions</span></span>  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a><span data-ttu-id="3c336-245">Vista de árbol de accesibilidad completa en la herramienta Elementos</span><span class="sxs-lookup"><span data-stu-id="3c336-245">Full accessibility tree view in the Elements tool</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="3c336-246">Este experimento proporciona una **vista de árbol de accesibilidad completa** en la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="3c336-246">This experiment provides a **full accessibility tree view** in the **Elements** tool.</span></span>  <span data-ttu-id="3c336-247">El [panel Accesibilidad][DevtoolsAccessibilityReferenceTheAccessibilityPane] proporciona una vista de árbol de accesibilidad parcial, que muestra la cadena antecesora directa del nodo raíz al nodo inspeccionado.</span><span class="sxs-lookup"><span data-stu-id="3c336-247">The [Accessibility][DevtoolsAccessibilityReferenceTheAccessibilityPane] pane provides a partial accessibility tree view, that displays the direct ancestor chain from the root node to the inspected node.</span></span>  
<span data-ttu-id="3c336-248">Después de activar este experimento y volver a cargar DevTools, elija uno de los siguientes botones para cambiar la pantalla en la herramienta Elementos para todos los elementos de la página web.</span><span class="sxs-lookup"><span data-stu-id="3c336-248">After you turn on this experiment and reload the DevTools, choose one of the following buttons to switch the display in the Elements tool for all elements on the webpage.</span></span>  

*   <span data-ttu-id="3c336-249">Para mostrar la vista de árbol de accesibilidad completa, elija la **vista Cambiar a árbol de accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="3c336-249">To display the full accessibility tree view , choose the **Switch to Accessibility Tree view**.</span></span>  
*   <span data-ttu-id="3c336-250">Para mostrar la vista de árbol DOM, elija **la vista Cambiar a árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="3c336-250">To display the DOM tree view, choose the **Switch to DOM Tree view**.</span></span>  
    
<span data-ttu-id="3c336-251">Para activar el experimento, vaya a Activar características [experimentales][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] y seleccione la casilla situada junto a Habilitar la vista de árbol **de accesibilidad completa en el panel Elementos**.</span><span class="sxs-lookup"><span data-stu-id="3c336-251">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkbox next to **Enable full accessibility tree view in Elements pane**.</span></span>  <span data-ttu-id="3c336-252">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya al problema [887173][CR887173].</span><span class="sxs-lookup"><span data-stu-id="3c336-252">To review the history of this feature in the Chromium open-source project, navigate to Issue [887173][CR887173].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Mostrar la vista de árbol DOM" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         <span data-ttu-id="3c336-254">Mostrar la **vista DOM**</span><span class="sxs-lookup"><span data-stu-id="3c336-254">Display the **DOM view**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Mostrar la vista de árbol de accesibilidad completa" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         <span data-ttu-id="3c336-256">Mostrar la **vista Árbol de accesibilidad completa**</span><span class="sxs-lookup"><span data-stu-id="3c336-256">Display the **Full Accessibility Tree view**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="3c336-257">Descargar los canales de vista previa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3c336-257">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="3c336-258">Si estás en Windows, Linux o macOS, considera usar los canales de vista previa [de Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3c336-258">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="3c336-259">Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="3c336-259">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="3c336-260">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3c336-260">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityReferenceTheAccessibilityPane]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#the-accessibility-pane "El panel Accesibilidad: referencia de accesibilidad | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterByLogLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nivel de registro: referencia de consola | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterMessages]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-messages "Filtrar mensajes: referencia de consola | Microsoft Docs"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console-sidebar "Abra la barra lateral de la consola: referencia de consola | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalización de métodos abreviados de teclado en las herramientas de desarrollo de Microsoft Edge | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#enable--button-tab-menus-to-open-more-tools "Habilitar los menús de la pestaña + botón para abrir más herramientas: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft Docs"  
[DevtoolsNetworkReferenceAddRemoveColumns]: /microsoft-edge/devtools-guide-chromium/network/reference#add-or-remove-columns "Agregar o quitar columnas: referencia de análisis de red | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#display-initiators-and-dependencies "Mostrar iniciadores y dependencias: referencia de análisis de red | Microsoft Docs"  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Información general de Aplicaciones web progresivas en Windows | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Extension Marketplace | Visual Studio código"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio código | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Mejora de la detección de soporte técnico sin conexión de Progressive Web App | Desarrolladores de Chrome"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "Consulta multimedia de gama de colores | Estado de la plataforma Chrome"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  
[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir la personalización de métodos abreviados de teclado o enlaces de clave | Errores de Chromium"  
[CR887173]: https://crbug.com/887173 "Problema 887173: DevTools: Inspección completa del árbol de accesibilidad | Errores de Chromium"  
[CR965802]: https://crbug.com/965802 "Problema 965802: Implementar la detección de funcionalidad sin conexión del trabajador del servicio más precisa | Errores de Chromium"  
[CR1073887]: https://crbug.com/1073887 "Problema 1073887: DevTools: @media (color-gamut: ...) colorspace emulation | Errores de Chromium"  
[CR1128885]: https://crbug.com/1128885 "Problema 1128885: Compatibilidad con DevTools para CORS-RFC1918 | Errores de Chromium"  
[CR1146450]: https://crbug.com/1146450 "Problema 1146450: [Android] Implementar las instalación de la hoja inferior | Errores de Chromium"  
[CR1158276]: https://crbug.com/1158276 "Problema 1158276: No se puede expandir o contratar el panel "Solicitar cadena de iniciador" mediante teclas de flecha en la sección "Red" de DevTools | Errores de Chromium"  
[CR1158827]: https://crbug.com/1158827 "Problema 1158827: [Directiva de permisos] Implementar la compatibilidad de devtool para la directiva de permisos | Errores de Chromium"  
[CR1160637]: https://crbug.com/1160637 "Problema 1160637: El foco en "Solicitar cadena de iniciador" se ve incompleto en la sección "Red" de la ventana "Herramientas de desarrollo" | Errores de Chromium"  
[CR1161427]: https://crbug.com/1161427 "Problema 1161427: &#9730; compatibilidad con la depuración de atributos de cookies sameparty en DevTools | Errores de Chromium"  
[CR1166710]: https://crbug.com/1166710 "Problema 1166710: activar el experimento de herramientas flexbox de forma predeterminada | Errores de Chromium"  
[CR1169689]: https://crbug.com/1169689 "Problema 1169689: La hoja inferior de instalación de PWA no debe incluir categorías | Errores de Chromium"  
[CR1175699]: https://crbug.com/1175699 "Problema 1175699: Editor de Flexbox | Errores de Chromium"  
[CR1177685]: https://crbug.com/1177685 "Problema 1177685: Quitar la compatibilidad con fn.displayName no estándar | Errores de Chromium"  
[CR1178530]: https://crbug.com/1178530 "Problema 1178530: la consola no se escapa a las comillas dobles al imprimir cadenas | Errores de Chromium"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Calidad de visualización de color: la característica "color-gamut" | Borradores del editor de grupo de trabajo css"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools: Interfaz de usuario del modo de enfoque: MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "Conjuntos de primera | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explicador de directivas de permisos | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> <span data-ttu-id="3c336-300">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3c336-300">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3c336-301">La página original se encuentra [aquí](https://developers.google.com/web/updates/2021/02/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="3c336-301">The original page is found [here](https://developers.google.com/web/updates/2021/02/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3c336-303">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3c336-303">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

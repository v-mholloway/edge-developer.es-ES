---
description: Combina los métodos abreviados de teclado Visual Studio código, emular Surface Duo y Samsung Galaxy Fold, mejoras de superposición de cuadrícula CSS y mucho más.
title: Novedades de DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a981c8b1a2658ba8cf771096e63001f7d6f69616
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408349"
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
# <a name="whats-new-in-devtools-microsoft-edge-86"></a><span data-ttu-id="81344-104">Novedades de DevTools (Microsoft Edge 86)</span><span class="sxs-lookup"><span data-stu-id="81344-104">What's New In DevTools (Microsoft Edge 86)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="81344-105">Anuncios del equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="81344-105">Announcements from the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <a name="match-keyboard-shortcuts-in-devtools-to-visual-studio-code"></a><span data-ttu-id="81344-106">Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio código</span><span class="sxs-lookup"><span data-stu-id="81344-106">Match keyboard shortcuts in DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="81344-107">En Microsoft Edge 86, puede hacer coincidir los métodos abreviados de teclado de DevTools con los accesos directos de [Microsoft Visual Studio Code][VisualStudioCode].</span><span class="sxs-lookup"><span data-stu-id="81344-107">In Microsoft Edge 86, you may match keyboard shortcuts in the DevTools to your shortcuts in [Microsoft Visual Studio Code][VisualStudioCode].</span></span>  

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio código" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   <span data-ttu-id="81344-109">Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio código</span><span class="sxs-lookup"><span data-stu-id="81344-109">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="81344-110">Para activar esta característica, vaya a [Personalizar métodos abreviados de teclado en Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="81344-110">To activate this feature, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  

<span data-ttu-id="81344-111">Por ejemplo, el método abreviado de teclado para pausar o continuar ejecutando un script [en Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] es `F5` .</span><span class="sxs-lookup"><span data-stu-id="81344-111">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="81344-112">Con el valor preestablecido **DevTools (predeterminado),** ese mismo acceso directo en DevTools es , pero cuando elige el valor preestablecido Visual Studio `F8` **Code,** ese acceso directo ahora también es `F5` .</span><span class="sxs-lookup"><span data-stu-id="81344-112">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8`, but when you choose the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="81344-113">Problema de [chromium #174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="81344-113">Chromium issue [#174309][CR174309]</span></span>  

### <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a><span data-ttu-id="81344-114">Emular Surface Duo y Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="81344-114">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="81344-116">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="81344-116">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="81344-117">Ahora puedes probar el aspecto de tu sitio web o aplicación en dos nuevos dispositivos:  [Surface Duo][MicrosoftSurfaceDevicesDuo] y Samsung [Galaxy Fold][SamsungMobileGalaxyFold] en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="81344-117">You are now able to test the look and feel of your website or app on two new devices:  [Surface Duo][MicrosoftSurfaceDevicesDuo] and [Samsung Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.</span></span>  

<span data-ttu-id="81344-118">Para ayudar a mejorar tu sitio web o aplicación para los dispositivos de pantalla doble y plegables, usa las siguientes características [al emular el dispositivo][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="81344-118">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="81344-119">[Spanning][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], que es cuando aparece el sitio web \(o aplicación\) en ambas pantallas.</span><span class="sxs-lookup"><span data-stu-id="81344-119">[Spanning][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>
*   <span data-ttu-id="81344-120">[Representación de la costura][DualScreenIntroductionHowWorkSeam], que es el espacio entre las dos pantallas.</span><span class="sxs-lookup"><span data-stu-id="81344-120">[Rendering the seam][DualScreenIntroductionHowWorkSeam], which is the space between the two screens.</span></span>
*   <span data-ttu-id="81344-121">[Habilitar las API experimentales de plataforma web][DevtoolsExperimentalFeaturesEnableExperimentalApis] para tener acceso a la nueva característica de pantalla multimedia [CSS][DualScreenWebCssMediaSpanning] y a la [API getWindowSegments de JavaScript.][DualScreenWebJavascriptGetwindowsegments]</span><span class="sxs-lookup"><span data-stu-id="81344-121">[Enabling experimental Web Platform APIs][DevtoolsExperimentalFeaturesEnableExperimentalApis] to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [JavaScript getWindowSegments API][DualScreenWebJavascriptGetwindowsegments].</span></span>  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Emulación de dispositivos para Surface Duo" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   <span data-ttu-id="81344-123">Emulación de dispositivos para Surface Duo</span><span class="sxs-lookup"><span data-stu-id="81344-123">Device emulation for Surface Duo</span></span>  
:::image-end:::  

<span data-ttu-id="81344-124">Para activar esta característica experimental, vaya a Activar características [experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla junto a **Emulación: Admitir modo de pantalla dual.**</span><span class="sxs-lookup"><span data-stu-id="81344-124">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Emulation: Support dual screen mode**.</span></span>  

<span data-ttu-id="81344-125">Para obtener más información acerca de este experimento, vaya [a Emulation: Support dual screen mode][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span><span class="sxs-lookup"><span data-stu-id="81344-125">For more information about this experiment, navigate to [Emulation: Support dual screen mode][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span></span>  

<span data-ttu-id="81344-126">Problema de Chromium: [#1054281][CR1054281]</span><span class="sxs-lookup"><span data-stu-id="81344-126">Chromium issue: [#1054281][CR1054281]</span></span>  

### <a name="css-grid-overlay-improvements-and-new-experimental-grid-features"></a><span data-ttu-id="81344-127">Mejoras de superposición de cuadrícula CSS y nuevas características de cuadrícula experimental</span><span class="sxs-lookup"><span data-stu-id="81344-127">CSS grid overlay improvements and new experimental grid features</span></span>  

<span data-ttu-id="81344-128">Gracias por los comentarios positivos sobre las superposiciones de cuadrícula CSS mejoradas.</span><span class="sxs-lookup"><span data-stu-id="81344-128">Thank you for the positive feedback about the improved CSS grid overlays.</span></span>  <span data-ttu-id="81344-129">Las superposiciones de cuadrícula CSS ahora están habilitadas de forma predeterminada y no requieren que actives un experimento.</span><span class="sxs-lookup"><span data-stu-id="81344-129">The CSS grid overlays are now enabled by default and do not require you to turn on an experiment.</span></span>  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Superposición de cuadrícula CSS para elemento de artículo" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   <span data-ttu-id="81344-131">Superposición de cuadrícula CSS para `article` elemento</span><span class="sxs-lookup"><span data-stu-id="81344-131">CSS grid overlay for `article` element</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="81344-132">Para obtener más información acerca de las superposiciones de cuadrícula, vaya a [Características de depuración de][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]cuadrícula CSS .</span><span class="sxs-lookup"><span data-stu-id="81344-132">For more information about grid overlays, navigate to [CSS grid debugging features][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="81344-133">El equipo de Microsoft Edge DevTools y el equipo de Chrome DevTools colaboran en características adicionales.</span><span class="sxs-lookup"><span data-stu-id="81344-133">The Microsoft Edge DevTools team and the Chrome DevTools team collaborate on additional features.</span></span>  <span data-ttu-id="81344-134">Las nuevas características incluyen varias superposiciones que son persistentes y configurables desde un nuevo panel **Diseño** de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="81344-134">The new features include multiple overlays that are persistent and configurable from a new **Layout** pane on the **Elements** tool.</span></span>  

<span data-ttu-id="81344-135">Para activar esta característica experimental, vaya a Activar características [experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla situada junto a Habilitar nuevas características de depuración **de css grid (opciones**de configuración disponibles en el panel de la barra lateral Diseño en Elementos después del reinicio).</span><span class="sxs-lookup"><span data-stu-id="81344-135">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)**.</span></span>  

<span data-ttu-id="81344-136">Para obtener más información acerca de este experimento, vaya [a Habilitar nuevas características de depuración de cuadrícula CSS][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span><span class="sxs-lookup"><span data-stu-id="81344-136">For more information about this experiment, navigate to [Enable new CSS grid debugging features][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="81344-137">Problema de Chromium: [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="81344-137">Chromium issue: [#1047356][CR1047356]</span></span>  

### <a name="table-copied-from-the-console-preserves-formatting"></a><span data-ttu-id="81344-138">La tabla copiada desde la consola conserva el formato</span><span class="sxs-lookup"><span data-stu-id="81344-138">Table copied from the Console preserves formatting</span></span>  

<span data-ttu-id="81344-139">En Microsoft Edge 85 o versiones anteriores, se perdió el formato de una `console.table` copiada.</span><span class="sxs-lookup"><span data-stu-id="81344-139">In Microsoft Edge 85 or earlier, the formatting of a copied `console.table` was lost.</span></span>  <span data-ttu-id="81344-140">Si copió el resultado [][DevtoolsConsoleApiTable] de la API de consola de la tabla y la pega, solo se guardó el texto de la tabla.</span><span class="sxs-lookup"><span data-stu-id="81344-140">If you copied the output from the [table][DevtoolsConsoleApiTable] Console API, and pasted it, only the text of the table was kept.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Resultado de la API de consola de tabla en Microsoft Edge 85 o versiones anteriores" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` <span data-ttu-id="81344-142">Salida de la API de consola en Microsoft Edge 85 o versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="81344-142">Console API output in Microsoft Edge 85 or earlier</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="table Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="81344-144">Salida de la API de consola de Microsoft Edge 85 o anterior pegada en Visual Studio código</span><span class="sxs-lookup"><span data-stu-id="81344-144">Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="81344-145">En Microsoft Edge 86 o posterior, al copiar una tabla desde la **consola,** el formato se conserva ahora.</span><span class="sxs-lookup"><span data-stu-id="81344-145">In Microsoft Edge 86 or later, when you copy a table from the **Console**, the formatting is now preserved.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Resultado de la API de consola de tabla en Microsoft Edge 86 o posterior" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` <span data-ttu-id="81344-147">Salida de la API de consola en Microsoft Edge 86 o posterior</span><span class="sxs-lookup"><span data-stu-id="81344-147">Console API output in Microsoft Edge 86 or later</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="table Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="81344-149">Salida de la API de consola de Microsoft Edge 86 o posterior pegada en Visual Studio código</span><span class="sxs-lookup"><span data-stu-id="81344-149">Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="81344-150">Problema de Chromium: [#1115011][CR1115011]</span><span class="sxs-lookup"><span data-stu-id="81344-150">Chromium issue: [#1115011][CR1115011]</span></span>  

### <a name="source-order-viewer-for-easier-accessibility-testing"></a><span data-ttu-id="81344-151">Visor de pedidos de origen para pruebas de accesibilidad más fáciles</span><span class="sxs-lookup"><span data-stu-id="81344-151">Source Order Viewer for easier accessibility testing</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="81344-153">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="81344-153">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="81344-154">La nueva aplicación auxiliar de accesibilidad muestra el orden de los elementos en el origen.</span><span class="sxs-lookup"><span data-stu-id="81344-154">The new accessibility helper displays the order of elements in the source.</span></span>  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Activar Mostrar orden de origen" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   <span data-ttu-id="81344-156">Activar **Mostrar orden de origen**</span><span class="sxs-lookup"><span data-stu-id="81344-156">Activate **Show source order**</span></span>  
:::image-end:::  

<span data-ttu-id="81344-157">Esta característica facilita la prueba de la forma en que los usuarios del lector de pantalla y el teclado experimentan su sitio web o aplicación.</span><span class="sxs-lookup"><span data-stu-id="81344-157">This feature makes it easier to test the way screen reader and keyboard users experience your website or app.</span></span>  <span data-ttu-id="81344-158">Los lectores de pantalla y la navegación por teclado dependen de que el contenido se coloque en un orden determinado en el código fuente de su sitio web o aplicación, de modo que coincida con la página representada.</span><span class="sxs-lookup"><span data-stu-id="81344-158">Screen readers and keyboard navigation depend on content being placed in a particular order in the source code of your website or app, so that it matches the rendered page.</span></span>  <span data-ttu-id="81344-159">El Visor de pedidos de origen muestra posibles diferencias de orden entre la página representada y el código fuente.</span><span class="sxs-lookup"><span data-stu-id="81344-159">The Source Order Viewer displays potential differences in order between the rendered page and the source code.</span></span>  

<span data-ttu-id="81344-160">Para activar esta característica experimental, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla situada junto a Habilitar visor **de pedidos de origen**.</span><span class="sxs-lookup"><span data-stu-id="81344-160">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Source Order Viewer**.</span></span>  

<span data-ttu-id="81344-161">Para obtener más información acerca de este experimento, vaya a [Habilitar el Visor de pedidos de origen][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span><span class="sxs-lookup"><span data-stu-id="81344-161">For more information about this experiment, navigate to [Enable Source Order Viewer][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span></span>  

<span data-ttu-id="81344-162">Problema de Chromium: [#1094406][CR1094406]</span><span class="sxs-lookup"><span data-stu-id="81344-162">Chromium issue: [#1094406][CR1094406]</span></span>  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Microsoft Edge DevTools in Traditional Chinese" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Microsoft Edge DevTools in Japanese" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <a name="highlight-all-search-results-in-elements-tool"></a><span data-ttu-id="81344-163">Resaltar todos los resultados de búsqueda en la herramienta Elementos</span><span class="sxs-lookup"><span data-stu-id="81344-163">Highlight all search results in Elements tool</span></span>  

<span data-ttu-id="81344-164">En Microsoft Edge 84 y 85, no se resaltó el primer resultado de búsqueda en **la herramienta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="81344-164">In Microsoft Edge 84 and 85, the first search result in the **Elements** tool did not highlight.</span></span>  <span data-ttu-id="81344-165">Los resultados de búsqueda restantes se resaltaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="81344-165">The remaining search results were highlighted correctly.</span></span>  

<span data-ttu-id="81344-166">Gracias por enviar sus comentarios y ayudar a mejorar Chromium.</span><span class="sxs-lookup"><span data-stu-id="81344-166">Thank you for sending your feedback and helping improve Chromium.</span></span>  <span data-ttu-id="81344-167">Sus comentarios revelaron el [problema #1103316][CR1103316] en el proyecto chromium de código abierto.</span><span class="sxs-lookup"><span data-stu-id="81344-167">Your feedback uncovered Issue [#1103316][CR1103316] in the open-source Chromium project.</span></span>  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Primer resultado de búsqueda resaltado en el panel Elementos de Microsoft Edge 84 o posterior" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   <span data-ttu-id="81344-169">Primer resultado de búsqueda resaltado en **la herramienta Elements** en Microsoft Edge 84 o posterior</span><span class="sxs-lookup"><span data-stu-id="81344-169">Highlighted first search result on **Elements** tool in Microsoft Edge 84 or later</span></span>  
:::image-end:::  

<span data-ttu-id="81344-170">El problema ahora se soluciona en todas las versiones de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="81344-170">The issue is now fixed in all versions of Microsoft Edge.</span></span>  

<span data-ttu-id="81344-171">Problema de Chromium: [#1103316][CR1103316]</span><span class="sxs-lookup"><span data-stu-id="81344-171">Chromium issue: [#1103316][CR1103316]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="81344-172">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="81344-172">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-media-tool"></a><span data-ttu-id="81344-173">Nueva herramienta multimedia</span><span class="sxs-lookup"><span data-stu-id="81344-173">New Media tool</span></span>  

<span data-ttu-id="81344-174">Ahora DevTools muestra información de reproductores multimedia en la [herramienta][DevtoolsMediaPanelIndex] Multimedia.</span><span class="sxs-lookup"><span data-stu-id="81344-174">DevTools now displays media players information in the [Media][DevtoolsMediaPanelIndex] tool.</span></span>  

<span data-ttu-id="81344-175">Para abrir la nueva **herramienta Multimedia,** complete el siguiente paso.</span><span class="sxs-lookup"><span data-stu-id="81344-175">To open the new **Media** tool, complete the following step.</span></span>  

1.  <span data-ttu-id="81344-176">Elija **Personalizar y controlar DevTools** \( `...` \) > Más herramientas \*\*\*\*  >  **Multimedia**.</span><span class="sxs-lookup"><span data-stu-id="81344-176">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Nueva herramienta multimedia" lightbox="../../media/2020/08/media-panel.msft.png":::
       <span data-ttu-id="81344-178">Nueva **herramienta multimedia**</span><span class="sxs-lookup"><span data-stu-id="81344-178">New **Media** tool</span></span>  
    :::image-end:::  

<span data-ttu-id="81344-179">Antes de la nueva **herramienta Multimedia** en DevTools, la información de registro y depuración sobre los reproductores de vídeo se encontraba en la configuración **Reproductores recientes.**</span><span class="sxs-lookup"><span data-stu-id="81344-179">Before the new **Media** tool in DevTools, the logging and debug information about video players was located under the **Recent Players** setting.</span></span>  <span data-ttu-id="81344-180">Para abrir la configuración **Jugadores recientes,** vaya a `edge://media-internals` y elija la herramienta **Jugadores.**</span><span class="sxs-lookup"><span data-stu-id="81344-180">To open the **Recent Players** setting, navigate to `edge://media-internals` and choose the **Players** tool.</span></span>  

<span data-ttu-id="81344-181">Vea contenido dinámico e inspeccione los posibles problemas más rápidamente, incluidos los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="81344-181">View live content and inspect potential issues more quickly, including the following examples.</span></span>  

*   <span data-ttu-id="81344-182">¿Por qué se descartan fotogramas?</span><span class="sxs-lookup"><span data-stu-id="81344-182">Why frames are dropped?</span></span>  
*   <span data-ttu-id="81344-183">¿Por qué JavaScript interactúa con el jugador de forma inesperada?</span><span class="sxs-lookup"><span data-stu-id="81344-183">Why JavaScript is interacting with the player in an unexpected way?</span></span>  

### <a name="capture-node-screenshots-using-the-elements-tool-context-menu"></a><span data-ttu-id="81344-184">Capturar capturas de pantalla de nodo con el menú contextual de la herramienta Elementos</span><span class="sxs-lookup"><span data-stu-id="81344-184">Capture node screenshots using the Elements tool context menu</span></span>  

<span data-ttu-id="81344-185">Ahora puede capturar capturas de pantalla de nodo mediante el menú contextual de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="81344-185">You may now capture node screenshots using the context menu in the **Elements** tool.</span></span>  

<span data-ttu-id="81344-186">Por ejemplo, para realizar una captura de pantalla de la tabla de contenido, mantenga el mouse en el elemento, abra el menú contextual \(hacer clic con el botón secundario\) y seleccione Capturar captura de pantalla **del nodo**.</span><span class="sxs-lookup"><span data-stu-id="81344-186">For example, to take a screenshot of the table of contents, hover on the element, open the contextual menu \(right-click\), and select **Capture node screenshot**.</span></span>  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Capturar capturas de pantalla de nodo" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   <span data-ttu-id="81344-188">Capturar capturas de pantalla de nodo</span><span class="sxs-lookup"><span data-stu-id="81344-188">Capture node screenshots</span></span>  
:::image-end:::  

<span data-ttu-id="81344-189">Problema de Chromium: [#1100253][CR1100253]</span><span class="sxs-lookup"><span data-stu-id="81344-189">Chromium issue: [#1100253][CR1100253]</span></span>  

### <a name="issues-tool-updates"></a><span data-ttu-id="81344-190">Problemas de actualizaciones de herramientas</span><span class="sxs-lookup"><span data-stu-id="81344-190">Issues tool updates</span></span>  

<span data-ttu-id="81344-191">La barra de advertencia Problemas de la **herramienta Consola** ahora se reemplaza por un mensaje normal.</span><span class="sxs-lookup"><span data-stu-id="81344-191">The Issues warning bar on the **Console** tool is now replaced with a regular message.</span></span>  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Problemas en el mensaje de consola" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   <span data-ttu-id="81344-193">Problemas en el mensaje de consola</span><span class="sxs-lookup"><span data-stu-id="81344-193">Issues in console message</span></span>  
:::image-end:::  

<span data-ttu-id="81344-194">Los problemas de cookies de terceros ahora están ocultos de forma predeterminada en la **herramienta** Problemas.</span><span class="sxs-lookup"><span data-stu-id="81344-194">Third-party cookie issues are now hidden by default in the **Issues** tool.</span></span>  <span data-ttu-id="81344-195">Habilite la nueva **casilla Incluir problemas de cookies de** terceros para ver los problemas.</span><span class="sxs-lookup"><span data-stu-id="81344-195">Enable the new **Include third-party cookie issues** checkbox to view the issues.</span></span>  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Casilla de verificación problemas de cookies de terceros" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   <span data-ttu-id="81344-197">Casilla de verificación problemas de cookies de terceros</span><span class="sxs-lookup"><span data-stu-id="81344-197">third-party cookie issues checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="81344-198">Problemas de cromo: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span><span class="sxs-lookup"><span data-stu-id="81344-198">Chromium issues: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span></span>  

### <a name="emulate-missing-local-fonts"></a><span data-ttu-id="81344-199">Emular fuentes locales que faltan</span><span class="sxs-lookup"><span data-stu-id="81344-199">Emulate missing local fonts</span></span>  

<span data-ttu-id="81344-200">Abra la [herramienta de representación y][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] use la nueva característica Deshabilitar fuentes **locales** para emular los orígenes que faltan en `local()` las `@font-face` reglas.</span><span class="sxs-lookup"><span data-stu-id="81344-200">Open the [Rendering tool][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] and use the new **Disable local fonts** feature to emulate missing `local()` sources in `@font-face` rules.</span></span>  

<span data-ttu-id="81344-201">Por ejemplo, cuando la fuente está instalada en el dispositivo y la regla la usa como fuente, Microsoft Edge usa el archivo de fuente `Rubik` `@font-face src` local del `local()` dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81344-201">For example, when the `Rubik` font is installed on your device and the `@font-face src` rule uses it as a `local()` font, Microsoft Edge uses the local font file from your device.</span></span>  

<span data-ttu-id="81344-202">Cuando **se habilita Deshabilitar fuentes** locales, DevTools omite las fuentes y captura cada una de la `local()` red.</span><span class="sxs-lookup"><span data-stu-id="81344-202">When **Disable local fonts** is enabled, DevTools ignores the `local()` fonts and fetches each from the network.</span></span>  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Emular fuentes locales que faltan" lightbox="../../media/2020/08/disable-font.msft.png":::
   <span data-ttu-id="81344-204">Emular fuentes locales que faltan</span><span class="sxs-lookup"><span data-stu-id="81344-204">Emulate missing local fonts</span></span>  
:::image-end:::  

<span data-ttu-id="81344-205">Si usa dos copias diferentes de la misma fuente durante el desarrollo, como los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="81344-205">If you use two different copies of the same font during development, such as the following examples.</span></span>  

*   <span data-ttu-id="81344-206">Una fuente local para las herramientas de diseño.</span><span class="sxs-lookup"><span data-stu-id="81344-206">A local font for your design tools.</span></span>  
*   <span data-ttu-id="81344-207">Una fuente web para el código.</span><span class="sxs-lookup"><span data-stu-id="81344-207">A web font for your code.</span></span>  

<span data-ttu-id="81344-208">Use **Deshabilitar fuentes locales** para facilitar la realización de las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="81344-208">Use **Disable local fonts** to make it easier for you to complete the following tasks.</span></span>  

*   <span data-ttu-id="81344-209">Depurar y medir el rendimiento de carga y optimización de fuentes web.</span><span class="sxs-lookup"><span data-stu-id="81344-209">Debug and measure loading performance and optimization of web fonts.</span></span>  
*   <span data-ttu-id="81344-210">Compruebe la precisión de las reglas `@font-face` CSS.</span><span class="sxs-lookup"><span data-stu-id="81344-210">Verify accuracy of your CSS `@font-face` rules.</span></span>  
*   <span data-ttu-id="81344-211">Descubra las diferencias entre las versiones locales instaladas en el dispositivo y una fuente web.</span><span class="sxs-lookup"><span data-stu-id="81344-211">Discover differences between local versions installed on your device and a web font.</span></span>  

<span data-ttu-id="81344-212">Problema de Chromium: [#384968][CR384968]</span><span class="sxs-lookup"><span data-stu-id="81344-212">Chromium issue: [#384968][CR384968]</span></span>  

### <a name="emulate-inactive-users"></a><span data-ttu-id="81344-213">Emular usuarios inactivos</span><span class="sxs-lookup"><span data-stu-id="81344-213">Emulate inactive users</span></span>  

<span data-ttu-id="81344-214">La [API de detección de][WebDevIdleDetection] inactividad permite a los desarrolladores detectar usuarios inactivos y reaccionar en los cambios de estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="81344-214">The [Idle Detection API][WebDevIdleDetection] allows developers to detect inactive users and react on idle state changes.</span></span>  <span data-ttu-id="81344-215">Ahora puede usar DevTools para emular los \*\*\*\* cambios de estado de inactividad en la herramienta Sensores tanto para el estado de usuario como para el estado de pantalla en lugar de esperar a que cambie el estado de inactividad real.</span><span class="sxs-lookup"><span data-stu-id="81344-215">You are now able to use DevTools to emulate idle state changes in the **Sensors** tool for both the user state and the screen state instead of waiting for the actual idle state to change.</span></span>  <span data-ttu-id="81344-216">Puede abrir la herramienta **Sensores** desde el [cajón][DevtoolsCustomizeIndexDrawer].</span><span class="sxs-lookup"><span data-stu-id="81344-216">You may open the **Sensors** tool from the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Emular usuarios inactivos" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   <span data-ttu-id="81344-218">Emular usuarios inactivos</span><span class="sxs-lookup"><span data-stu-id="81344-218">Emulate inactive users</span></span>  
:::image-end:::  

<span data-ttu-id="81344-219">Problema de Chromium: [#1090802][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="81344-219">Chromium issue: [#1090802][CR1090802]</span></span>  

### <a name="emulate-prefers-reduced-data"></a><span data-ttu-id="81344-220">Emular prefers-reduced-data</span><span class="sxs-lookup"><span data-stu-id="81344-220">Emulate prefers-reduced-data</span></span>  

> [!NOTE]
> <span data-ttu-id="81344-221">En Microsoft Edge 86, para habilitar esta característica, vaya a y active la marca características de plataforma `edge://flags#enable-experimental-web-platform-features` **web experimental.**</span><span class="sxs-lookup"><span data-stu-id="81344-221">In Microsoft Edge 86, to enable this feature, navigate to `edge://flags#enable-experimental-web-platform-features` and turn on the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="81344-222">La opción de emulación solo se muestra si la marca está habilitada.</span><span class="sxs-lookup"><span data-stu-id="81344-222">The emulation option is only displayed if the flag is enabled.</span></span>  

<span data-ttu-id="81344-223">La [consulta multimedia prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] detecta las preferencias de contenido del usuario para los datos reducidos.</span><span class="sxs-lookup"><span data-stu-id="81344-223">The [prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] media query detects user content preferences for reduced data.</span></span>  <span data-ttu-id="81344-224">Si se selecciona, el usuario recibe contenido de página alternativo que usa menos datos.</span><span class="sxs-lookup"><span data-stu-id="81344-224">If selected, the user receives alternate page content that uses less data.</span></span>  

<span data-ttu-id="81344-225">Ahora puede usar DevTools para emular la `prefers-reduced-data` consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="81344-225">You may now use DevTools to emulate the `prefers-reduced-data` media query.</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Emular prefers-reduced-data" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   <span data-ttu-id="81344-227">Emular prefers-reduced-data</span><span class="sxs-lookup"><span data-stu-id="81344-227">Emulate prefers-reduced-data</span></span>  
:::image-end:::  

<span data-ttu-id="81344-228">Problema de Chromium: [#1096068][CR1096068]</span><span class="sxs-lookup"><span data-stu-id="81344-228">Chromium issue: [#1096068][CR1096068]</span></span>  

### <a name="support-for-new-javascript-features"></a><span data-ttu-id="81344-229">Compatibilidad con nuevas características de JavaScript</span><span class="sxs-lookup"><span data-stu-id="81344-229">Support for new JavaScript features</span></span>  

<span data-ttu-id="81344-230">DevTools ahora admite mejor las siguientes características del lenguaje JavaScript.</span><span class="sxs-lookup"><span data-stu-id="81344-230">DevTools now have better supported the following JavaScript language features.</span></span>  

| <span data-ttu-id="81344-231">Característica de lenguaje JavaScript</span><span class="sxs-lookup"><span data-stu-id="81344-231">JavaScript language feature</span></span> | <span data-ttu-id="81344-232">Detalles</span><span class="sxs-lookup"><span data-stu-id="81344-232">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="81344-233">Operadores de asignación lógica</span><span class="sxs-lookup"><span data-stu-id="81344-233">Logical assignment operators</span></span>][V8FeaturesLogicalAssignment] | <span data-ttu-id="81344-234">DevTools ahora admite la asignación lógica con los `&&=` nuevos operadores , y en las herramientas `||=` `??=` **Consola** **y** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="81344-234">DevTools now supports logical assignment with the new `&&=`, `||=`, and `??=` operators in the **Console** and **Sources** tools.</span></span>  |  
| <span data-ttu-id="81344-235">Separadores [numéricos de impresión bastante][V8FeaturesNumericSeparators]</span><span class="sxs-lookup"><span data-stu-id="81344-235">Pretty-print [numeric separators][V8FeaturesNumericSeparators]</span></span> | <span data-ttu-id="81344-236">Ahora DevTools imprime correctamente los separadores numéricos en la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="81344-236">DevTools now properly pretty-prints the numeric separators in the **Sources** tool.</span></span>  |  

<span data-ttu-id="81344-237">Problemas de cromo: [1086817][CR1086817], [1080569][CR1080569]</span><span class="sxs-lookup"><span data-stu-id="81344-237">Chromium issues: [1086817][CR1086817], [1080569][CR1080569]</span></span>  

### <a name="lighthouse-62-in-the-lighthouse-panel"></a><span data-ttu-id="81344-238">Faro 6.2 en el panel Faro</span><span class="sxs-lookup"><span data-stu-id="81344-238">Lighthouse 6.2 in the Lighthouse panel</span></span>  

<span data-ttu-id="81344-239">Ahora, **la herramienta Lighthouse** está ejecutando Lighthouse 6.2.</span><span class="sxs-lookup"><span data-stu-id="81344-239">The **Lighthouse** tool is now running Lighthouse 6.2.</span></span>  <span data-ttu-id="81344-240">Para obtener una lista completa de los cambios, vaya a las notas [de la versión de Lighthouse][GithubGooglechromeLighthouseV620].</span><span class="sxs-lookup"><span data-stu-id="81344-240">For a full list of changes, navigate to the [Lighthouse release notes][GithubGooglechromeLighthouseV620].</span></span>  

<span data-ttu-id="81344-241">Problema de Chromium: [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="81344-241">Chromium issue: [#772558][CR772558]</span></span>  

### <a name="deprecation-of-other-origins-listing-in-the-service-workers-pane"></a><span data-ttu-id="81344-242">Desuso de la descripción de otros orígenes en el panel Trabajadores de servicio</span><span class="sxs-lookup"><span data-stu-id="81344-242">Deprecation of other origins listing in the Service Workers pane</span></span>  

<span data-ttu-id="81344-243">DevTools ahora proporciona un vínculo desde el panel **Trabajadores** de servicio**\(** Herramienta de aplicación > Panel de trabajadores **de** servicio\) para ver la lista completa de trabajadores de servicio de otros orígenes.</span><span class="sxs-lookup"><span data-stu-id="81344-243">DevTools now provides a link from the **Service workers** pane \(**Application** tool > **Service workers** pane\) to view the full list of service workers from other origins.</span></span>  <span data-ttu-id="81344-244">Para obtener acceso a la lista sin abrir DevTools, vaya a `edge://service-worker-internals/?devtools` .</span><span class="sxs-lookup"><span data-stu-id="81344-244">To access the list without opening the DevTools, navigate to `edge://service-worker-internals/?devtools`.</span></span>  

<span data-ttu-id="81344-245">Anteriormente, DevTools muestra una lista anidada en el panel **DevTools** > **DevTools.**</span><span class="sxs-lookup"><span data-stu-id="81344-245">Previously DevTools displayed a list nested under the **Application** tool > **Service workers** pane.</span></span>  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Vínculo a otros orígenes" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   <span data-ttu-id="81344-247">Vínculo a otros orígenes</span><span class="sxs-lookup"><span data-stu-id="81344-247">Link to other origins</span></span>  
:::image-end:::  

<span data-ttu-id="81344-248">Problema de Chromium: [#807440][CR807440]</span><span class="sxs-lookup"><span data-stu-id="81344-248">Chromium issue: [#807440][CR807440]</span></span>  

### <a name="show-coverage-summary-for-filtered-items"></a><span data-ttu-id="81344-249">Mostrar resumen de cobertura para elementos filtrados</span><span class="sxs-lookup"><span data-stu-id="81344-249">Show coverage summary for filtered items</span></span>  

<span data-ttu-id="81344-250">DevTools ahora vuelve a calcular y mostrar un resumen de la información de cobertura dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="81344-250">DevTools now recalculate and display a summary of coverage information dynamically.</span></span>  <span data-ttu-id="81344-251">La pantalla dinámica se desencadena cuando se aplican filtros en la [herramienta Cobertura.][DevtoolsCoverageIndex]</span><span class="sxs-lookup"><span data-stu-id="81344-251">The dynamic display is triggered when filters are applied in the [Coverage][DevtoolsCoverageIndex] tool.</span></span>  <span data-ttu-id="81344-252">Antes de **que la herramienta** Cobertura siempre mostrara un resumen de toda la información de cobertura.</span><span class="sxs-lookup"><span data-stu-id="81344-252">Before the **Coverage** tool always displayed a summary of all coverage information.</span></span>  

<span data-ttu-id="81344-253">En la primera de las siguientes figuras, el resumen se muestra inicialmente y, en la segunda de las siguientes cifras, el resumen se muestra después de aplicar el filtrado `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` CSS.</span><span class="sxs-lookup"><span data-stu-id="81344-253">In the first of the following figures, the summary initially displays `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` and in the second of the following figures, the summary displays `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` after CSS filtering is applied.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Resumen de cobertura" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         <span data-ttu-id="81344-255">Resumen de cobertura</span><span class="sxs-lookup"><span data-stu-id="81344-255">Coverage summary</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Resumen de cobertura para elementos filtrados" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         <span data-ttu-id="81344-257">Resumen de cobertura para elementos filtrados</span><span class="sxs-lookup"><span data-stu-id="81344-257">Coverage summary for filtered items</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="81344-258">Problema de Chromium: [#1061385][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="81344-258">Chromium issue: [#1061385][CR1090802]</span></span>  

### <a name="new-frame-details-view-in-application-panel"></a><span data-ttu-id="81344-259">Nueva vista detalles del marco en el panel Aplicación</span><span class="sxs-lookup"><span data-stu-id="81344-259">New frame details view in Application panel</span></span>  

<span data-ttu-id="81344-260">DevTools ahora muestra una vista detallada para cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="81344-260">DevTools now show a detailed view for each frame.</span></span>  <span data-ttu-id="81344-261">Para acceder a él, elija un marco en el **menú Marcos** de la **herramienta** Aplicación.</span><span class="sxs-lookup"><span data-stu-id="81344-261">To access it, choose a frame under the **Frames** menu in the **Application** tool.</span></span>  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Nueva vista detallada para un marco en el panel Aplicación" lightbox="../../media/2020/08/frame-details.msft.png":::
   <span data-ttu-id="81344-263">Nueva vista detallada para un marco en **la herramienta Aplicación**</span><span class="sxs-lookup"><span data-stu-id="81344-263">New detailed view for a frame in **Application** tool</span></span>  
:::image-end:::  

<span data-ttu-id="81344-264">Problema de Chromium: [#1093247][CR1093247]</span><span class="sxs-lookup"><span data-stu-id="81344-264">Chromium issue: [#1093247][CR1093247]</span></span>  

#### <a name="frame-details-for-opened-windows"></a><span data-ttu-id="81344-265">Detalles del marco para ventanas abiertas</span><span class="sxs-lookup"><span data-stu-id="81344-265">Frame details for opened windows</span></span>  

<span data-ttu-id="81344-266">Las ventanas abiertas y las ventanas emergentes ahora también se muestran debajo del árbol de marcos.</span><span class="sxs-lookup"><span data-stu-id="81344-266">Open windows and pop-up windows now display under the frame tree as well.</span></span>  <span data-ttu-id="81344-267">La vista detallada de las ventanas abiertas incluye información de seguridad adicional.</span><span class="sxs-lookup"><span data-stu-id="81344-267">The detailed view of the opened windows includes additional security information.</span></span>  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Nueva vista detallada de fotogramas para ventanas abiertas" lightbox="../../media/2020/08/window-opener.msft.png":::
   <span data-ttu-id="81344-269">Nueva vista detallada de fotogramas para ventanas abiertas</span><span class="sxs-lookup"><span data-stu-id="81344-269">New frame detailed view for opened windows</span></span>  
:::image-end:::  

<span data-ttu-id="81344-270">Problema de Chromium: [#1107766][CR1107766]</span><span class="sxs-lookup"><span data-stu-id="81344-270">Chromium issue: [#1107766][CR1107766]</span></span>  

#### <a name="security-and-isolation-information"></a><span data-ttu-id="81344-271">Información de seguridad y aislamiento</span><span class="sxs-lookup"><span data-stu-id="81344-271">Security and isolation information</span></span>  

<span data-ttu-id="81344-272">Contexto seguro, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep]y [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] ahora se muestran en los detalles del marco.</span><span class="sxs-lookup"><span data-stu-id="81344-272">Secure context, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep], and [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] are now displayed in the frame details.</span></span>  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Información de seguridad y aislamiento" lightbox="../../media/2020/08/coep-coop.msft.png":::
   <span data-ttu-id="81344-274">Información de seguridad y aislamiento</span><span class="sxs-lookup"><span data-stu-id="81344-274">Security and isolation information</span></span>  
:::image-end:::  

<span data-ttu-id="81344-275">En el futuro, el equipo de DevTools de Microsoft Edge y el equipo de Chrome DevTools planean agregar más información de seguridad a los detalles del marco.</span><span class="sxs-lookup"><span data-stu-id="81344-275">In the future, the Microsoft Edge DevTools team and the Chrome DevTools team are planning to add more security information to the frame details.</span></span>  

<span data-ttu-id="81344-276">Problema de Chromium: [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="81344-276">Chromium issue: [#1051466][CR1051466]</span></span>  

### <a name="elements-and-network-panel-updates"></a><span data-ttu-id="81344-277">Actualizaciones de elementos y panel de red</span><span class="sxs-lookup"><span data-stu-id="81344-277">Elements and Network panel updates</span></span>  

#### <a name="accessible-color-suggestion-in-the-styles-pane"></a><span data-ttu-id="81344-278">Sugerencia de color accesible en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="81344-278">Accessible color suggestion in the Styles pane</span></span>  

<span data-ttu-id="81344-279">DevTools ahora proporciona sugerencias de color para texto de contraste de color bajo.</span><span class="sxs-lookup"><span data-stu-id="81344-279">DevTools now provides color suggestions for low color contrast text.</span></span>  

<span data-ttu-id="81344-280">En el ejemplo siguiente, `h1` tiene texto de contraste bajo.</span><span class="sxs-lookup"><span data-stu-id="81344-280">In the example below, `h1` has low contrast text.</span></span>  <span data-ttu-id="81344-281">Para corregirlo, abra el selector de color de la `color` propiedad en el panel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="81344-281">To fix it, open the color picker of the `color` property in the **Styles** pane.</span></span>  <span data-ttu-id="81344-282">Después de expandir la **sección Relación de contraste,** DevTools proporciona sugerencias de color AAA y AA.</span><span class="sxs-lookup"><span data-stu-id="81344-282">After you expand the **Contrast ratio** section, DevTools provides AA and AAA color suggestions.</span></span>  <span data-ttu-id="81344-283">Elija el color sugerido para aplicar el color.</span><span class="sxs-lookup"><span data-stu-id="81344-283">Choose the suggested color to apply the color.</span></span>  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="El selector de colores sugiere sugerencias de color AAA y AA" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   <span data-ttu-id="81344-285">El selector de colores sugiere sugerencias de color AAA y AA</span><span class="sxs-lookup"><span data-stu-id="81344-285">Color picker suggests AA and AAA color suggestions</span></span>  
:::image-end:::  

<span data-ttu-id="81344-286">Problema de Chromium: [#1093227][CR1093227]</span><span class="sxs-lookup"><span data-stu-id="81344-286">Chromium issue: [#1093227][CR1093227]</span></span>  

#### <a name="reinstate-properties-pane-in-the-elements-panel"></a><span data-ttu-id="81344-287">Reinstaurar el panel Propiedades en el panel Elementos</span><span class="sxs-lookup"><span data-stu-id="81344-287">Reinstate Properties pane in the Elements panel</span></span>  

<span data-ttu-id="81344-288">El **panel Propiedades** ha vuelto.</span><span class="sxs-lookup"><span data-stu-id="81344-288">The **Properties** pane is back.</span></span>  <span data-ttu-id="81344-289">Estaba en [desuso en Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span><span class="sxs-lookup"><span data-stu-id="81344-289">It was [deprecated in Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span></span>  <span data-ttu-id="81344-290">El equipo de Microsoft Edge DevTools y el equipo de Chrome DevTools están planeando mejoras para inspeccionar las propiedades de los elementos.</span><span class="sxs-lookup"><span data-stu-id="81344-290">The Microsoft Edge DevTools team and the Chrome DevTools team are planning improvements for inspecting properties of elements.</span></span>  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Panel Propiedades en el panel Elementos" lightbox="../../media/2020/08/properties-pane.msft.png":::
   <span data-ttu-id="81344-292">**Panel Propiedades** de la **herramienta** Elementos</span><span class="sxs-lookup"><span data-stu-id="81344-292">**Properties** pane in the **Elements** tool</span></span>  
:::image-end:::  

<span data-ttu-id="81344-293">Problema de Chromium:</span><span class="sxs-lookup"><span data-stu-id="81344-293">Chromium issue:</span></span>  <!--  [#1105205][CR1105205],  -->  <span data-ttu-id="81344-294">[#1116085] [CR1116085]</span><span class="sxs-lookup"><span data-stu-id="81344-294">[#1116085][CR1116085]</span></span>  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Human-readable `X-Client-Data` header values" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <a name="autocomplete-custom-fonts-in-the-styles-pane"></a><span data-ttu-id="81344-295">Autocompletar fuentes personalizadas en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="81344-295">Autocomplete custom fonts in the Styles pane</span></span>  

<span data-ttu-id="81344-296">Las caras de fuente importadas ahora se agregan a la lista de autocompletar CSS al editar la `font-family` propiedad en el panel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="81344-296">Imported font faces are now added to the list of CSS autocompletion when editing the `font-family` property in the **Styles** pane.</span></span>  

<span data-ttu-id="81344-297">Por ejemplo, si `monospace` es una fuente personalizada instalada en el equipo local, se muestra en la lista de finalización de CSS.</span><span class="sxs-lookup"><span data-stu-id="81344-297">For example, if `monospace` is a custom font installed on the local machine, it displays in the CSS completion list.</span></span>  <span data-ttu-id="81344-298">En versiones anteriores de Microsoft Edge, no se mostró la fuente.</span><span class="sxs-lookup"><span data-stu-id="81344-298">In previous versions of Microsoft Edge, the font was not displayed.</span></span>

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Autocompletar fuentes personalizadas" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   <span data-ttu-id="81344-300">Autocompletar fuentes personalizadas</span><span class="sxs-lookup"><span data-stu-id="81344-300">Autocomplete custom fonts</span></span>  
:::image-end:::  

<span data-ttu-id="81344-301">Problema de Chromium: [#1106221][CR1106221]</span><span class="sxs-lookup"><span data-stu-id="81344-301">Chromium issue: [#1106221][CR1106221]</span></span>  

#### <a name="consistently-display-resource-type-in-network-panel"></a><span data-ttu-id="81344-302">Mostrar de forma coherente el tipo de recurso en el panel Red</span><span class="sxs-lookup"><span data-stu-id="81344-302">Consistently display resource type in Network panel</span></span>  

<span data-ttu-id="81344-303">Ahora DevTools muestra de forma coherente el mismo tipo de recurso que la solicitud de red original y se anexa al valor de columna Tipo cuando se produce el redireccionamiento `/ Redirect` \(Código de estado HTTP 302\). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="81344-303">DevTools now consistently display the same resource type as the original network request and appends `/ Redirect` to the **Type** column value when redirection \(HTTP status code 302\) happens.</span></span>  

<span data-ttu-id="81344-304">Anteriormente, DevTools cambió el tipo a `Other` veces.</span><span class="sxs-lookup"><span data-stu-id="81344-304">Previously DevTools changed the type to `Other` sometimes.</span></span>  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Mostrar tipo de recurso de redireccionamiento" lightbox="../../media/2020/08/network-redirect.msft.png":::
   <span data-ttu-id="81344-306">Mostrar tipo de recurso de redireccionamiento</span><span class="sxs-lookup"><span data-stu-id="81344-306">Display redirect resource type</span></span>  
:::image-end:::  

<span data-ttu-id="81344-307">Problema de Chromium: [#997694][CR997694]</span><span class="sxs-lookup"><span data-stu-id="81344-307">Chromium issue: [#997694][CR997694]</span></span>  

#### <a name="clear-buttons-in-the-elements-and-network-tools"></a><span data-ttu-id="81344-308">Borrar botones en las herramientas Elementos y Red</span><span class="sxs-lookup"><span data-stu-id="81344-308">Clear buttons in the Elements and Network tools</span></span>  

<span data-ttu-id="81344-309">Los cuadros de texto siguientes ahora tienen **botones** Borrar.</span><span class="sxs-lookup"><span data-stu-id="81344-309">The following text boxes now have **Clear** buttons.</span></span>  

*   <span data-ttu-id="81344-310">Los cuadros de texto de filtro del panel **Estilos** y **la herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="81344-310">The filter text boxes in the **Styles** pane and **Network** tool.</span></span>  
*   <span data-ttu-id="81344-311">Cuadro de texto de búsqueda DOM de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="81344-311">The DOM search text box in the **Elements** tool.</span></span>  

<span data-ttu-id="81344-312">Elija el **botón** Borrar para quitar cualquier texto escrito.</span><span class="sxs-lookup"><span data-stu-id="81344-312">Choose the **Clear** button to remove any inputted text.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Borrar botones en los paneles Elementos" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         <span data-ttu-id="81344-314">Borrar botones en las **herramientas de** elementos</span><span class="sxs-lookup"><span data-stu-id="81344-314">Clear buttons in the **Elements** tools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Borrar botones en los paneles de red" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         <span data-ttu-id="81344-316">Borrar botones en las  **herramientas de** red</span><span class="sxs-lookup"><span data-stu-id="81344-316">Clear buttons in the  **Network** tools</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="81344-317">Problema de Chromium: [#1067184][CR1067184]</span><span class="sxs-lookup"><span data-stu-id="81344-317">Chromium issue: [#1067184][CR1067184]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="81344-318">Descargar los canales de vista previa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="81344-318">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="81344-319">Si estás en Windows o macOS, considera usar los canales de vista [previa de Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81344-319">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="81344-320">Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="81344-320">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="81344-321">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="81344-321">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Icono DevTools Settings"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Desuso del panel Propiedades en el panel Elementos: novedades de DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Características de depuración de cuadrícula CSS: novedades de DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalización de métodos abreviados de teclado en las herramientas de desarrollo de Microsoft Edge | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Habilitar API experimentales: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulación: admite el modo de pantalla dual: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Habilitar visor de pedidos de origen: características experimentales | Microsoft Docs"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Emulación: admite el modo de pantalla dual: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Pruebas en dispositivos plegables y de pantalla doble: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft Docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tabla: referencia de api de consola | Microsoft Docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Busque código JavaScript y CSS sin usar con la pestaña Cobertura en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Drawer: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analizar el rendimiento de representación con la pestaña Representación: referencia de análisis de rendimiento | Microsoft Docs"  
[DevtoolsMediaPanelIndex]: /microsoft-edge/devtools-guide-chromium/media-panel/index "Ver y depurar información de reproductores multimedia | Microsoft Docs"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la costura: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Característica de pantalla de medios CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio código "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio métodos abreviados de teclado de código para Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "El nuevo Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar los métodos abreviados de teclado o los enlaces de teclas | Errores de Chromium"
[CR384968]: https://crbug.com/384968 "Opción para omitir fuentes local() | Errores de Chromium"  
[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la versión más reciente de | Errores de Chromium"  
[CR807440]: https://crbug.com/807440 "Chrome se bloquea con un gran número de SWs | Errores de Chromium"  
[CR997694]: https://crbug.com/997694 "Las solicitudes XHR con estado 302 no se muestran en el filtro \"xhr\" del panel de red | Errores de Chromium"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS Grid/Flexbox/Table | Errores de Chromium"  
[CR1051466]: https://crbug.com/1051466 "Admite la depuración de COOP/COEP en DevTools | Errores de Chromium"  
[CR1054281]: https://crbug.com/1054281 "Solicitud de característica: DevTools debe emular dispositivos de pantalla doble y | Errores de Chromium"  
[CR1067184]: https://crbug.com/1067184 "Solicitud de característica: botón Borrar filtro en elementos de & -> de filtro de estilos | Errores de Chromium"  
[CR1068116]: https://crbug.com/1068116 "☂ Panel de problemas de envío | Errores de Chromium"  
[CR1080569]: https://crbug.com/1080569 "acorn no admite operadores de asignación lógica | Errores de Chromium"  
[CR1080589]: https://crbug.com/1080589 "Clasificar problemas por terceros o por terceros | Errores de Chromium"  
[CR1086817]: https://crbug.com/1086817 "acorn no admite separadores numéricos | Errores de Chromium"  
[CR1090802]: https://crbug.com/1090802 "Simular cambios de estado de inactividad desde la API de detección de inactividad | Errores de Chromium"  
[CR1093227]: https://crbug.com/1093227 "DevTools: sugerir colores accesibles más cercanos | Errores de Chromium"  
[CR1093247]: https://crbug.com/1093247 "Mostrar información sobre fotogramas en el panel de aplicaciones | Errores de Chromium"  
[CR1094406]: https://crbug.com/1094406 "Los desarrolladores desean un visor de pedidos de origen para AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: admite la emulación de la característica multimedia prefers-reduced-data | Errores de Chromium"  
[CR1096481]: https://crbug.com/1096481 "Problemas de colocación de banner | Errores de Chromium"  
[CR1100253]: https://crbug.com/1100253 "Agregar acceso directo de nodo de captura de pantalla en el menú contextual elemento | Errores de Chromium"  
[CR1103316]: https://crbug.com/1103316 "La búsqueda de elementos no resuelveNode (texto resaltado, etc.) en la primera búsqueda de resultados | Errores de Chromium"  
[CR1103854]: https://crbug.com/1103854 "Desuso de los valores X-Client-Data en Developer Tools | Errores de Chromium"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: "Agregar fuentes importadas a la autocompleción de familia de fuentes en el panel Estilos | https://crbug.com/1106221 Errores de Chromium"  
[CR1107766]: "Mostrar información sobre fotogramas generados por https://crbug.com/1107766 'window.open()' en el árbol de | Errores de Chromium"  
[CR1115011]: "Al copiar una tabla desde la consola, la estructura de la tabla no se https://crbug.com/1115011 conserva | Errores de Chromium"  
[CR1116085]: "Vuelva a traer el inspector de propiedades https://crbug.com/1116085 de DevTools | Errores de Chromium"  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "prefers-reduced-data: Media Queries Level 5 | Borradores del editor de grupo de trabajo CSS de W3C"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v6.2.0: GoogleChrome/lighthouse | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Búferes de protocolo | Desarrolladores de Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Asignación lógica | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Separadores numéricos | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Hacer que el sitio web \"cross-origin se aísla\" con COOP y COEP | web.dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Detectar usuarios inactivos con la API de detección inactiva | web.dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Evite las animaciones no compuestas | web.dev"  

> [!NOTE]
> <span data-ttu-id="81344-382">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="81344-382">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="81344-383">La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/08/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="81344-383">The original page is found [here](https://developers.google.com/web/updates/2020/08/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="81344-385">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="81344-385">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

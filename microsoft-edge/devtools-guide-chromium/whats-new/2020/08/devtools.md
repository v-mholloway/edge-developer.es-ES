---
description: Hacer coincidir los métodos abreviados de teclado con el código de Visual Studio, emular Surface Duo y el plegado de Samsung Galaxy, mejoras de la cuadrícula CSS y mucho más.
title: Novedades de DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 74fb4e276547d9f653a5bcbdcab9c4406d09a81a
ms.sourcegitcommit: 912609aa49864e3363aaa3b245ff2aa4bec3fc3e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104864"
---
# <span data-ttu-id="b0da3-104">Novedades de DevTools (Microsoft Edge 86)</span><span class="sxs-lookup"><span data-stu-id="b0da3-104">What's New In DevTools (Microsoft Edge 86)</span></span>  

## <span data-ttu-id="b0da3-105">Anuncios del equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b0da3-105">Announcements from the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <span data-ttu-id="b0da3-106">Hacer coincidir los métodos abreviados de teclado en DevTools a Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b0da3-106">Match keyboard shortcuts in DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="b0da3-107">En Microsoft Edge 86, puedes hacer coincidir los métodos abreviados de teclado del DevTools con tus accesos directos en [Visual Studio Code][VisualStudioCode].</span><span class="sxs-lookup"><span data-stu-id="b0da3-107">In Microsoft Edge 86, you may match keyboard shortcuts in the DevTools to your shortcuts in [Visual Studio Code][VisualStudioCode].</span></span> 

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   <span data-ttu-id="b0da3-109">Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b0da3-109">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-110">Para activar esta característica, vaya a [personalizar los métodos abreviados de teclado en el DevTools de Microsoft Edge][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="b0da3-110">To activate this feature, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  

<span data-ttu-id="b0da3-111">Por ejemplo, el método abreviado de teclado para pausar o seguir ejecutando un script en [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] es `F5` .</span><span class="sxs-lookup"><span data-stu-id="b0da3-111">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="b0da3-112">Con el valor preestablecido **DevTools (predeterminado)** , ese mismo método abreviado de DevTools es `F8` , pero cuando eliges el ajuste preestablecido de **Visual Studio** , ahora también está el método abreviado `F5` .</span><span class="sxs-lookup"><span data-stu-id="b0da3-112">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8`, but when you choose the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="b0da3-113">[#174309][CR174309] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b0da3-113">Chromium issue [#174309][CR174309]</span></span>  

### <span data-ttu-id="b0da3-114">Emula Surface Duo y Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="b0da3-114">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio":::
   <span data-ttu-id="b0da3-116">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="b0da3-116">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-117">Ahora puede probar el aspecto de su sitio web o aplicación en dos nuevos dispositivos:  [Surface Duo][MicrosoftSurfaceDevicesDuo] y [Samsung Galaxy Foldr][SamsungMobileGalaxyFold] en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b0da3-117">You are now able to test the look and feel of your website or app on two new devices:  [Surface Duo][MicrosoftSurfaceDevicesDuo] and [Samsung Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.</span></span>  

<span data-ttu-id="b0da3-118">Para ayudar a mejorar el sitio web o la aplicación para los dispositivos de plegable y pantalla doble, usa las siguientes características al [emular el dispositivo][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="b0da3-118">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="b0da3-119">[Expansión][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], que es cuando su sitio web \ (o aplicación \) aparece en las dos pantallas.</span><span class="sxs-lookup"><span data-stu-id="b0da3-119">[Spanning][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>
*   <span data-ttu-id="b0da3-120">[Representando la costura][DualScreenIntroductionHowWorkSeam], que es el espacio entre las dos pantallas.</span><span class="sxs-lookup"><span data-stu-id="b0da3-120">[Rendering the seam][DualScreenIntroductionHowWorkSeam], which is the space between the two screens.</span></span>
*   <span data-ttu-id="b0da3-121">[Habilitar las API experimentales de la plataforma web][DevtoolsExperimentalFeaturesEnableExperimentalApis] para acceder a la nueva [característica de expansión de pantalla multimedia de CSS][DualScreenWebCssMediaSpanning] y [API de getWindowSegments de JavaScript][DualScreenWebJavascriptGetwindowsegments].</span><span class="sxs-lookup"><span data-stu-id="b0da3-121">[Enabling experimental Web Platform APIs][DevtoolsExperimentalFeaturesEnableExperimentalApis] to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [JavaScript getWindowSegments API][DualScreenWebJavascriptGetwindowsegments].</span></span>  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   <span data-ttu-id="b0da3-123">Emulación de dispositivos para Surface Duo</span><span class="sxs-lookup"><span data-stu-id="b0da3-123">Device emulation for Surface Duo</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-124">Para activar esta característica experimental, navegue para [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla situada junto a **emulación: modo de pantalla doble de soporte**.</span><span class="sxs-lookup"><span data-stu-id="b0da3-124">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Emulation: Support dual screen mode**.</span></span>  

<span data-ttu-id="b0da3-125">Para obtener más información sobre este experimento, vaya a [emulación: compatibilidad con el modo de pantalla doble][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span><span class="sxs-lookup"><span data-stu-id="b0da3-125">For more information about this experiment, navigate to [Emulation: Support dual screen mode][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span></span>  

<span data-ttu-id="b0da3-126">Problema de cromo: [#1054281][CR1054281]</span><span class="sxs-lookup"><span data-stu-id="b0da3-126">Chromium issue: [#1054281][CR1054281]</span></span>  

### <span data-ttu-id="b0da3-127">Mejoras de superposición de cuadrícula CSS y nuevas características de cuadrícula experimental</span><span class="sxs-lookup"><span data-stu-id="b0da3-127">CSS grid overlay improvements and new experimental grid features</span></span>  

<span data-ttu-id="b0da3-128">Agradecemos tus comentarios positivos sobre las superposiciones de cuadrícula CSS mejoradas.</span><span class="sxs-lookup"><span data-stu-id="b0da3-128">Thank you for the positive feedback about the improved CSS grid overlays.</span></span>  <span data-ttu-id="b0da3-129">Las superposiciones de cuadrícula CSS ahora están habilitadas de forma predeterminada y no requieren que se active un experimento.</span><span class="sxs-lookup"><span data-stu-id="b0da3-129">The CSS grid overlays are now enabled by default and do not require you to turn on an experiment.</span></span>  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   <span data-ttu-id="b0da3-131">Superposición de cuadrícula CSS para `article` elemento</span><span class="sxs-lookup"><span data-stu-id="b0da3-131">CSS grid overlay for `article` element</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="b0da3-132">Para obtener más información sobre las superposiciones de cuadrícula, vaya a [características de depuración de cuadrícula de CSS][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span><span class="sxs-lookup"><span data-stu-id="b0da3-132">For more information about grid overlays, go to [CSS grid debugging features][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="b0da3-133">El equipo de Microsoft Edge DevTools y el equipo de DevTools de Chrome colaboran en características adicionales.</span><span class="sxs-lookup"><span data-stu-id="b0da3-133">The Microsoft Edge DevTools team and the Chrome DevTools team collaborate on additional features.</span></span>  <span data-ttu-id="b0da3-134">Las nuevas características incluyen varias superposiciones que son persistentes y se pueden configurar desde un nuevo panel de **diseño** en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="b0da3-134">The new features include multiple overlays that are persistent and configurable from a new **Layout** pane on the **Elements** panel.</span></span>  

<span data-ttu-id="b0da3-135">Para activar esta característica experimental, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla situada junto a **Habilitar nuevas características de depuración de cuadrícula CSS (opciones de configuración disponibles en el panel de la barra lateral de diseño en elementos después de reiniciar)**.</span><span class="sxs-lookup"><span data-stu-id="b0da3-135">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)**.</span></span>  

<span data-ttu-id="b0da3-136">Para obtener más información sobre este experimento, navegue para [Habilitar nuevas características de depuración de cuadrícula CSS][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span><span class="sxs-lookup"><span data-stu-id="b0da3-136">For more information about this experiment, navigate to [Enable new CSS grid debugging features][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="b0da3-137">Problema de cromo: [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="b0da3-137">Chromium issue: [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="b0da3-138">La tabla copiada de la consola conserva el formato</span><span class="sxs-lookup"><span data-stu-id="b0da3-138">Table copied from the Console preserves formatting</span></span>  

<span data-ttu-id="b0da3-139">En Microsoft Edge 85 o versiones anteriores, se perdió el formato de una copiada `console.table` .</span><span class="sxs-lookup"><span data-stu-id="b0da3-139">In Microsoft Edge 85 or earlier, the formatting of a copied `console.table` was lost.</span></span>  <span data-ttu-id="b0da3-140">Si ha copiado el resultado de la API de consola de [tabla][DevtoolsConsoleApiTable] y lo ha pegado, solo se conservará el texto de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b0da3-140">If you copied the output from the [table][DevtoolsConsoleApiTable] Console API, and pasted it, only the text of the table was kept.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` <span data-ttu-id="b0da3-142">Salida de la API de consola en Microsoft Edge 85 o versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="b0da3-142">Console API output in Microsoft Edge 85 or earlier</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="b0da3-144">Salida de la API de consola de Microsoft Edge 85 o versiones anteriores pegadas en código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b0da3-144">Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="b0da3-145">En Microsoft Edge 86 o posterior, al copiar una tabla desde la **consola**, se conserva el formato.</span><span class="sxs-lookup"><span data-stu-id="b0da3-145">In Microsoft Edge 86 or later, when you copy a table from the **Console**, the formatting is now preserved.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` <span data-ttu-id="b0da3-147">Salida de la API de consola en Microsoft Edge 86 o posterior</span><span class="sxs-lookup"><span data-stu-id="b0da3-147">Console API output in Microsoft Edge 86 or later</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="b0da3-149">Salida de la API de consola de Microsoft Edge 86 o posterior pegada en el código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b0da3-149">Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="b0da3-150">Error de cromo: [#1115011] [CR1115011]</span><span class="sxs-lookup"><span data-stu-id="b0da3-150">Chromium issue: [#1115011][CR1115011]</span></span>  

### <span data-ttu-id="b0da3-151">Visor de pedidos de origen para realizar pruebas de accesibilidad más sencillas</span><span class="sxs-lookup"><span data-stu-id="b0da3-151">Source Order Viewer for easier accessibility testing</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio":::
   <span data-ttu-id="b0da3-153">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="b0da3-153">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-154">La nueva aplicación auxiliar de accesibilidad muestra el orden de los elementos en el origen.</span><span class="sxs-lookup"><span data-stu-id="b0da3-154">The new accessibility helper displays the order of elements in the source.</span></span>  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   <span data-ttu-id="b0da3-156">Activar **Mostrar orden de origen**</span><span class="sxs-lookup"><span data-stu-id="b0da3-156">Activate **Show source order**</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-157">Esta característica hace que sea más fácil comprobar la forma en que los usuarios del teclado y el lector de pantalla experimentan su sitio web o aplicación.</span><span class="sxs-lookup"><span data-stu-id="b0da3-157">This feature makes it easier to test the way screen reader and keyboard users experience your website or app.</span></span>  <span data-ttu-id="b0da3-158">Los lectores de pantalla y la navegación mediante teclado dependen del contenido que se coloca en un orden determinado en el código fuente de su sitio web o aplicación, de modo que coincida con la página representada.</span><span class="sxs-lookup"><span data-stu-id="b0da3-158">Screen readers and keyboard navigation depend on content being placed in a particular order in the source code of your website or app, so that it matches the rendered page.</span></span>  <span data-ttu-id="b0da3-159">El visor del pedido de origen muestra posibles diferencias en el orden entre la página representada y el código fuente.</span><span class="sxs-lookup"><span data-stu-id="b0da3-159">The Source Order Viewer displays potential differences in order between the rendered page and the source code.</span></span>  

<span data-ttu-id="b0da3-160">Para activar esta característica experimental, navegue para [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla que se encuentra junto a **Habilitar el visor de orden de origen**.</span><span class="sxs-lookup"><span data-stu-id="b0da3-160">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Source Order Viewer**.</span></span>  

<span data-ttu-id="b0da3-161">Para obtener más información sobre este experimento, vaya a [Habilitar el visor de orden de origen][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span><span class="sxs-lookup"><span data-stu-id="b0da3-161">For more information about this experiment, navigate to [Enable Source Order Viewer][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span></span>  

<span data-ttu-id="b0da3-162">Problema de cromo: [#1094406][CR1094406]</span><span class="sxs-lookup"><span data-stu-id="b0da3-162">Chromium issue: [#1094406][CR1094406]</span></span>  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <span data-ttu-id="b0da3-163">Resaltar todos los resultados de búsqueda en la herramienta elementos</span><span class="sxs-lookup"><span data-stu-id="b0da3-163">Highlight all search results in Elements tool</span></span>  

<span data-ttu-id="b0da3-164">En Microsoft Edge 84 y 85, el primer resultado de búsqueda en el panel **elementos** no resaltado.</span><span class="sxs-lookup"><span data-stu-id="b0da3-164">In Microsoft Edge 84 and 85, the first search result in the **Elements** panel did not highlight.</span></span>  <span data-ttu-id="b0da3-165">El resto de los resultados de la búsqueda estaban resaltados correctamente.</span><span class="sxs-lookup"><span data-stu-id="b0da3-165">The remaining search results were highlighted correctly.</span></span>  

<span data-ttu-id="b0da3-166">Gracias por enviar tus comentarios y de mejorar el cromo.</span><span class="sxs-lookup"><span data-stu-id="b0da3-166">Thank you for sending your feedback and helping improve Chromium.</span></span>  <span data-ttu-id="b0da3-167">Su comentario no cubierto [#1103316][CR1103316] problema en el proyecto de cromo de código abierto.</span><span class="sxs-lookup"><span data-stu-id="b0da3-167">Your feedback uncovered Issue [#1103316][CR1103316] in the open-source Chromium project.</span></span>  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   <span data-ttu-id="b0da3-169">Primer resultado de búsqueda resaltado en el panel **elementos** en Microsoft Edge 84 o posterior</span><span class="sxs-lookup"><span data-stu-id="b0da3-169">Highlighted first search result on **Elements** panel in Microsoft Edge 84 or later</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-170">Ahora el problema se ha corregido en todas las versiones de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b0da3-170">The issue is now fixed in all versions of Microsoft Edge.</span></span>  

<span data-ttu-id="b0da3-171">Problema de cromo: [#1103316][CR1103316]</span><span class="sxs-lookup"><span data-stu-id="b0da3-171">Chromium issue: [#1103316][CR1103316]</span></span>  

## <span data-ttu-id="b0da3-172">Anuncios del proyecto de cromo</span><span class="sxs-lookup"><span data-stu-id="b0da3-172">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="b0da3-173">Nuevo panel multimedia</span><span class="sxs-lookup"><span data-stu-id="b0da3-173">New Media panel</span></span>  

<span data-ttu-id="b0da3-174">DevTools ahora muestra la información de los reproductores multimedia en el panel [multimedia][DevtoolsMediaPanelIndex] .</span><span class="sxs-lookup"><span data-stu-id="b0da3-174">DevTools now displays media players information in the [Media][DevtoolsMediaPanelIndex] panel.</span></span>  

<span data-ttu-id="b0da3-175">Para abrir el nuevo panel **multimedia** , complete el paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="b0da3-175">To open the new **Media** panel, complete the following step.</span></span>  

1.  <span data-ttu-id="b0da3-176">Elija **personalizar y controlar DevTools** \ ( `...` \) > **más**  >  **medios**de herramientas.</span><span class="sxs-lookup"><span data-stu-id="b0da3-176">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/media-panel.msft.png":::
       <span data-ttu-id="b0da3-178">Nuevo panel **multimedia**</span><span class="sxs-lookup"><span data-stu-id="b0da3-178">New **Media** panel</span></span>  
    :::image-end:::  

<span data-ttu-id="b0da3-179">Antes del nuevo panel **multimedia** de DevTools, la información de registro y depuración de los reproductores de vídeo se encontró en la configuración de **reproductores recientes** .</span><span class="sxs-lookup"><span data-stu-id="b0da3-179">Before the new **Media** panel in DevTools, the logging and debug information about video players was located under the **Recent Players** setting.</span></span>  <span data-ttu-id="b0da3-180">Para abrir la configuración de **reproductores recientes** , vaya a `edge://media-internals` la ficha **reproductores** y elija.</span><span class="sxs-lookup"><span data-stu-id="b0da3-180">To open the **Recent Players** setting, go to `edge://media-internals` and choose the **Players** tab.</span></span>  

<span data-ttu-id="b0da3-181">Ver contenido en vivo e inspeccionar problemas potenciales más rápidamente, incluidos los siguientes ejemplos.</span><span class="sxs-lookup"><span data-stu-id="b0da3-181">View live content and inspect potential issues more quickly, including the following examples.</span></span>  

*   <span data-ttu-id="b0da3-182">¿Por qué se eliminan los marcos?</span><span class="sxs-lookup"><span data-stu-id="b0da3-182">Why frames are dropped?</span></span>  
*   <span data-ttu-id="b0da3-183">¿Por qué JavaScript interactúa con el reproductor de forma inesperada?</span><span class="sxs-lookup"><span data-stu-id="b0da3-183">Why JavaScript is interacting with the player in an unexpected way?</span></span>  

### <span data-ttu-id="b0da3-184">Captura de capturas de nodo con el menú contextual del panel de elementos</span><span class="sxs-lookup"><span data-stu-id="b0da3-184">Capture node screenshots using the Elements panel context menu</span></span>  

<span data-ttu-id="b0da3-185">Ahora puede capturar capturas de pantalla de nodo usando el menú contextual en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="b0da3-185">You may now capture node screenshots using the context menu in the **Elements** panel.</span></span>  

<span data-ttu-id="b0da3-186">Por ejemplo, para tomar una captura de pantalla de la tabla de contenido, mantenga el puntero sobre el elemento, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **capturar nodo captura de pantalla**.</span><span class="sxs-lookup"><span data-stu-id="b0da3-186">For example, to take a screenshot of the table of contents, hover on the element, open the contextual menu \(right-click\), and select **Capture node screenshot**.</span></span>  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   <span data-ttu-id="b0da3-188">Capturar capturas de nodo</span><span class="sxs-lookup"><span data-stu-id="b0da3-188">Capture node screenshots</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-189">Problema de cromo: [#1100253][CR1100253]</span><span class="sxs-lookup"><span data-stu-id="b0da3-189">Chromium issue: [#1100253][CR1100253]</span></span>  

### <span data-ttu-id="b0da3-190">Actualizaciones de la herramienta problemas</span><span class="sxs-lookup"><span data-stu-id="b0da3-190">Issues tool updates</span></span>  

<span data-ttu-id="b0da3-191">La barra de advertencias de problemas del panel de la **consola** se reemplaza por un mensaje normal.</span><span class="sxs-lookup"><span data-stu-id="b0da3-191">The Issues warning bar on the **Console** panel is now replaced with a regular message.</span></span>  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   <span data-ttu-id="b0da3-193">Problemas en el mensaje de consola</span><span class="sxs-lookup"><span data-stu-id="b0da3-193">Issues in console message</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-194">Los problemas de cookies de terceros ahora están ocultos de forma predeterminada en la herramienta **problemas** .</span><span class="sxs-lookup"><span data-stu-id="b0da3-194">Third-party cookie issues are now hidden by default in the **Issues** tool.</span></span>  <span data-ttu-id="b0da3-195">Active la casilla **incluir problemas de cookie de terceros** para ver los problemas.</span><span class="sxs-lookup"><span data-stu-id="b0da3-195">Enable the new **Include third-party cookie issues** checkbox to view the issues.</span></span>  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   <span data-ttu-id="b0da3-197">casilla de verificación de problemas de cookies de terceros</span><span class="sxs-lookup"><span data-stu-id="b0da3-197">third-party cookie issues checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-198">Problemas de cromo: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span><span class="sxs-lookup"><span data-stu-id="b0da3-198">Chromium issues: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span></span>  

### <span data-ttu-id="b0da3-199">Emular las fuentes locales que faltan</span><span class="sxs-lookup"><span data-stu-id="b0da3-199">Emulate missing local fonts</span></span>  

<span data-ttu-id="b0da3-200">Abra la [herramienta de representación][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] y use la nueva característica **deshabilitar fuentes locales** para emular los orígenes que faltan `local()` en `@font-face` las reglas.</span><span class="sxs-lookup"><span data-stu-id="b0da3-200">Open the [Rendering tool][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] and use the new **Disable local fonts** feature to emulate missing `local()` sources in `@font-face` rules.</span></span>  

<span data-ttu-id="b0da3-201">Por ejemplo, cuando la `Rubik` fuente está instalada en el dispositivo y la `@font-face src` regla la usa como `local()` fuente, Microsoft Edge usa el archivo de fuente local del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0da3-201">For example, when the `Rubik` font is installed on your device and the `@font-face src` rule uses it as a `local()` font, Microsoft Edge uses the local font file from your device.</span></span>  

<span data-ttu-id="b0da3-202">Cuando **deshabilitar fuentes locales** está habilitado, DevTools ignora las `local()` fuentes y las recupera desde la red.</span><span class="sxs-lookup"><span data-stu-id="b0da3-202">When **Disable local fonts** is enabled, DevTools ignores the `local()` fonts and fetches each from the network.</span></span>  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/disable-font.msft.png":::
   <span data-ttu-id="b0da3-204">Emular las fuentes locales que faltan</span><span class="sxs-lookup"><span data-stu-id="b0da3-204">Emulate missing local fonts</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-205">Si usa dos copias diferentes de la misma fuente durante el desarrollo, como los siguientes ejemplos.</span><span class="sxs-lookup"><span data-stu-id="b0da3-205">If you use two different copies of the same font during development, such as the following examples.</span></span>  

*   <span data-ttu-id="b0da3-206">Una fuente local para las herramientas de diseño.</span><span class="sxs-lookup"><span data-stu-id="b0da3-206">A local font for your design tools.</span></span>  
*   <span data-ttu-id="b0da3-207">Una fuente web para tu código.</span><span class="sxs-lookup"><span data-stu-id="b0da3-207">A web font for your code.</span></span>  

<span data-ttu-id="b0da3-208">Use **deshabilitar fuentes locales** para que le resulte más fácil completar las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="b0da3-208">Use **Disable local fonts** to make it easier for you to complete the following tasks.</span></span>  

*   <span data-ttu-id="b0da3-209">Depure y mida el rendimiento de carga y la optimización de fuentes web.</span><span class="sxs-lookup"><span data-stu-id="b0da3-209">Debug and measure loading performance and optimization of web fonts.</span></span>  
*   <span data-ttu-id="b0da3-210">Verifica la precisión de las `@font-face` reglas de CSS.</span><span class="sxs-lookup"><span data-stu-id="b0da3-210">Verify accuracy of your CSS `@font-face` rules.</span></span>  
*   <span data-ttu-id="b0da3-211">Descubra las diferencias entre las versiones locales instaladas en el dispositivo y una fuente web.</span><span class="sxs-lookup"><span data-stu-id="b0da3-211">Discover differences between local versions installed on your device and a web font.</span></span>  

<span data-ttu-id="b0da3-212">Problema de cromo: [#384968][CR384968]</span><span class="sxs-lookup"><span data-stu-id="b0da3-212">Chromium issue: [#384968][CR384968]</span></span>  

### <span data-ttu-id="b0da3-213">Emular usuarios inactivos</span><span class="sxs-lookup"><span data-stu-id="b0da3-213">Emulate inactive users</span></span>  

<span data-ttu-id="b0da3-214">La [API de detección de inactividad][WebDevIdleDetection] permite a los programadores detectar usuarios inactivos y reaccionar según los cambios de estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="b0da3-214">The [Idle Detection API][WebDevIdleDetection] allows developers to detect inactive users and react on idle state changes.</span></span>  <span data-ttu-id="b0da3-215">Ahora puede usar DevTools para emular los cambios de estado de inactividad en la herramienta **sensores** para el estado del usuario y el estado de la pantalla en lugar de esperar a que cambie el estado real de inactividad.</span><span class="sxs-lookup"><span data-stu-id="b0da3-215">You are now able to use DevTools to emulate idle state changes in the **Sensors** tool for both the user state and the screen state instead of waiting for the actual idle state to change.</span></span>  <span data-ttu-id="b0da3-216">Puede abrir la herramienta de **sensores** desde el [cajón][DevtoolsCustomizeIndexDrawer].</span><span class="sxs-lookup"><span data-stu-id="b0da3-216">You may open the **Sensors** tool from the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   <span data-ttu-id="b0da3-218">Emular usuarios inactivos</span><span class="sxs-lookup"><span data-stu-id="b0da3-218">Emulate inactive users</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-219">Problema de cromo: [#1090802][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="b0da3-219">Chromium issue: [#1090802][CR1090802]</span></span>  

### <span data-ttu-id="b0da3-220">Emular preferidos: datos reducidos</span><span class="sxs-lookup"><span data-stu-id="b0da3-220">Emulate prefers-reduced-data</span></span>  

> [!NOTE]
> <span data-ttu-id="b0da3-221">En Microsoft Edge 86, para habilitar esta característica, vaya a `edge://flags#enable-experimental-web-platform-features` la bandera **experimental características de plataforma web** y enciéndala.</span><span class="sxs-lookup"><span data-stu-id="b0da3-221">In Microsoft Edge 86, to enable this feature, go to `edge://flags#enable-experimental-web-platform-features` and turn on the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="b0da3-222">La opción de emulación solo se muestra si la marca está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b0da3-222">The emulation option is only displayed if the flag is enabled.</span></span>  

<span data-ttu-id="b0da3-223">La consulta de medios de [datos preferidos-datos][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] detecta las preferencias de contenido de usuario para reducir los datos.</span><span class="sxs-lookup"><span data-stu-id="b0da3-223">The [prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] media query detects user content preferences for reduced data.</span></span>  <span data-ttu-id="b0da3-224">Si se selecciona, el usuario recibe contenido de página alternativo que usa menos datos.</span><span class="sxs-lookup"><span data-stu-id="b0da3-224">If selected, the user receives alternate page content that uses less data.</span></span>  

<span data-ttu-id="b0da3-225">Ahora puede usar DevTools para emular la `prefers-reduced-data` consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="b0da3-225">You may now use DevTools to emulate the `prefers-reduced-data` media query.</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   <span data-ttu-id="b0da3-227">Emular preferidos: datos reducidos</span><span class="sxs-lookup"><span data-stu-id="b0da3-227">Emulate prefers-reduced-data</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-228">Problema de cromo: [#1096068][CR1096068]</span><span class="sxs-lookup"><span data-stu-id="b0da3-228">Chromium issue: [#1096068][CR1096068]</span></span>  

### <span data-ttu-id="b0da3-229">Compatibilidad con las nuevas características de JavaScript</span><span class="sxs-lookup"><span data-stu-id="b0da3-229">Support for new JavaScript features</span></span>  

<span data-ttu-id="b0da3-230">DevTools ahora admite las siguientes características del lenguaje JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b0da3-230">DevTools now have better supported the following JavaScript language features.</span></span>  

| <span data-ttu-id="b0da3-231">Característica del lenguaje JavaScript</span><span class="sxs-lookup"><span data-stu-id="b0da3-231">JavaScript language feature</span></span> | <span data-ttu-id="b0da3-232">Detalles</span><span class="sxs-lookup"><span data-stu-id="b0da3-232">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="b0da3-233">Operadores de asignación lógica</span><span class="sxs-lookup"><span data-stu-id="b0da3-233">Logical assignment operators</span></span>][V8FeaturesLogicalAssignment] | <span data-ttu-id="b0da3-234">DevTools ahora admite la asignación lógica con los `&&=` operadores New, `||=` y `??=` en los paneles **Console (consola** ) y **Sources (orígenes** ).</span><span class="sxs-lookup"><span data-stu-id="b0da3-234">DevTools now supports logical assignment with the new `&&=`, `||=`, and `??=` operators in the **Console** and **Sources** panels.</span></span>  |  
| <span data-ttu-id="b0da3-235">[Separadores numéricos][V8FeaturesNumericSeparators] muy imprimibles</span><span class="sxs-lookup"><span data-stu-id="b0da3-235">Pretty-print [numeric separators][V8FeaturesNumericSeparators]</span></span> | <span data-ttu-id="b0da3-236">DevTools ahora correctamente: imprime los separadores numéricos en el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="b0da3-236">DevTools now properly pretty-prints the numeric separators in the **Sources** panel.</span></span>  |  

<span data-ttu-id="b0da3-237">Problemas de cromo: [1086817][CR1086817], [1080569][CR1080569]</span><span class="sxs-lookup"><span data-stu-id="b0da3-237">Chromium issues: [1086817][CR1086817], [1080569][CR1080569]</span></span>  

### <span data-ttu-id="b0da3-238">Lighthouse 6,2 en el panel de Lighthouse</span><span class="sxs-lookup"><span data-stu-id="b0da3-238">Lighthouse 6.2 in the Lighthouse panel</span></span>  

<span data-ttu-id="b0da3-239">El panel de **Lighthouse** ahora se ejecuta Lighthouse 6,2.</span><span class="sxs-lookup"><span data-stu-id="b0da3-239">The **Lighthouse** panel is now running Lighthouse 6.2.</span></span>  <span data-ttu-id="b0da3-240">Para obtener una lista completa de los cambios, vaya a las notas de la [versión de Lighthouse][GithubGooglechromeLighthouseV620].</span><span class="sxs-lookup"><span data-stu-id="b0da3-240">For a full list of changes, go to the [Lighthouse release notes][GithubGooglechromeLighthouseV620].</span></span>  

<span data-ttu-id="b0da3-241">Problema de cromo: [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="b0da3-241">Chromium issue: [#772558][CR772558]</span></span>  

### <span data-ttu-id="b0da3-242">Desuso de otras listas de orígenes en el panel de trabajo de servicios</span><span class="sxs-lookup"><span data-stu-id="b0da3-242">Deprecation of other origins listing in the Service Workers pane</span></span>  

<span data-ttu-id="b0da3-243">DevTools ahora proporciona un vínculo desde el panel de **trabajo de servicios** \ (panel de**aplicaciones** > panel de **trabajo de servicios** \) para ver la lista completa de trabajadores de servicios de otros orígenes.</span><span class="sxs-lookup"><span data-stu-id="b0da3-243">DevTools now provides a link from the **Service workers** pane \(**Application** panel > **Service workers** pane\) to view the full list of service workers from other origins.</span></span>  <span data-ttu-id="b0da3-244">Para acceder a la lista sin abrir la DevTools, vaya a `edge://service-worker-internals/?devtools` .</span><span class="sxs-lookup"><span data-stu-id="b0da3-244">To access the list without opening the DevTools, go to `edge://service-worker-internals/?devtools`.</span></span>  

<span data-ttu-id="b0da3-245">Anteriormente, DevTools mostrado una lista anidada en el panel de **aplicaciones** > panel de **trabajo de servicios** .</span><span class="sxs-lookup"><span data-stu-id="b0da3-245">Previously DevTools displayed a list nested under the **Application** panel > **Service workers** pane.</span></span>  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   <span data-ttu-id="b0da3-247">Vincular a otros orígenes</span><span class="sxs-lookup"><span data-stu-id="b0da3-247">Link to other origins</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-248">Problema de cromo: [#807440][CR807440]</span><span class="sxs-lookup"><span data-stu-id="b0da3-248">Chromium issue: [#807440][CR807440]</span></span>  

### <span data-ttu-id="b0da3-249">Mostrar Resumen de cobertura para elementos filtrados</span><span class="sxs-lookup"><span data-stu-id="b0da3-249">Show coverage summary for filtered items</span></span>  

<span data-ttu-id="b0da3-250">DevTools ahora recalcular y mostrar un resumen de la información de cobertura de forma dinámica.</span><span class="sxs-lookup"><span data-stu-id="b0da3-250">DevTools now recalculate and display a summary of coverage information dynamically.</span></span>  <span data-ttu-id="b0da3-251">La pantalla dinámica se desencadena cuando se aplican filtros en la herramienta de [cobertura][DevtoolsCoverageIndex] .</span><span class="sxs-lookup"><span data-stu-id="b0da3-251">The dynamic display is triggered when filters are applied in the [Coverage][DevtoolsCoverageIndex] tool.</span></span>  <span data-ttu-id="b0da3-252">Antes de que la herramienta de **cobertura** siempre muestre un resumen de toda la información de cobertura.</span><span class="sxs-lookup"><span data-stu-id="b0da3-252">Before the **Coverage** tool always displayed a summary of all coverage information.</span></span>  

<span data-ttu-id="b0da3-253">En la primera de las siguientes figuras, el resumen se muestra inicialmente `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` y en el segundo de las siguientes figuras, el Resumen `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` se muestra después de aplicar el filtrado CSS.</span><span class="sxs-lookup"><span data-stu-id="b0da3-253">In the first of the following figures, the summary initially displays `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` and in the second of the following figures, the summary displays `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` after CSS filtering is applied.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         <span data-ttu-id="b0da3-255">Resumen de la cobertura</span><span class="sxs-lookup"><span data-stu-id="b0da3-255">Coverage summary</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         <span data-ttu-id="b0da3-257">Resumen de la cobertura de los elementos filtrados</span><span class="sxs-lookup"><span data-stu-id="b0da3-257">Coverage summary for filtered items</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="b0da3-258">Problema de cromo: [#1061385][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="b0da3-258">Chromium issue: [#1061385][CR1090802]</span></span>  

### <span data-ttu-id="b0da3-259">Vista de detalles del nuevo marco en el panel de aplicación</span><span class="sxs-lookup"><span data-stu-id="b0da3-259">New frame details view in Application panel</span></span>  

<span data-ttu-id="b0da3-260">DevTools ahora mostrar una vista detallada de cada marco.</span><span class="sxs-lookup"><span data-stu-id="b0da3-260">DevTools now show a detailed view for each frame.</span></span>  <span data-ttu-id="b0da3-261">Para acceder a ella, elija un marco en el menú **Marcos** en el panel **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="b0da3-261">To access it, choose a frame under the **Frames** menu in the **Application** panel.</span></span>  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/frame-details.msft.png":::
   <span data-ttu-id="b0da3-263">Nueva vista detallada de un marco en el panel de **aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="b0da3-263">New detailed view for a frame in **Application** panel</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-264">Problema de cromo: [#1093247][CR1093247]</span><span class="sxs-lookup"><span data-stu-id="b0da3-264">Chromium issue: [#1093247][CR1093247]</span></span>  

#### <span data-ttu-id="b0da3-265">Detalles de trama para las ventanas abiertas</span><span class="sxs-lookup"><span data-stu-id="b0da3-265">Frame details for opened windows</span></span>  

<span data-ttu-id="b0da3-266">Las ventanas abiertas y las ventanas emergentes se muestran ahora también en el árbol de Marcos.</span><span class="sxs-lookup"><span data-stu-id="b0da3-266">Open windows and pop-up windows now display under the frame tree as well.</span></span>  <span data-ttu-id="b0da3-267">La vista detallada de las ventanas abiertas incluye información de seguridad adicional.</span><span class="sxs-lookup"><span data-stu-id="b0da3-267">The detailed view of the opened windows includes additional security information.</span></span>  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/window-opener.msft.png":::
   <span data-ttu-id="b0da3-269">Vista detallada de nuevo marco para ventanas abiertas</span><span class="sxs-lookup"><span data-stu-id="b0da3-269">New frame detailed view for opened windows</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-270">Error de cromo: [#1107766] [CR1107766]</span><span class="sxs-lookup"><span data-stu-id="b0da3-270">Chromium issue: [#1107766][CR1107766]</span></span>  

#### <span data-ttu-id="b0da3-271">Información de seguridad y aislamiento</span><span class="sxs-lookup"><span data-stu-id="b0da3-271">Security and isolation information</span></span>  

<span data-ttu-id="b0da3-272">En los detalles de la trama, ahora se muestra el contexto seguro, la [Directiva de origen cruzado-Embedder (COEP)][WebDevCoopCoep]y las [directivas de apertura cruzada entre orígenes (COOP)][WebDevCoopCoep] .</span><span class="sxs-lookup"><span data-stu-id="b0da3-272">Secure context, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep], and [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] are now displayed in the frame details.</span></span>  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/coep-coop.msft.png":::
   <span data-ttu-id="b0da3-274">Información de seguridad y aislamiento</span><span class="sxs-lookup"><span data-stu-id="b0da3-274">Security and isolation information</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-275">En el futuro, el equipo de Microsoft Edge DevTools y el equipo de Chrome DevTools planean agregar más información de seguridad a los detalles del marco.</span><span class="sxs-lookup"><span data-stu-id="b0da3-275">In the future, the Microsoft Edge DevTools team and the Chrome DevTools team are planning to add more security information to the frame details.</span></span>  

<span data-ttu-id="b0da3-276">Problema de cromo: [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="b0da3-276">Chromium issue: [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="b0da3-277">Elementos y actualizaciones del panel de red</span><span class="sxs-lookup"><span data-stu-id="b0da3-277">Elements and Network panel updates</span></span>  

#### <span data-ttu-id="b0da3-278">Sugerencia de color accesible en el panel estilos</span><span class="sxs-lookup"><span data-stu-id="b0da3-278">Accessible color suggestion in the Styles pane</span></span>  

<span data-ttu-id="b0da3-279">DevTools ahora ofrece sugerencias de color para el texto de contraste de color bajo.</span><span class="sxs-lookup"><span data-stu-id="b0da3-279">DevTools now provides color suggestions for low color contrast text.</span></span>  

<span data-ttu-id="b0da3-280">En el ejemplo siguiente, `h1` hay texto de bajo contraste.</span><span class="sxs-lookup"><span data-stu-id="b0da3-280">In the example below, `h1` has low contrast text.</span></span>  <span data-ttu-id="b0da3-281">Para corregirlo, abra el selector de color de la `color` propiedad en el panel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="b0da3-281">To fix it, open the color picker of the `color` property in the **Styles** pane.</span></span>  <span data-ttu-id="b0da3-282">Después de expandir la sección **relación de contraste** , DevTools ofrece sugerencias de color AA y AAA.</span><span class="sxs-lookup"><span data-stu-id="b0da3-282">After you expand the **Contrast ratio** section, DevTools provides AA and AAA color suggestions.</span></span>  <span data-ttu-id="b0da3-283">Seleccione el color sugerido para aplicar el color.</span><span class="sxs-lookup"><span data-stu-id="b0da3-283">Select the suggested color to apply the color.</span></span>  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   <span data-ttu-id="b0da3-285">El selector de colores sugiere sugerencias de color AA y AAA</span><span class="sxs-lookup"><span data-stu-id="b0da3-285">Color picker suggests AA and AAA color suggestions</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-286">Problema de cromo: [#1093227][CR1093227]</span><span class="sxs-lookup"><span data-stu-id="b0da3-286">Chromium issue: [#1093227][CR1093227]</span></span>  

#### <span data-ttu-id="b0da3-287">Panel de propiedades de restablecer en el panel elementos</span><span class="sxs-lookup"><span data-stu-id="b0da3-287">Reinstate Properties pane in the Elements panel</span></span>  

<span data-ttu-id="b0da3-288">El panel **propiedades** está atrás.</span><span class="sxs-lookup"><span data-stu-id="b0da3-288">The **Properties** pane is back.</span></span>  <span data-ttu-id="b0da3-289">Quedó [obsoleto en Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span><span class="sxs-lookup"><span data-stu-id="b0da3-289">It was [deprecated in Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span></span>  <span data-ttu-id="b0da3-290">El equipo de Microsoft Edge DevTools y el equipo de Chrome DevTools están planeando las mejoras para inspeccionar las propiedades de los elementos.</span><span class="sxs-lookup"><span data-stu-id="b0da3-290">The Microsoft Edge DevTools team and the Chrome DevTools team are planning improvements for inspecting properties of elements.</span></span>  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/properties-pane.msft.png":::
   <span data-ttu-id="b0da3-292">Panel de **propiedades** en el panel **elementos**</span><span class="sxs-lookup"><span data-stu-id="b0da3-292">**Properties** pane in the **Elements** panel</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-293">Problema de cromo:</span><span class="sxs-lookup"><span data-stu-id="b0da3-293">Chromium issue:</span></span>  <!--  [#1105205][CR1105205],  -->  <span data-ttu-id="b0da3-294">[#1116085] [CR1116085]</span><span class="sxs-lookup"><span data-stu-id="b0da3-294">[#1116085][CR1116085]</span></span>  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <span data-ttu-id="b0da3-295">Autocompletar fuentes personalizadas en el panel estilos</span><span class="sxs-lookup"><span data-stu-id="b0da3-295">Autocomplete custom fonts in the Styles pane</span></span>  

<span data-ttu-id="b0da3-296">Las caras de las fuentes importadas se agregan ahora a la lista de autocompletar CSS al editar la `font-family` propiedad en el panel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="b0da3-296">Imported font faces are now added to the list of CSS autocompletion when editing the `font-family` property in the **Styles** pane.</span></span>  

<span data-ttu-id="b0da3-297">Por ejemplo, si `monospace` es una fuente personalizada instalada en la máquina local, se muestra en la lista de finalización de CSS.</span><span class="sxs-lookup"><span data-stu-id="b0da3-297">For example, if `monospace` is a custom font installed on the local machine, it's displayed in the CSS completion list.</span></span> <span data-ttu-id="b0da3-298">En versiones anteriores de Microsoft Edge, no se mostraba la fuente.</span><span class="sxs-lookup"><span data-stu-id="b0da3-298">In previous versions of Microsoft Edge, the font wasn't displayed.</span></span>

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   <span data-ttu-id="b0da3-300">Autocompletar fuentes personalizadas</span><span class="sxs-lookup"><span data-stu-id="b0da3-300">Autocomplete custom fonts</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-301">Error de cromo: [#1106221] [CR1106221]</span><span class="sxs-lookup"><span data-stu-id="b0da3-301">Chromium issue: [#1106221][CR1106221]</span></span>  

#### <span data-ttu-id="b0da3-302">Mostrar el tipo de recurso de forma coherente en el panel red</span><span class="sxs-lookup"><span data-stu-id="b0da3-302">Consistently display resource type in Network panel</span></span>  

<span data-ttu-id="b0da3-303">DevTools ahora muestra el mismo tipo de recurso que la solicitud de red original y anexa `/ Redirect` al valor de la columna **Type** cuando el redireccionamiento ha transformado \ (código de estado http 302 \).</span><span class="sxs-lookup"><span data-stu-id="b0da3-303">DevTools now consistently display the same resource type as the original network request and appends `/ Redirect` to the **Type** column value when redirection \(HTTP status code 302\) happens.</span></span>  

<span data-ttu-id="b0da3-304">Anteriormente DevTools cambiado el tipo a `Other` veces.</span><span class="sxs-lookup"><span data-stu-id="b0da3-304">Previously DevTools changed the type to `Other` sometimes.</span></span>  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/network-redirect.msft.png":::
   <span data-ttu-id="b0da3-306">Mostrar tipo de recurso de redirección</span><span class="sxs-lookup"><span data-stu-id="b0da3-306">Display redirect resource type</span></span>  
:::image-end:::  

<span data-ttu-id="b0da3-307">Problema de cromo: [#997694][CR997694]</span><span class="sxs-lookup"><span data-stu-id="b0da3-307">Chromium issue: [#997694][CR997694]</span></span>  

#### <span data-ttu-id="b0da3-308">Botones borrar en los paneles elementos y red</span><span class="sxs-lookup"><span data-stu-id="b0da3-308">Clear buttons in the Elements and Network panels</span></span>  

<span data-ttu-id="b0da3-309">Los siguientes cuadros de texto ahora tienen botones **claros** .</span><span class="sxs-lookup"><span data-stu-id="b0da3-309">The following text boxes now have **Clear** buttons.</span></span>  

*   <span data-ttu-id="b0da3-310">Los cuadros de texto de filtro en el panel **estilos** y en el panel **red** .</span><span class="sxs-lookup"><span data-stu-id="b0da3-310">The filter text boxes in the **Styles** pane and **Network** panel.</span></span>  
*   <span data-ttu-id="b0da3-311">Cuadro de texto de búsqueda de DOM en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="b0da3-311">The DOM search text box in the **Elements** panel.</span></span>  

<span data-ttu-id="b0da3-312">Haga clic en el botón **Borrar** para quitar el texto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="b0da3-312">Choose the **Clear** button to remove any inputted text.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         <span data-ttu-id="b0da3-314">Botones Borrar de los paneles **elementos**</span><span class="sxs-lookup"><span data-stu-id="b0da3-314">Clear buttons in the **Elements** panels</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         <span data-ttu-id="b0da3-316">Botones borrar en los paneles de **red**</span><span class="sxs-lookup"><span data-stu-id="b0da3-316">Clear buttons in the  **Network** panels</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="b0da3-317">Problema de cromo: [#1067184][CR1067184]</span><span class="sxs-lookup"><span data-stu-id="b0da3-317">Chromium issue: [#1067184][CR1067184]</span></span>  

## <span data-ttu-id="b0da3-318">Descargar los canales de Microsoft Edge Preview</span><span class="sxs-lookup"><span data-stu-id="b0da3-318">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="b0da3-319">Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b0da3-319">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="b0da3-320">Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0da3-320">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="b0da3-321">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b0da3-321">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Icono configuración de DevTools"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Desuso del panel de propiedades en el panel de elementos: novedades de DevTools (Microsoft Edge 84) | Microsoft docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Características de depuración de la cuadrícula CSS: novedades de DevTools (Microsoft Edge 85) | Microsoft docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar los métodos abreviados de teclado en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Habilitar las API experimentales: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulación: compatibilidad con el modo de pantalla dual-características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Habilitar visor de pedidos de origen-características experimentales | Microsoft docs"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Emulación: compatibilidad con el modo de pantalla dual-características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Pruebas en dispositivos de plegable y dos pantallas: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tabla-referencia de API de consola | Microsoft docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Buscar código JavaScript y CSS sin usar con la pestaña cobertura en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Cajón-personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analizar el rendimiento de la representación con la pestaña representación, referencia de análisis de rendimiento | Microsoft docs"  
[DevtoolsMediaPanelIndex]: /microsoft-edge/devtools-guide-chromium/media-panel/index "Ver y depurar información de reproductores multimedia | Microsoft docs"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con las costuras-Introducción a los dispositivos de doble pantalla | Microsoft docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Característica de expansión de pantalla multimedia CSS para detección de pantalla doble | Microsoft docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript de getWindowSegments para dispositivos de doble pantalla | Microsoft docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de Microsoft Edge Preview"  

[VisualStudioCode]: https://code.visualstudio.com "Código de Visual Studio "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Métodos abreviados de teclado de código de Visual Studio para Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "La nueva superficie Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de cromo"  

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar métodos abreviados de teclado o enlaces de clave | Errores de cromo"
[CR384968]: https://crbug.com/384968 "Opción para omitir las fuentes locales () | Errores de cromo"  
[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la última versión de Lighthouse | Errores de cromo"  
[CR807440]: https://crbug.com/807440 "Chrome se bloquea con grandes cantidades de SWs | Errores de cromo"  
[CR997694]: https://crbug.com/997694 "Las solicitudes de XHR con el estado 302 no se muestran en el filtro \ "XHR \" en el panel red | Errores de cromo"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS/Flexbox/Table de CSS"  
[CR1051466]: https://crbug.com/1051466 "Compatibilidad con COOP/depuración COEP en DevTools | Errores de cromo"  
[CR1054281]: https://crbug.com/1054281 "Solicitud de característica: DevTools debe emular plegable y dispositivos de pantalla dual | Errores de cromo"  
[CR1067184]: https://crbug.com/1067184 "Solicitud de característica: botón Borrar filtro en los elementos del & de red: entradas del filtro de estilo de > | Errores de cromo"  
[CR1068116]: https://crbug.com/1068116 "Panel de problemas de envío de ☂ | Errores de cromo"  
[CR1080569]: https://crbug.com/1080569 "ACORN no admite operadores de asignación lógica | Errores de cromo"  
[CR1080589]: https://crbug.com/1080589 "Clasificar problemas por terceros o por terceros | Errores de cromo"  
[CR1086817]: https://crbug.com/1086817 "ACORN no admite separadores numéricos | Errores de cromo"  
[CR1090802]: https://crbug.com/1090802 "Simular cambios de estado de inactividad de API de detección de inactividad | Errores de cromo"  
[CR1093227]: https://crbug.com/1093227 "DevTools: sugerir color más accesible | Errores de cromo"  
[CR1093247]: https://crbug.com/1093247 "Mostrar información sobre marcos en el panel aplicación | Errores de cromo"  
[CR1094406]: https://crbug.com/1094406 "Los desarrolladores desean un visor de pedidos de origen para al https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: compatibilidad emulando la característica de medios de datos preferidos, menos-datos | Errores de cromo"  
[CR1096481]: https://crbug.com/1096481 "Ubicación del banner de problemas | Errores de cromo"  
[CR1100253]: https://crbug.com/1100253 "Agregar acceso directo al nodo de captura en el menú contextual del elemento | Errores de cromo"  
[CR1103316]: https://crbug.com/1103316 "La búsqueda de elementos no resolveNode (resaltar texto, etc.) en el primer resultado de búsqueda | Errores de cromo"  
[CR1103854]: https://crbug.com/1103854 "Desproteger los valores de datos de X-Client en herramientas para desarrolladores | Errores de cromo"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: https://crbug.com/1106221 "agregar fuentes importadas a la autocompletada de la familia de fuentes en el panel estilos | Errores de cromo "  
[CR1107766]: https://crbug.com/1107766 "Mostrar información sobre fotogramas generados por" Window. Open () "en árbol de marcos | Errores de cromo "  
[CR1115011]: https://crbug.com/1115011 "al copiar una tabla desde la consola, no se conserva la estructura de la tabla | Errores de cromo "  
[CR1116085]: https://crbug.com/1116085 "vuelve al inspector de propiedades de DevTools | Errores de cromo "  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "preferidas, menos-consultas de medios de datos nivel 5 | Borradores del editor del grupo de trabajo CSS W3C"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v 6.2.0-GoogleChrome/Lighthouse | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Búferes de protocolo | Desarrolladores de Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Plegado de Galaxy | Samsung, Estados Unidos"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Asignación lógica | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Separadores numéricos | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Cómo convertir tu sitio web \ "aislamiento de origen cruzado \" usando COOP y COEP | Web. dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Detectar usuarios inactivos con la API de detección de inactividad | Web. dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Evitar animaciones no compuestas | Web. dev"  

> [!NOTE]
> <span data-ttu-id="b0da3-382">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b0da3-382">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b0da3-383">La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/08/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \ (defensor para desarrolladores, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="b0da3-383">The original page is found [here](https://developers.google.com/web/updates/2020/08/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b0da3-385">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b0da3-385">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

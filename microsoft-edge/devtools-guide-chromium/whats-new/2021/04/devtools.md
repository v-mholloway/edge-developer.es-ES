---
description: Wavy subraya los problemas de código destacado en la herramienta Elementos, escala de tiempo de actualización del trabajador de servicio y mucho más.
title: Novedades de DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 5f499a6c9f1109f80a9d459edf94ed2226734f19
ms.sourcegitcommit: 87ba918b0910373bb645615377709bf140dc9b19
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "11583462"
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
# <a name="whats-new-in-devtools-microsoft-edge-91"></a><span data-ttu-id="4057e-104">Novedades de DevTools (Microsoft Edge 91)</span><span class="sxs-lookup"><span data-stu-id="4057e-104">What's New In DevTools (Microsoft Edge 91)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a><span data-ttu-id="4057e-105">Wavy subraya los problemas de código destacado y las mejoras en la herramienta Elementos</span><span class="sxs-lookup"><span data-stu-id="4057e-105">Wavy underlines highlight code issues and improvements in Elements tool</span></span>  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

<span data-ttu-id="4057e-106">En la mayoría de los identificadores modernos, los subrayados ondulados debajo del texto indican errores de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="4057e-106">In most modern IDEs, wavy underlines under text indicate syntax errors.</span></span>   <span data-ttu-id="4057e-107">En Microsoft Edge versión 91 o posterior, los subrayados ondulados se muestran en HTML en la vista **DOM** de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="4057e-107">In Microsoft Edge version 91 or later, wavy underlines display under HTML in the **DOM** view of the **Elements** tool.</span></span>  <span data-ttu-id="4057e-108">Los subrayados ondulados indican problemas de código y sugerencias relacionadas con la accesibilidad, la compatibilidad, el rendimiento, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="4057e-108">The wavy underlines indicate code issues and suggestions related to accessibility, compatibility, performance, and so on.</span></span>  <span data-ttu-id="4057e-109">Para obtener más información acerca de cómo revisar y editar problemas, vaya a Buscar y solucionar problemas con la [Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="4057e-109">For more information about how to review and edit issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

<span data-ttu-id="4057e-110">Para abrir la **herramienta Problemas** y obtener más información sobre el problema y cómo solucionarlo, complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4057e-110">To open the **Issues** tool and learn more about the issue and how to fix it, complete one of the following actions.</span></span>  

*   <span data-ttu-id="4057e-111">Seleccione y mantenga presionado y, a `Shift` continuación, elija cualquier subrayado ondulado.</span><span class="sxs-lookup"><span data-stu-id="4057e-111">Select and hold `Shift`, and then choose any wavy underline.</span></span>  
*   <span data-ttu-id="4057e-112">Complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4057e-112">Complete the following actions.</span></span>  
    1.  <span data-ttu-id="4057e-113">Mantenga el mouse sobre cualquier subrayado ondulado.</span><span class="sxs-lookup"><span data-stu-id="4057e-113">Hover on any wavy underline.</span></span>  
    1.  <span data-ttu-id="4057e-114">Abra el menú contextual \(haga clic con el botón derecho\).</span><span class="sxs-lookup"><span data-stu-id="4057e-114">Open the contextual menu \(right-click\).</span></span>  
    1.  <span data-ttu-id="4057e-115">Elija **Mostrar en Problemas**.</span><span class="sxs-lookup"><span data-stu-id="4057e-115">Choose **Show in Issues**.</span></span>  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Elija el error subrayado en la herramienta Elementos" lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         <span data-ttu-id="4057e-117">Elija el error subrayado en la **herramienta** Elementos</span><span class="sxs-lookup"><span data-stu-id="4057e-117">Choose the underlined error in the **Elements** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Mostrar detalles de error en la herramienta Problemas" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         <span data-ttu-id="4057e-119">Mostrar detalles de error en la **herramienta Problemas**</span><span class="sxs-lookup"><span data-stu-id="4057e-119">Display error details in the **Issues** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="4057e-120">Aprenda más sobre DevTools con la información sobre herramientas informativas</span><span class="sxs-lookup"><span data-stu-id="4057e-120">Learn about DevTools with informative tooltips</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

<span data-ttu-id="4057e-121">La característica DevTools Tooltips le ayuda a obtener información sobre todas las diferentes herramientas y paneles de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4057e-121">The DevTools Tooltips feature helps you learn about all the different tools and panes in DevTools.</span></span>  <span data-ttu-id="4057e-122">Para desactivar la información sobre herramientas, seleccione `Esc` .</span><span class="sxs-lookup"><span data-stu-id="4057e-122">To turn off Tooltips, select `Esc`.</span></span>  <span data-ttu-id="4057e-123">Para activar información sobre herramientas, complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4057e-123">To turn on Tooltips, complete one of the following actions.</span></span>  

*   <span data-ttu-id="4057e-124">Seleccione `Ctrl` + `Shift` + `H` \(Windows/Linux\) o `Cmd` + `Shift` + `H` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="4057e-124">Select `Ctrl`+`Shift`+`H` \(Windows/Linux\) or `Cmd`+`Shift`+`H` \(macOS\).</span></span>  
*   <span data-ttu-id="4057e-125">[Abra el menú comando y,][DevtoolsCommandMenuIndexOpenCommandMenu] a continuación, escriba `tooltips` .</span><span class="sxs-lookup"><span data-stu-id="4057e-125">[Open the Command Menu][DevtoolsCommandMenuIndexOpenCommandMenu] and then type `tooltips`.</span></span>  
*   <span data-ttu-id="4057e-126">Elija **Personalizar y controlar DevTools** \( \) > Ayuda para alternar la información sobre herramientas de `...` \*\*\*\*  >  **DevTools**.</span><span class="sxs-lookup"><span data-stu-id="4057e-126">Choose **Customize and control DevTools** \(`...`\) > **Help** > **Toggle the DevTools Tooltips**.</span></span>  

<span data-ttu-id="4057e-127">Además, si activa el experimento Modo de enfoque y Información sobre herramientas [de DevTools,][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] también puede elegir el botón Alternar la información sobre herramientas **de DevTools** \( \) en la parte inferior de la barra de `?` **actividades**.</span><span class="sxs-lookup"><span data-stu-id="4057e-127">Also, if you turn on the [Focus Mode and DevTools Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] experiment, you may also choose the **Toggle the DevTools Tooltips** \(`?`\) button at the bottom of the **Activity Bar**.</span></span>  

<span data-ttu-id="4057e-128">Para mostrar más información sobre cómo usar DevTools, active Información sobre herramientas y, a continuación, mantenga el mouse en cada región de esquema de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4057e-128">To display more information about how to use the DevTools, turn on Tooltips, and then hover on each outlined region of the DevTools.</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Mantenga el mouse en cualquier lugar de la región resaltada de la herramienta Problemas para mostrar más detalles" lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   <span data-ttu-id="4057e-130">Mantenga el mouse en cualquier lugar de la región resaltada de la **herramienta Problemas** para mostrar más detalles</span><span class="sxs-lookup"><span data-stu-id="4057e-130">Hover on anywhere in the highlighted region of the **Issues** tool to display more details</span></span>  
:::image-end:::  

## <a name="service-worker-update-timeline"></a><span data-ttu-id="4057e-131">Escala de tiempo de actualización del trabajador de servicio</span><span class="sxs-lookup"><span data-stu-id="4057e-131">Service worker update timeline</span></span>  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

<span data-ttu-id="4057e-132">En Microsoft Edge versión 91 o posterior, si eres desarrollador de aplicación web progresiva o trabajador de servicio, muestra el ciclo de vida de actualización de los trabajadores de servicio como una escala de tiempo en la herramienta **Aplicación.**</span><span class="sxs-lookup"><span data-stu-id="4057e-132">In Microsoft Edge version 91 or later, if you're a Progressive Web App or Service Worker developer, display the update lifecycle of your Service Workers as a timeline in the **Application** tool.</span></span>  <span data-ttu-id="4057e-133">Esta característica le ayuda a comprender el tiempo que el trabajador de servicio pasa en cada una de las siguientes fases.</span><span class="sxs-lookup"><span data-stu-id="4057e-133">This feature helps you understand the time your Service Worker spends in each of the following stages.</span></span>  

*   **<span data-ttu-id="4057e-134">Instalar</span><span class="sxs-lookup"><span data-stu-id="4057e-134">Install</span></span>**  
*   **<span data-ttu-id="4057e-135">Esperar</span><span class="sxs-lookup"><span data-stu-id="4057e-135">Wait</span></span>**  
*   **<span data-ttu-id="4057e-136">Activar</span><span class="sxs-lookup"><span data-stu-id="4057e-136">Activate</span></span>**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Revisar la escala de tiempo del ciclo de actualización para el trabajador de servicio" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   <span data-ttu-id="4057e-138">Revisar la **escala de** tiempo del ciclo **de actualización** para el trabajador de servicio</span><span class="sxs-lookup"><span data-stu-id="4057e-138">Review the **Timeline** in the **Update Cycle** for your Service Worker</span></span>  
:::image-end:::  

<span data-ttu-id="4057e-139">Para obtener más información sobre el ciclo de vida de los trabajadores de servicio, vaya a [El ciclo de vida del trabajador de servicio][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span><span class="sxs-lookup"><span data-stu-id="4057e-139">For more information about the lifecycle of your Service Workers, navigate to [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span></span>  <span data-ttu-id="4057e-140">Para obtener más información acerca de las herramientas de depuración para las aplicaciones web progresivas y los trabajadores de servicio en DevTools, vaya a [Mejoras del trabajador de servicio][DevtoolsServiceWorkerIndex].</span><span class="sxs-lookup"><span data-stu-id="4057e-140">For more information about debugging tools for Progressive Web Apps and Service Workers in the DevTools, navigate to [Service Worker improvements][DevtoolsServiceWorkerIndex].</span></span>  <span data-ttu-id="4057e-141">Para revisar las actualizaciones en tiempo real de esta característica en Chromium proyecto de código abierto, vaya al problema [1066604][CR1066604].</span><span class="sxs-lookup"><span data-stu-id="4057e-141">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1066604][CR1066604].</span></span>  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a><span data-ttu-id="4057e-142">Las aplicaciones web progresivas ya no muestran advertencias para iconos que no son cuadrados</span><span class="sxs-lookup"><span data-stu-id="4057e-142">Progressive Web Apps no longer display warnings for non-square icons</span></span>  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

<span data-ttu-id="4057e-143">En Microsoft Edge versión [90][DevtoolsWhatsNew202102Devtools] o anterior, si el manifiesto de aplicación web de su PWA incluía un icono que no es cuadrado, se muestra una advertencia en la sección Errores y **advertencias** para cada icono que no sea cuadrado.</span><span class="sxs-lookup"><span data-stu-id="4057e-143">In [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] or earlier, if the Web App Manifest of your PWA included a non-square icon, a warning was displayed in the **Errors and Warnings**  section for each non-square icon.</span></span>  <span data-ttu-id="4057e-144">En Microsoft Edge versión 91 o \*\*\*\* posterior, la \*\*\*\* sección Manifiesto de la herramienta Aplicación no muestra advertencias si proporciona al menos un icono cuadrado.</span><span class="sxs-lookup"><span data-stu-id="4057e-144">In Microsoft Edge version 91 or later, the **Manifest** section in the **Application** tool displays no warnings if you provide at least one square icon.</span></span>  <span data-ttu-id="4057e-145">Si no proporciona ningún icono cuadrado, una advertencia muestra el siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="4057e-145">If you don't provide any square icons, a warning displays the following message.</span></span>  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="En Microsoft Edge versión 90 o anterior, se muestra un error para cada icono que no es cuadrado" lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="4057e-147">En Microsoft Edge versión 90 o anterior, se muestra un error para cada icono que no es cuadrado</span><span class="sxs-lookup"><span data-stu-id="4057e-147">In Microsoft Edge version 90 or earlier, an error displays for each icon that is non-square</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="En Microsoft Edge versión 91 o posterior, no se muestra ningún error al proporcionar al menos un icono cuadrado" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="4057e-149">En Microsoft Edge versión 91 o posterior, no se muestra ningún error al proporcionar al menos un icono cuadrado</span><span class="sxs-lookup"><span data-stu-id="4057e-149">In Microsoft Edge version 91 or later, no error displays when you provide at least one square icon</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="4057e-150">Para revisar errores y advertencias en el manifiesto de la aplicación web, vaya a la **herramienta Aplicación** y elija la **sección** Manifiesto.</span><span class="sxs-lookup"><span data-stu-id="4057e-150">To review errors and warnings in your Web App Manifest, navigate to the **Application** tool and choose the **Manifest** section.</span></span>  <span data-ttu-id="4057e-151">Los errores y advertencias se enumeran en el **encabezado Errores y advertencias.**</span><span class="sxs-lookup"><span data-stu-id="4057e-151">Errors and warnings are listed under the **Errors and Warnings** heading.</span></span>  <span data-ttu-id="4057e-152">Para obtener más información sobre el manifiesto de aplicación web, vaya a Usar el manifiesto de aplicación [web para integrar la aplicación web progresiva en el sistema operativo][ProgressiveWebAppsWebappmanifests].</span><span class="sxs-lookup"><span data-stu-id="4057e-152">For more information about the Web App Manifest, navigate to [Use the Web App Manifest to integrate your Progressive Web App into the Operating System][ProgressiveWebAppsWebappmanifests].</span></span>  <span data-ttu-id="4057e-153">Para crear iconos para incluir en el manifiesto de la aplicación web, vaya al Generador de [imágenes de PWABuilder][PwabuilderImagegenerator].</span><span class="sxs-lookup"><span data-stu-id="4057e-153">To create icons to include in your Web App Manifest, navigate to the [PWABuilder Image Generator][PwabuilderImagegenerator].</span></span>  <span data-ttu-id="4057e-154">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto Chromium, vaya al problema [1185945][CR1185945].</span><span class="sxs-lookup"><span data-stu-id="4057e-154">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1185945][CR1185945].</span></span>  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a><span data-ttu-id="4057e-155">Localized DevTools ahora es compatible con Chromium exploradores basados en aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4057e-155">Localized DevTools now supported in Chromium-based browsers</span></span>  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

<span data-ttu-id="4057e-156">A partir [Microsoft Edge versión 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools se muestra en su propio idioma.</span><span class="sxs-lookup"><span data-stu-id="4057e-156">Starting in [Microsoft Edge version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools displays in your own language.</span></span>  <span data-ttu-id="4057e-157">Muchos desarrolladores usan otras herramientas de desarrollador como StackOverflow y Visual Studio Code en su idioma nativo, no solo en inglés.</span><span class="sxs-lookup"><span data-stu-id="4057e-157">Many developers use other developer tools like StackOverflow and Visual Studio Code in their native language, not just in English.</span></span>  <span data-ttu-id="4057e-158">El Microsoft Edge de DevTools, el equipo de Chrome DevTools y el equipo de Google Lighthouse colaboraron para proporcionar la misma experiencia en todos los exploradores basados en Chromium web.</span><span class="sxs-lookup"><span data-stu-id="4057e-158">The Microsoft Edge DevTools team, Chrome DevTools team, and the Google Lighthouse team collaborated to provide the same experience in all Chromium-based browsers.</span></span>  <span data-ttu-id="4057e-159">Para obtener más información sobre cómo usar DevTools en su idioma, vaya a [Cambiar la configuración de idioma de DevTools][DevtoolsCustomizeLocalization].</span><span class="sxs-lookup"><span data-stu-id="4057e-159">For more information about how to use DevTools in your language, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  <span data-ttu-id="4057e-160">Para obtener más información sobre la colaboración en esta característica en el proyecto de código abierto Chromium, vaya a [1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="4057e-160">For more information about the collaboration on this feature in the Chromium open-source project, navigate to [1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge explorador y DevTools establecidos en japonés" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   <span data-ttu-id="4057e-162">Microsoft Edge explorador y DevTools establecidos en japonés</span><span class="sxs-lookup"><span data-stu-id="4057e-162">Microsoft Edge browser and DevTools set to Japanese</span></span>  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a><span data-ttu-id="4057e-163">Usar el teclado para navegar a variables CSS</span><span class="sxs-lookup"><span data-stu-id="4057e-163">Use the keyboard to navigate to CSS variables</span></span>  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

<span data-ttu-id="4057e-164">A partir [Microsoft Edge versión 88,][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]el panel **Estilos** muestra variables CSS y proporciona un vínculo directamente a la definición de cada variable.</span><span class="sxs-lookup"><span data-stu-id="4057e-164">Starting in [Microsoft Edge version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], the **Styles** pane displays CSS variables and provides a link directly to the definition of each variable.</span></span>  <span data-ttu-id="4057e-165">En Microsoft Edge versión 91 o posterior, puede usar las teclas de flecha para navegar fácilmente a las variables CSS.</span><span class="sxs-lookup"><span data-stu-id="4057e-165">In Microsoft Edge version 91 or later, you may use the arrow keys to easily navigate to CSS variables.</span></span>  <span data-ttu-id="4057e-166">Para abrir la definición en el panel **Estilos,** mantenga el mouse en una variable y, a continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4057e-166">To open the definition in the **Styles** pane, hover on a variable, and then select `Enter`.</span></span>  <span data-ttu-id="4057e-167">Para obtener más información acerca de las variables CSS, vaya [a Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span><span class="sxs-lookup"><span data-stu-id="4057e-167">For more information about CSS variables, navigate to [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span></span>  <span data-ttu-id="4057e-168">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto de Chromium, vaya al problema [1187735][CR1187735].</span><span class="sxs-lookup"><span data-stu-id="4057e-168">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1187735][CR1187735].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Variable CSS --theme-body-background resaltada en el panel Estilos" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   <span data-ttu-id="4057e-170">Variable `--theme-body-background` CSS resaltada en el **panel Estilos**</span><span class="sxs-lookup"><span data-stu-id="4057e-170">The `--theme-body-background` CSS variable highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a><span data-ttu-id="4057e-171">Los problemas se ordenan automáticamente por gravedad</span><span class="sxs-lookup"><span data-stu-id="4057e-171">Issues are automatically sorted by severity</span></span>  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

<span data-ttu-id="4057e-172">La **herramienta Problemas** muestra recomendaciones para mejorar el sitio web, incluida la accesibilidad, el rendimiento, la seguridad, entre otros.</span><span class="sxs-lookup"><span data-stu-id="4057e-172">The **Issues** tool displays recommendations to improve your website, including accessibility, performance, security, and so on.</span></span> <span data-ttu-id="4057e-173">En función de sus comentarios, los problemas ahora se ordenan automáticamente por gravedad.</span><span class="sxs-lookup"><span data-stu-id="4057e-173">Based on your feedback, issues are now automatically sorted by severity.</span></span>  <span data-ttu-id="4057e-174">En cada categoría de comentarios, cada problema marcado como **error** aparece primero, seguido de cada problema marcado como advertencia **y,** a continuación, cada problema marcado como **sugerencia**.</span><span class="sxs-lookup"><span data-stu-id="4057e-174">In each feedback category, each issue marked as an **Error** appears first, followed each issue marked as a **Warning**, then each issue marked as a **Tip**.</span></span>  <span data-ttu-id="4057e-175">Para ayudarle a refinar sus problemas, se planean opciones de filtro adicionales para una actualización futura.</span><span class="sxs-lookup"><span data-stu-id="4057e-175">To help you refine your issues, extra filter options are planned for a future update.</span></span>  <span data-ttu-id="4057e-176">Para obtener más información acerca de cómo revisar problemas, vaya a Buscar y solucionar problemas con la [Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="4057e-176">For more information about how to review issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="La herramienta Problemas muestra los problemas ordenados por gravedad" lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   <span data-ttu-id="4057e-178">La **herramienta Problemas** muestra los problemas ordenados por gravedad</span><span class="sxs-lookup"><span data-stu-id="4057e-178">The **Issues** tool displays sorted issues by severity</span></span>  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a><span data-ttu-id="4057e-179">Microsoft Edge Developer Tools for Visual Studio Code versión 1.1.7</span><span class="sxs-lookup"><span data-stu-id="4057e-179">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.7</span></span>  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

<span data-ttu-id="4057e-180">El [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 proporciona DevTools de Microsoft Edge versión [88][DevtoolsWhatsNew202011Devtools].</span><span class="sxs-lookup"><span data-stu-id="4057e-180">The [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 provides the DevTools from [Microsoft Edge version 88][DevtoolsWhatsNew202011Devtools].</span></span>  <span data-ttu-id="4057e-181">Esta extensión ahora admite ARM dispositivos y ya no depende del [depurador para Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extensión.</span><span class="sxs-lookup"><span data-stu-id="4057e-181">This extension now supports ARM devices and no longer depends on the [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extension.</span></span>  <span data-ttu-id="4057e-182">La versión 1.1.7 incluye las siguientes correcciones de errores y mejoras.</span><span class="sxs-lookup"><span data-stu-id="4057e-182">Version 1.1.7 includes the following bug fixes and improvements.</span></span>  

*   <span data-ttu-id="4057e-183">Se actualizó la confiabilidad del cierre de destino.</span><span class="sxs-lookup"><span data-stu-id="4057e-183">Updated the reliability of target closure.</span></span>  
*   <span data-ttu-id="4057e-184">Se actualizó el panel lateral para que se actualice automáticamente al depurar los destinos que se crean o destruyen.</span><span class="sxs-lookup"><span data-stu-id="4057e-184">Updated the side panel to automatically refreshes when you debug targets that are created or destroyed.</span></span>  
*   <span data-ttu-id="4057e-185">Se agregó un nuevo menú contextual que le ofrece un acceso más rápido a la configuración de extensión y al registro de cambios más reciente.</span><span class="sxs-lookup"><span data-stu-id="4057e-185">Added a new contextual menu that gives you faster access to the extension settings and the latest Changelog.</span></span>  
*   <span data-ttu-id="4057e-186">Se actualizó y simplificó la versión de la documentación de extensión, incluidas las características más nuevas.</span><span class="sxs-lookup"><span data-stu-id="4057e-186">Updated and simplified the release of extension documentation including the newest features.</span></span>  
    
<span data-ttu-id="4057e-187">Para actualizar manualmente a la versión 1.1.7, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="4057e-187">To manually update to version 1.1.7, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="4057e-188">Puede archivar los problemas y contribuir con la extensión en el [repositorio de GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="4057e-188">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="4057e-189">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="4057e-189">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="visualize-css-scroll-snap"></a><span data-ttu-id="4057e-190">Visualizar ajuste de desplazamiento CSS</span><span class="sxs-lookup"><span data-stu-id="4057e-190">Visualize CSS scroll-snap</span></span>  

<span data-ttu-id="4057e-191">Ahora puede alternar el distintivo en la herramienta Elementos para inspeccionar la alineación de ajuste de desplazamiento `scroll-snap` CSS. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4057e-191">You may now toggle the `scroll-snap` badge in the **Elements** tool to inspect the CSS scroll-snap alignment.</span></span>  <span data-ttu-id="4057e-192">Cuando se aplica un elemento HTML en la página web, se muestra un distintivo junto a él `scroll-snap-type` `scroll-snap` en la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="4057e-192">When an HTML element on your webpage has `scroll-snap-type` applied to it, a `scroll-snap` badge displays next to it in the **Elements** tool.</span></span>  <span data-ttu-id="4057e-193">Elija el distintivo para activar \(or off\) la presentación de una superposición de ajuste de desplazamiento en la página web.</span><span class="sxs-lookup"><span data-stu-id="4057e-193">Choose the badge to turn on \(or off\) the display of a scroll-snap overlay on the webpage.</span></span>  <span data-ttu-id="4057e-194">Para revisar una página web de ejemplo, vaya a [Scroll Acoplar Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].</span><span class="sxs-lookup"><span data-stu-id="4057e-194">To review an example webpage, navigate to [Scroll Snap Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].</span></span>  <span data-ttu-id="4057e-195">En el ejemplo, los puntos se muestran en bordes de ajuste.</span><span class="sxs-lookup"><span data-stu-id="4057e-195">In the example, dots display on snap edges.</span></span>  <span data-ttu-id="4057e-196">El puerto de desplazamiento tiene un esquema sólido mientras que los elementos de ajuste tienen contornos de guión.</span><span class="sxs-lookup"><span data-stu-id="4057e-196">The scroll port has a solid outline while the snap items have dash outlines.</span></span>  <span data-ttu-id="4057e-197">El relleno de desplazamiento se rellena en verde mientras el margen de desplazamiento se rellena en naranja.</span><span class="sxs-lookup"><span data-stu-id="4057e-197">The scroll padding is filled in green while the scroll margin is filled in orange.</span></span>  <span data-ttu-id="4057e-198">Para revisar el historial de esta característica en el Chromium de código abierto, vaya al problema [862450][CR862450].</span><span class="sxs-lookup"><span data-stu-id="4057e-198">To review the history of this feature in the Chromium open-source project, navigate to Issue [862450][CR862450].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-scroll-snap-highlight.msft.png" alt-text="Complemento de desplazamiento CSS" lightbox="../../media/2021/04/elements-scroll-snap-highlight.msft.png":::
   <span data-ttu-id="4057e-200">Complemento de desplazamiento CSS</span><span class="sxs-lookup"><span data-stu-id="4057e-200">CSS scroll-snap</span></span>  
:::image-end:::  

### <a name="new-memory-inspector-tool"></a><span data-ttu-id="4057e-201">Nueva herramienta inspector de memoria</span><span class="sxs-lookup"><span data-stu-id="4057e-201">New Memory Inspector tool</span></span>  

<span data-ttu-id="4057e-202">Use la nueva **herramienta Inspector de** memoria para inspeccionar una memoria de `ArrayBuffer` JavaScript y Wasm.</span><span class="sxs-lookup"><span data-stu-id="4057e-202">Use the new **Memory Inspector** tool to inspect an `ArrayBuffer` in JavaScript and Wasm memory.</span></span>  <span data-ttu-id="4057e-203">Abra la [página web de demostración memoria en JS.][GlitchMemoryInspectorDemoJsHtml]</span><span class="sxs-lookup"><span data-stu-id="4057e-203">Open the [Memory in JS][GlitchMemoryInspectorDemoJsHtml] demo webpage.</span></span>  <span data-ttu-id="4057e-204">En la **herramienta Orígenes,** abra el `memory-write-wasm` archivo y establezca un punto de interrupción en la línea `0x03c` .</span><span class="sxs-lookup"><span data-stu-id="4057e-204">In the **Sources** tool, open the `memory-write-wasm` file, and set a breakpoint at line `0x03c`.</span></span>  <span data-ttu-id="4057e-205">Actualice la página web.</span><span class="sxs-lookup"><span data-stu-id="4057e-205">Refresh the webpage.</span></span>  <span data-ttu-id="4057e-206">Expanda la **sección Ámbito** en el panel del depurador.</span><span class="sxs-lookup"><span data-stu-id="4057e-206">Expand the **Scope** section in the debugger pane.</span></span>  <span data-ttu-id="4057e-207">El nuevo icono se muestra junto al valor **del búfer.**</span><span class="sxs-lookup"><span data-stu-id="4057e-207">The new icon is displayed next to the **buffer** value.</span></span>  <span data-ttu-id="4057e-208">Elirá para abrir la nueva **herramienta Inspector de** memoria.</span><span class="sxs-lookup"><span data-stu-id="4057e-208">Choose it to open the new **Memory Inspector** tool.</span></span>  

<span data-ttu-id="4057e-209">Para obtener más información sobre la depuración en la **herramienta Orígenes,** vaya a Usar el [panel Depurador para depurar código JavaScript][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode].</span><span class="sxs-lookup"><span data-stu-id="4057e-209">To learn more about debugging in the **Sources** tool, navigate to [Using the Debugger pane to debug JavaScript code][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode].</span></span>  <span data-ttu-id="4057e-210">Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya al problema [1166577][CR1166577].</span><span class="sxs-lookup"><span data-stu-id="4057e-210">To review the history of this feature in the Chromium open-source project, navigate to Issue [1166577][CR1166577].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png" alt-text="Herramienta Inspector de memoria" lightbox="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png":::
   <span data-ttu-id="4057e-212">**Herramienta inspector de** memoria</span><span class="sxs-lookup"><span data-stu-id="4057e-212">**Memory inspector** tool</span></span>  
:::image-end:::  

### <a name="new-badge-settings-pane-in-the-elements-tool"></a><span data-ttu-id="4057e-213">Panel Nueva configuración de distintivo en la herramienta Elementos</span><span class="sxs-lookup"><span data-stu-id="4057e-213">New Badge settings pane in the Elements tool</span></span>  

<span data-ttu-id="4057e-214">Ahora, usa la **configuración de distintivo en** la herramienta **Elementos** para activar \(o desactivar\) distintivos individuales.</span><span class="sxs-lookup"><span data-stu-id="4057e-214">Now, use the **Badge settings** in the **Elements** tool to turn on \(or off\) individual badges.</span></span>  <span data-ttu-id="4057e-215">Usa esta característica para personalizar y mantenerte centrado en distintivos importantes mientras inspeccionas páginas web.</span><span class="sxs-lookup"><span data-stu-id="4057e-215">Use this feature to customize and stay focused on important badges while you inspect webpages.</span></span>  <span data-ttu-id="4057e-216">Para mostrar el panel de configuración del distintivo en la parte superior de la **herramienta Elementos,** realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4057e-216">To display the badge settings pane at the top of the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="4057e-217">Mantenga el mouse sobre cualquier elemento.</span><span class="sxs-lookup"><span data-stu-id="4057e-217">Hover on any element.</span></span>  
1.  <span data-ttu-id="4057e-218">Abra el menú contextual \(haga clic con el botón derecho\).</span><span class="sxs-lookup"><span data-stu-id="4057e-218">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="4057e-219">Elija **Configuración de distintivo...**.</span><span class="sxs-lookup"><span data-stu-id="4057e-219">Choose **Badge settings...**.</span></span>  
    
<span data-ttu-id="4057e-220">Para mostrar \(u ocultar\) los distintivos, elija \(o quitar\) la casilla situada junto al nombre del distintivo.</span><span class="sxs-lookup"><span data-stu-id="4057e-220">To display \(or hide\) the badges, choose \(or remove\) the checkbox next to the badge name.</span></span>  

<!--  To review the history of this feature in the Chromium open-source project, navigate to Issue [1066772][CR1066772].  -->  

:::image type="complex" source="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png" alt-text="Panel de configuración de distintivo en la herramienta Elementos" lightbox="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png":::
   <span data-ttu-id="4057e-222">**Panel de configuración** de distintivo en la **herramienta** Elementos</span><span class="sxs-lookup"><span data-stu-id="4057e-222">**Badge settings** pane in the **Elements** tool</span></span>  
:::image-end:::  

### <a name="enhanced-image-preview-with-aspect-ratio-information"></a><span data-ttu-id="4057e-223">Vista previa de imagen mejorada con información de relación de aspecto</span><span class="sxs-lookup"><span data-stu-id="4057e-223">Enhanced image preview with aspect ratio information</span></span>  

<span data-ttu-id="4057e-224">Las vistas previas de imágenes en DevTools se han mejorado para mostrar más información, incluidos los siguientes detalles.</span><span class="sxs-lookup"><span data-stu-id="4057e-224">Image previews in the DevTools have been enhanced to display more information, including the following details.</span></span>  

*   <span data-ttu-id="4057e-225">Tamaño representado</span><span class="sxs-lookup"><span data-stu-id="4057e-225">Rendered size</span></span>  
*   <span data-ttu-id="4057e-226">Relación de aspecto representado</span><span class="sxs-lookup"><span data-stu-id="4057e-226">Rendered aspect ratio</span></span>  
*   <span data-ttu-id="4057e-227">Tamaño intrínseco</span><span class="sxs-lookup"><span data-stu-id="4057e-227">Intrinsic size</span></span>  
*   <span data-ttu-id="4057e-228">Relación de aspecto intrínseca</span><span class="sxs-lookup"><span data-stu-id="4057e-228">Intrinsic aspect ratio</span></span>  
*   <span data-ttu-id="4057e-229">Tamaño de archivo</span><span class="sxs-lookup"><span data-stu-id="4057e-229">File size</span></span>  
    
<span data-ttu-id="4057e-230">La información le ayuda a comprender mejor las imágenes y aplicar la optimización.</span><span class="sxs-lookup"><span data-stu-id="4057e-230">The  information helps you better understand your images and apply optimization.</span></span>  <span data-ttu-id="4057e-231">La información de relación de aspecto de imagen también está disponible en la **herramienta Red,** cuando se elige una vista previa de imagen.</span><span class="sxs-lookup"><span data-stu-id="4057e-231">The image aspect ratio information is also available in the **Network** tool, when you choose an image preview.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="4057e-232">En la **herramienta Elementos,** la vista previa de imagen ahora muestra más información sobre la imagen.</span><span class="sxs-lookup"><span data-stu-id="4057e-232">In the **Elements** tool, image preview now displays more information about the image.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4057e-233">Además, la información de relación de aspecto de imagen está disponible en la **herramienta Red,** al elegir una vista previa de imagen.</span><span class="sxs-lookup"><span data-stu-id="4057e-233">Also, the image aspect ratio information is available in the **Network** tool, when you choose an image preview.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png" alt-text="Vista previa de imagen con información de relación de aspecto en la herramienta Elemento" lightbox="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png":::
         <span data-ttu-id="4057e-235">Vista previa de imagen con información de relación de aspecto en la **herramienta** Elemento</span><span class="sxs-lookup"><span data-stu-id="4057e-235">Image preview with aspect ratio information in the **Element** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/network-img-name-filters-preview.msft.png" alt-text="Información de relación de aspecto de imagen en la herramienta Red" lightbox="../../media/2021/04/network-img-name-filters-preview.msft.png":::
         <span data-ttu-id="4057e-237">Información de relación de aspecto de imagen en la **herramienta Red**</span><span class="sxs-lookup"><span data-stu-id="4057e-237">Image aspect ratio information in the **Network** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="4057e-238">Para revisar el historial de esta característica en el proyecto de código abierto de Chromium, vaya a Problemas [1149832][CR1149832] y [1170656][CR1170656].</span><span class="sxs-lookup"><span data-stu-id="4057e-238">To review the history of this feature in the Chromium open-source project, navigate to Issues [1149832][CR1149832] and [1170656][CR1170656].</span></span>  

### <a name="new-options-to-configure-content-encodings-in-the-network-conditions-tool"></a><span data-ttu-id="4057e-239">Nuevas opciones para configurar codificaciones de contenido en la herramienta Condiciones de red</span><span class="sxs-lookup"><span data-stu-id="4057e-239">New options to configure Content-Encodings in the Network conditions tool</span></span> 

<span data-ttu-id="4057e-240">En la **herramienta Red,** elija el nuevo botón \*\*\*\* Más condiciones de **red...** junto al menú desplegable Limitación para abrir la **herramienta Condiciones de** red.</span><span class="sxs-lookup"><span data-stu-id="4057e-240">In the **Network** tool, choose the new **More network conditions...** button next to the **Throttling** dropdown menu to open the **Network conditions** tool.</span></span>  <span data-ttu-id="4057e-241">Para probar si las respuestas del servidor están codificadas correctamente para exploradores que no admiten [gzip][GnuSoftwareGzipManual], [brotli][|::ref1::|Main]u otro `Content-Encoding` futuro, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4057e-241">To test if server responses are correctly encoded for browsers that don't support [gzip][GnuSoftwareGzipManual], [brotli][|::ref1::|Main], or another future `Content-Encoding`, complete the following actions.</span></span>  

1.  <span data-ttu-id="4057e-242">Abrir la herramienta **Condiciones de** red</span><span class="sxs-lookup"><span data-stu-id="4057e-242">Open the **Network conditions** tool</span></span>
1.  <span data-ttu-id="4057e-243">Vaya a **Codificaciones de contenido aceptadas**.</span><span class="sxs-lookup"><span data-stu-id="4057e-243">Navigate to **Accepted Content-Encodings**.</span></span> 
1.  <span data-ttu-id="4057e-244">Quite la casilla situada junto a `Content-Encoding` la que desea probar.</span><span class="sxs-lookup"><span data-stu-id="4057e-244">Remove the checkbox next to the `Content-Encoding` you want to test.</span></span>  
    
<span data-ttu-id="4057e-245">Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya al problema [1162042][CR1162042].</span><span class="sxs-lookup"><span data-stu-id="4057e-245">To review the history of this feature in the Chromium open-source project, navigate to Issue [1162042][CR1162042].</span></span>  

:::image type="complex" source="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png" alt-text="Nuevas Más condiciones de red... botón abre la herramienta Condiciones de red para configurar Content-Encoding" lightbox="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png":::
   <span data-ttu-id="4057e-247">Nuevo **Botón Más condiciones de red...** abre la herramienta Condiciones **de** red para configurar</span><span class="sxs-lookup"><span data-stu-id="4057e-247">New **More network conditions...** button opens the **Network conditions** tool to configure</span></span> `Content-Encoding`  
:::image-end:::  

### <a name="styles-pane-enhancements"></a><span data-ttu-id="4057e-248">Mejoras en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="4057e-248">Styles pane enhancements</span></span>  

#### <a name="new-shortcut-to-display-computed-value-in-the-styles-pane"></a><span data-ttu-id="4057e-249">Nuevo acceso directo para mostrar el valor calculado en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="4057e-249">New shortcut to display computed value in the Styles pane</span></span>  

<span data-ttu-id="4057e-250">Ahora, para mostrar el valor CSS calculado en el panel **Estilos,** complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4057e-250">Now, to display the computed CSS value in the **Styles** pane, complete the following actions.</span></span>  

1.  <span data-ttu-id="4057e-251">Mantenga el mouse en una propiedad CSS.</span><span class="sxs-lookup"><span data-stu-id="4057e-251">Hover on a CSS property.</span></span>  
1.  <span data-ttu-id="4057e-252">Abra el menú contextual \(haga clic con el botón derecho\).</span><span class="sxs-lookup"><span data-stu-id="4057e-252">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="4057e-253">Elija **Ver valor calculado**.</span><span class="sxs-lookup"><span data-stu-id="4057e-253">Choose **View computed value**.</span></span>  
    
<span data-ttu-id="4057e-254">Para revisar el historial de esta característica en el proyecto de código abierto Chromium, vaya a Problema [1076198][CR1076198].</span><span class="sxs-lookup"><span data-stu-id="4057e-254">To review the history of this feature in the Chromium open-source project, navigate to Issue [1076198][CR1076198].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png" alt-text="Nuevo acceso directo para mostrar el valor calculado" lightbox="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png":::
   <span data-ttu-id="4057e-256">Nuevo acceso directo para mostrar el valor calculado</span><span class="sxs-lookup"><span data-stu-id="4057e-256">New shortcut to display computed value</span></span>  
:::image-end:::  

#### <a name="support-for-the-accent-color-keyword"></a><span data-ttu-id="4057e-257">Compatibilidad con la palabra clave accent-color</span><span class="sxs-lookup"><span data-stu-id="4057e-257">Support for the accent-color keyword</span></span>  

<span data-ttu-id="4057e-258">La interfaz de usuario de autocompletar del panel **Estilos** ahora detecta la palabra clave CSS, que te permite especificar el color de énfal para los controles de interfaz de usuario generados `accent-color` por el elemento.</span><span class="sxs-lookup"><span data-stu-id="4057e-258">The autocomplete UI of the **Styles** pane now detects the `accent-color` CSS keyword, which allows you to specify the accent color for UI controls generated by the element.</span></span>  <span data-ttu-id="4057e-259">Algunos ejemplos de controles de interfaz de usuario generados por un elemento incluyen casillas o botones de radio.</span><span class="sxs-lookup"><span data-stu-id="4057e-259">Examples of UI controls that are generated by an element include checkboxes or radio buttons.</span></span> <span data-ttu-id="4057e-260">Para obtener más información sobre el estado de la implementación Chromium, vaya a [Característica: propiedad CSS de color énfal][ChromestatusFeature4752739957473280].</span><span class="sxs-lookup"><span data-stu-id="4057e-260">For more information about the status of the Chromium implementation, navigate to [Feature: accent-color CSS property][ChromestatusFeature4752739957473280].</span></span>  <span data-ttu-id="4057e-261">Para activar esta característica, vaya a `edge://flags#enable-experimental-web-platform-features` y establezca la casilla en **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="4057e-261">To turn on this feature, navigate to `edge://flags#enable-experimental-web-platform-features` and set the checkbox to **Enabled**.</span></span>  <span data-ttu-id="4057e-262">Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya a Problema [1092093][CR1092093].</span><span class="sxs-lookup"><span data-stu-id="4057e-262">To review the history of this feature in the Chromium open-source project, navigate to Issue [1092093][CR1092093].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-accent-color.msft.png" alt-text="palabra clave CSS de color de acento" lightbox="../../media/2021/04/elements-styles-accent-color.msft.png":::
   `accent-color` <span data-ttu-id="4057e-264">Palabra clave CSS</span><span class="sxs-lookup"><span data-stu-id="4057e-264">CSS keyword</span></span>
:::image-end:::  

### <a name="display-details-about-blocked-features-in-the-frame-details-view"></a><span data-ttu-id="4057e-265">Mostrar detalles sobre las características bloqueadas en la vista Detalles del marco</span><span class="sxs-lookup"><span data-stu-id="4057e-265">Display details about blocked features in the Frame details view</span></span>  

<span data-ttu-id="4057e-266">La directiva de permisos es una API de plataforma web que ofrece a un sitio web la capacidad de permitir o bloquear el uso de características del explorador en un marco individual o en un que `iframe` inserta.</span><span class="sxs-lookup"><span data-stu-id="4057e-266">Permissions Policy is a web platform API that gives a website the ability to allow or block the use of browser features in an individual frame or in an `iframe` that it embeds.</span></span> <span data-ttu-id="4057e-267">Para obtener más información, vaya a [Permissions Policy Explainer][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd].</span><span class="sxs-lookup"><span data-stu-id="4057e-267">For more information, navigate to [Permissions Policy Explainer][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd].</span></span>  <span data-ttu-id="4057e-268">Para mostrar los detalles sobre por qué se bloquea una característica, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4057e-268">To display the details on why a feature is blocked, complete the following actions.</span></span>  

1.  <span data-ttu-id="4057e-269">Vaya a [OOPIF Permissions Policy][GlitchPermissionPolicyDemoMain].</span><span class="sxs-lookup"><span data-stu-id="4057e-269">Navigate to [OOPIF Permissions Policy][GlitchPermissionPolicyDemoMain].</span></span>  
1.  <span data-ttu-id="4057e-270">Vaya a la **herramienta Aplicación.**</span><span class="sxs-lookup"><span data-stu-id="4057e-270">Navigate to the **Application** tool.</span></span>  
1.  <span data-ttu-id="4057e-271">Elija un marco.</span><span class="sxs-lookup"><span data-stu-id="4057e-271">Choose a frame.</span></span>  
1.  <span data-ttu-id="4057e-272">Vaya a la **sección Directiva de permisos.**</span><span class="sxs-lookup"><span data-stu-id="4057e-272">Navigate to the **Permissions Policy** section.</span></span>  
1.  <span data-ttu-id="4057e-273">Vaya a la **propiedad Disabled Features.**</span><span class="sxs-lookup"><span data-stu-id="4057e-273">Navigate to the **Disabled Features** property.</span></span>  
1.  <span data-ttu-id="4057e-274">Elija **Mostrar detalles**.</span><span class="sxs-lookup"><span data-stu-id="4057e-274">Choose **Show details**.</span></span>  
1.  <span data-ttu-id="4057e-275">Elija el icono junto a cada directiva para navegar a la solicitud de red o `iframe` que bloqueó la característica.</span><span class="sxs-lookup"><span data-stu-id="4057e-275">Choose the icon next to each policy to navigate to the `iframe` or network request that blocked the feature.</span></span>  
    
<span data-ttu-id="4057e-276">Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya al problema [1158827][CR1158827].</span><span class="sxs-lookup"><span data-stu-id="4057e-276">To review the history of this feature in the Chromium open-source project, navigate to Issue [1158827][CR1158827].</span></span>  

:::image type="complex" source="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png" alt-text="Características bloqueadas en la vista Detalles del marco" lightbox="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png":::
   <span data-ttu-id="4057e-278">Características bloqueadas en la vista Detalles del marco</span><span class="sxs-lookup"><span data-stu-id="4057e-278">Blocked features in the Frame details view</span></span>  
:::image-end:::  

### <a name="filter-experiments-in-the-experiments-setting"></a><span data-ttu-id="4057e-279">Filtrar experimentos en la configuración Experimentos</span><span class="sxs-lookup"><span data-stu-id="4057e-279">Filter experiments in the Experiments setting</span></span>  

<span data-ttu-id="4057e-280">Busca experimentos más rápido con el nuevo filtro de experimento.</span><span class="sxs-lookup"><span data-stu-id="4057e-280">Find experiments quicker with the new experiment filter.</span></span>  <span data-ttu-id="4057e-281">Por ejemplo, para activar nuevos experimentos para problemas de código, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4057e-281">For example, to turn on new experiments for code issues, complete the following actions.</span></span>
``

1.  <span data-ttu-id="4057e-282">Vaya a **Configuración**  >  **Experiments**.</span><span class="sxs-lookup"><span data-stu-id="4057e-282">Navigate to **Settings** > **Experiments**.</span></span>  
1.  <span data-ttu-id="4057e-283">Vaya al **cuadro de texto** Filtrar.</span><span class="sxs-lookup"><span data-stu-id="4057e-283">Navigate to the **Filter** textbox.</span></span>  
1.  <span data-ttu-id="4057e-284">Escriba `issues`.</span><span class="sxs-lookup"><span data-stu-id="4057e-284">Type `issues`.</span></span>  
    
:::image type="complex" source="../../media/2021/04/settings-experiments-filter-by-issues.msft.png" alt-text="Filtrar experimentos en la configuración Experimentos" lightbox="../../media/2021/04/settings-experiments-filter-by-issues.msft.png":::
   <span data-ttu-id="4057e-286">Filtrar experimentos en la **configuración Experimentos**</span><span class="sxs-lookup"><span data-stu-id="4057e-286">Filter experiments in the **Experiments** setting</span></span>  
:::image-end:::  

### <a name="new-vary-header-column-in-the-cache-storage-pane"></a><span data-ttu-id="4057e-287">Nueva columna De encabezado Vary en el panel Almacenamiento en caché</span><span class="sxs-lookup"><span data-stu-id="4057e-287">New Vary Header column in the Cache storage pane</span></span>  

<span data-ttu-id="4057e-288">Use la nueva `Vary Header` columna en el panel De **Storage** caché para mostrar los valores de encabezado [de][HttpwgSpecsRfc7231HtmlHeaderVary] respuesta HTTP Variables.</span><span class="sxs-lookup"><span data-stu-id="4057e-288">Use the new `Vary Header` column in the **Cache Storage** pane to display the [Vary][HttpwgSpecsRfc7231HtmlHeaderVary] HTTP response header values.</span></span>  <span data-ttu-id="4057e-289">Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya al problema [1186049][CR1186049].</span><span class="sxs-lookup"><span data-stu-id="4057e-289">To review the history of this feature in the Chromium open-source project, navigate to Issue [1186049][CR1186049].</span></span>  

:::image type="complex" source="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png" alt-text="Variar columna de encabezado" lightbox="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png":::
   <span data-ttu-id="4057e-291">Variar columna de encabezado</span><span class="sxs-lookup"><span data-stu-id="4057e-291">Vary Header column</span></span>  
:::image-end:::  

### <a name="sources-tool-improvements"></a><span data-ttu-id="4057e-292">Mejoras de herramientas de orígenes</span><span class="sxs-lookup"><span data-stu-id="4057e-292">Sources tool improvements</span></span>  

#### <a name="support-for-new-javascript-features"></a><span data-ttu-id="4057e-293">Compatibilidad con nuevas características de JavaScript</span><span class="sxs-lookup"><span data-stu-id="4057e-293">Support for new JavaScript features</span></span>  

<span data-ttu-id="4057e-294">DevTools ahora admite las nuevas comprobaciones de marca privada [a.k.a.][V8DevFeaturesPrivateBrandChecks] #foo en la característica de lenguaje JavaScript de obj.</span><span class="sxs-lookup"><span data-stu-id="4057e-294">DevTools now support the new [Private brand checks a.k.a. #foo in obj][V8DevFeaturesPrivateBrandChecks] JavaScript language feature.</span></span>  <span data-ttu-id="4057e-295">La característica de comprobaciones de marca privada amplía el [operador in][MdnDocsWebJavascriptReferenceOperatorsIn] para admitir campos de clase [Private][V8DevFeaturesClassFieldsPrivateClassFields] en un objeto específico.</span><span class="sxs-lookup"><span data-stu-id="4057e-295">The private brand checks feature extends the [in operator][MdnDocsWebJavascriptReferenceOperatorsIn] to support [Private class fields][V8DevFeaturesClassFieldsPrivateClassFields] on a specific object.</span></span>  <span data-ttu-id="4057e-296">Pruébalo en las **herramientas Consola** **y** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="4057e-296">Try it in the **Console** and **Sources** tools.</span></span>  <span data-ttu-id="4057e-297">Además, para inspeccionar los campos privados, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4057e-297">Also, to inspect the private fields, complete the following actions.</span></span>  

1.  <span data-ttu-id="4057e-298">Vaya al **panel del** depurador.</span><span class="sxs-lookup"><span data-stu-id="4057e-298">Navigate to **debugger** pane.</span></span>  
1.  <span data-ttu-id="4057e-299">Vaya a la **sección Ámbito.**</span><span class="sxs-lookup"><span data-stu-id="4057e-299">Navigate to the **Scope** section.</span></span>  
    
<span data-ttu-id="4057e-300">Para revisar el historial de esta característica en el Chromium de código abierto, vaya al problema [11374][CR11374].</span><span class="sxs-lookup"><span data-stu-id="4057e-300">To review the history of this feature in the Chromium open-source project, navigate to Issue [11374][CR11374].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png" alt-text="Comprobaciones de marca privada de JavaScript" lightbox="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png":::
   <span data-ttu-id="4057e-302">Comprobaciones de marca privada de JavaScript</span><span class="sxs-lookup"><span data-stu-id="4057e-302">JavaScript private brand checks</span></span>  
:::image-end:::  

#### <a name="enhanced-support-for-breakpoints-debugging"></a><span data-ttu-id="4057e-303">Compatibilidad mejorada para la depuración de puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="4057e-303">Enhanced support for breakpoints debugging</span></span>  

<span data-ttu-id="4057e-304">Los agrupadores modernos de JavaScript como [Webpack][WebpackJsMain]y [Rollup][RollupjsMain] admiten la división de código.</span><span class="sxs-lookup"><span data-stu-id="4057e-304">Modern JavaScript bundlers like [Webpack][WebpackJsMain], and [Rollup][RollupjsMain] support code splitting.</span></span>  <span data-ttu-id="4057e-305">Para obtener más información sobre la división de código, vaya [a División de código][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules].</span><span class="sxs-lookup"><span data-stu-id="4057e-305">To learn more about code splitting, navigate to [Code splitting][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules].</span></span>  <span data-ttu-id="4057e-306">En Microsoft Edge versión 90 o anterior, DevTools solo establece puntos de interrupción en un único lote.</span><span class="sxs-lookup"><span data-stu-id="4057e-306">In Microsoft Edge version 90 or earlier, DevTools only set breakpoints in a single bundle.</span></span>  <span data-ttu-id="4057e-307">En Microsoft Edge versión 91 o posterior, DevTools establece correctamente los puntos de interrupción en varios lotes al depurar un componente compartido.</span><span class="sxs-lookup"><span data-stu-id="4057e-307">In Microsoft Edge version 91 or later, DevTools properly sets breakpoints in multiple bundles when you debug a shared component.</span></span>  <span data-ttu-id="4057e-308">Para revisar el historial de esta característica en el proyecto de código abierto de Chromium, vaya a Problemas [1142705][CR1142705], [979000][CR979000]y [1180794][CR1180794].</span><span class="sxs-lookup"><span data-stu-id="4057e-308">To review the history of this feature in the Chromium open-source project, navigate to Issues [1142705][CR1142705], [979000][CR979000], and [1180794][CR1180794].</span></span>  

#### <a name="support-hover-preview-with-bracket-notation"></a><span data-ttu-id="4057e-309">Compatibilidad con la vista previa activa con la notación entre corchetes</span><span class="sxs-lookup"><span data-stu-id="4057e-309">Support hover preview with bracket notation</span></span>  

<span data-ttu-id="4057e-310">DevTools ahora admite la vista previa activa en expresiones de miembros de JavaScript que usan `[]` la notación en la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="4057e-310">DevTools now support hover preview on JavaScript member expressions that use the `[]` notation in the **Sources** tool.</span></span>  <span data-ttu-id="4057e-311">Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya al problema [1178305][CR1178305].</span><span class="sxs-lookup"><span data-stu-id="4057e-311">To review the history of this feature in the Chromium open-source project, navigate to Issue [1178305][CR1178305].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png" alt-text="Compatibilidad con la vista previa activa con notación []" lightbox="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png":::
   <span data-ttu-id="4057e-313">Compatibilidad con la vista previa activa con `[]` la notación</span><span class="sxs-lookup"><span data-stu-id="4057e-313">Support hover preview with `[]` notation</span></span>  
:::image-end:::  

#### <a name="improved-outline-of-html-files"></a><span data-ttu-id="4057e-314">Esquema mejorado de archivos HTML</span><span class="sxs-lookup"><span data-stu-id="4057e-314">Improved outline of HTML files</span></span>  

<span data-ttu-id="4057e-315">DevTools ahora tiene mejor compatibilidad de esquema para `.html` los archivos.</span><span class="sxs-lookup"><span data-stu-id="4057e-315">DevTools now has better outline support for `.html` files.</span></span>  <span data-ttu-id="4057e-316">En la **herramienta Orígenes,** abra el `.html` archivo.</span><span class="sxs-lookup"><span data-stu-id="4057e-316">In the **Sources** tool, open the `.html` file.</span></span>  <span data-ttu-id="4057e-317">Para activar \(o desactivar\) el esquema de código, seleccione en `Ctrl` + `Shift` + `O` Windows/Linux o `Cmd` + `Shift` + `O` en macOS.</span><span class="sxs-lookup"><span data-stu-id="4057e-317">To turn on \(or off\) the code outline, select `Ctrl`+`Shift`+`O` on Windows/Linux or `Cmd`+`Shift`+`O` on macOS.</span></span>  <span data-ttu-id="4057e-318">En la siguiente figura, DevTools ahora enumera correctamente todas las funciones del esquema.</span><span class="sxs-lookup"><span data-stu-id="4057e-318">In the following figure, DevTools now correctly list all functions in the outline.</span></span>  <span data-ttu-id="4057e-319">Anteriormente, DevTools solo muestra algunas de las funciones.</span><span class="sxs-lookup"><span data-stu-id="4057e-319">Previously, DevTools only displayed some of the functions.</span></span>  <span data-ttu-id="4057e-320">Para revisar el historial de esta característica en el proyecto de código abierto de Chromium, vaya a Los problemas [761019][CR761019] y [1191465][CR1191465].</span><span class="sxs-lookup"><span data-stu-id="4057e-320">To review the history of this feature in the Chromium open-source project, navigate to Issues [761019][CR761019] and [1191465][CR1191465].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-jobobbx-at.msft.png" alt-text=" Esquema mejorado de archivos HTML" lightbox="../../media/2021/04/sources-page-jobobbx-at.msft.png":::
   <span data-ttu-id="4057e-322">Esquema mejorado de archivos HTML</span><span class="sxs-lookup"><span data-stu-id="4057e-322">Improved outline of HTML files</span></span>  
:::image-end:::  

#### <a name="proper-error-stack-traces-for-wasm-debugging"></a><span data-ttu-id="4057e-323">Seguimientos de pila de errores adecuados para la depuración de Wasm</span><span class="sxs-lookup"><span data-stu-id="4057e-323">Proper error stack traces for Wasm debugging</span></span>  

<span data-ttu-id="4057e-324">En Microsoft Edge versión 90 o anterior, DevTools solo muestra referencias wasm genéricas en seguimientos de pila de errores.</span><span class="sxs-lookup"><span data-stu-id="4057e-324">In Microsoft Edge version 90 or earlier, DevTools only displayed generic Wasm references in Error stack traces.</span></span>  <span data-ttu-id="4057e-325">En Microsoft Edge versión 91 o posterior, DevTools resuelve las solicitudes de función en línea y muestra la ubicación de origen en Seguimientos de pila de errores para la depuración de Wasm.</span><span class="sxs-lookup"><span data-stu-id="4057e-325">In Microsoft Edge version 91 or later, DevTools resolves inline function requests and displays the source location in Error stack traces for Wasm debugging.</span></span>  <span data-ttu-id="4057e-326">Para obtener más información sobre los seguimientos de pila de errores en **la consola,** vaya a [error][DevtoolsConsoleApiError].</span><span class="sxs-lookup"><span data-stu-id="4057e-326">To learn more about Error stack traces in the **Console**, navigate to [error][DevtoolsConsoleApiError].</span></span>  

<span data-ttu-id="4057e-327">En Microsoft Edge versión 91 o posterior, DevTools resuelve las solicitudes de función en línea y muestra los seguimientos de pila de errores adecuados para la depuración de Wasm.</span><span class="sxs-lookup"><span data-stu-id="4057e-327">In Microsoft Edge version 91 or later, DevTools resolves inline function requests and displays proper error stack traces for Wasm debugging.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="4057e-328">En Microsoft Edge versión 90 y versiones anteriores, la ubicación de origen no se muestra en los seguimientos de la pila de errores.</span><span class="sxs-lookup"><span data-stu-id="4057e-328">In Microsoft Edge version 90 and earlier, the source location doesn't display in the Error stack traces.</span></span>  <span data-ttu-id="4057e-329">Las ubicaciones de origen incluyen `dsquare` .</span><span class="sxs-lookup"><span data-stu-id="4057e-329">Source locations include `dsquare`.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4057e-330">En Microsoft Edge versión 91 y posteriores, la ubicación de origen se muestra en los seguimientos de la pila de errores.</span><span class="sxs-lookup"><span data-stu-id="4057e-330">In Microsoft Edge version 91 and later, the source location displays in the Error stack traces.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png" alt-text="Seguimientos de pila de errores anteriores para la depuración de Wasm" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png":::
         <span data-ttu-id="4057e-332">Seguimientos de pila de errores adecuados para la depuración de Wasm</span><span class="sxs-lookup"><span data-stu-id="4057e-332">Proper error stack traces for Wasm debugging</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png" alt-text="Seguimientos de pila de errores adecuados para la depuración de Wasm" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png":::
         <span data-ttu-id="4057e-334">Seguimientos de pila de errores adecuados para la depuración de Wasm</span><span class="sxs-lookup"><span data-stu-id="4057e-334">Proper error stack traces for Wasm debugging</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="4057e-335">Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya a Problema [1189161][CR1189161].</span><span class="sxs-lookup"><span data-stu-id="4057e-335">To review the history of this feature in the Chromium open-source project, navigate to Issue [1189161][CR1189161].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="4057e-336">Descargar los canales de vista previa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4057e-336">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="4057e-337">Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4057e-337">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="4057e-338">Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4057e-338">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="4057e-339">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4057e-339">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Uso de DevTools en otros idiomas: novedades de DevTools (Microsoft Edge 81) | Microsoft Docs"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Novedades de DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: ../../2020/11/devtools.md#css-variable-definitions-in-styles-pane "Definiciones de variables CSS en el panel Estilos: novedades de DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Novedades de DevTools (Microsoft Edge 90) | Microsoft Docs"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Agrupar herramientas en modo de enfoque: novedades de DevTools (Microsoft Edge 90) | Microsoft Docs"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: ../../../command-menu/index.md#open-the-command-menu "Abra el menú Comando: ejecute comandos con el Microsoft Edge menú DevTools Command | Microsoft Docs"  
[DevtoolsConsoleApiError]: ../../../console/api.md#error "error: referencia de api de consola | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: ../../../customize/localization.md "Cambiar la configuración de idioma de DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsServiceWorkerIndex]: ../../../service-workers/index.md "Mejoras de service worker | Microsoft Docs"  
[DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]: ../../../sources/index.md#using-the-debugger-pane-to-debug-javascript-code "Uso del panel Depurador para depurar código JavaScript: información general sobre la herramienta Orígenes | Microsoft Docs"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: ../../../../progressive-web-apps-chromium/serviceworker.md#the-service-worker-lifecycle "Ciclo de vida del trabajador de servicio: usar los trabajadores de servicio para administrar las solicitudes de red y las notificaciones de inserción | Microsoft Docs"  
[ProgressiveWebAppsWebappmanifests]: ../../../../progressive-web-apps-chromium/webappmanifests.md "Usa el manifiesto de aplicación web para integrar la aplicación web progresiva en el sistema operativo | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Marketplace de extensiones | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  

[BrotliMain]: https://www.brotli.org "Brotli"  

[ChromestatusFeature4752739957473280]: https://chromestatus.com/feature/4752739957473280 "Característica: propiedad CSS de color de énf | Estado de la plataforma Chrome"  

[CsswgDraftsCssUi4WidgetAccent]: https://drafts.csswg.org/css-ui-4/#widget-accent "Widget Accent Colors: la propiedad accent-color - Css Basic User Interface Module Level 4 | Borradores del editor de grupo de trabajo css"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  
[CR11374]: https://crbug.com/v8/11374 "Problema 11374: Implementar la comprobación de marca ergonómica para campos privados"  
[CR761019]: https://crbug.com/761019 "Problema 761019: &quot;Ir a símbolo&quot; pierde la primera función y prefiere una coincidencia peor si contiene todas las chars con tipo"  
[CR862450]: https://crbug.com/862450 "Problema 862450: [css-scroll-snap] Considere la posibilidad de agregar la característica Devtools para el complemento de desplazamiento css"  
[CR979000]: https://crbug.com/979000 "Problema 979000: Los mapas de origen con rutas de acceso de orígenes en colisión no funcionan."  
[CR1066604]: https://crbug.com/1066604 "Problema 1066604: DevTools: Vea detalles sobre ServiceWorker para instalar y activar eventos | Chromium errores"  
<!--  [CR1066772]: https://crbug.com/1066772 "Issue 1066772: "  locked  -->  
[CR1076198]: https://crbug.com/1076198 "Problema 1076198: [Solicitud de característica] Saltar a la propiedad calculada desde la `styles` pestaña"  
[CR1092093]: "Problema 1092093: Hacer que los controles de formularios se atenúan más al color al admitir la propiedad https://crbug.com/1092093 CSS 'accent-color'"  
[CR1136655]: https://crbug.com/1136655 "Problema 1136655: Devtools: Localización V2 | Chromium errores"  
[CR1142705]: "Problema 1142705: los puntos de interrupción dejan de funcionar cuando 2 mapas de origen apuntan al mismo archivo virtual al usar https://crbug.com/1142705 webpack"  
[CR1149832]: "Problema 1149832: Solicitud de característica: la vista previa de imagen también debe mostrar https://crbug.com/1149832 el tamaño del archivo"  
[CR1158827]: https://crbug.com/1158827 "Problema 1158827: [Directiva de permisos] Implementar la compatibilidad de devtool para la directiva de permisos"  
[CR1162042]: https://crbug.com/1162042 "Problema 1162042: DevTools: admite la deshabilitación de gzip/brotli/jxl content-encoding"  
[CR1166577]: https://crbug.com/1166577 "Problema 1166577: ☂️ inspector de memoria lineal 1.0"  
[CR1170656]: https://crbug.com/1170656 "Problema 1170656: Mostrar relación intrínseca de aspecto"  
[CR1178305]: "Problema 1178305: El depurador no muestra el valor de propiedad de un elemento indizado cuando está https://crbug.com/1178305 activa"  
[CR1180794]: "Problema 1180794: Los puntos de interrupción no funcionan con optimización de la línea del compilador https://crbug.com/1180794 de cierre"  
[CR1185945]: "Problema 1185945: La advertencia de manifiesto implica que todos los iconos deben ser cuadrados https://crbug.com/1185945 | Chromium errores"  
[CR1186049]: https://crbug.com/1186049 "Problema 1186049: Column for Vary: header in Cache Storage viewer"  
[CR1187735]: https://crbug.com/1187735 "Issue 1187735: Accessibility: MAS2.1.1: Keyboard: Unable to invoke the 'Var(..)' function using keyboard | Chromium errores"  
[CR1189161]: https://crbug.com/1189161 "Problema 1189161: los stacktraces no se `new Error` transforman a través de ENANO"  
[CR1191465]: https://crbug.com/1191465 "Problema 1191465: Ctrl+Mayús+O roto en HTML"  

[GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explicador de directivas de permisos | GitHub"  

[GlitchMemoryInspectorDemoJsHtml]: https://memory-inspector.glitch.me/demo-js.html "Memoria en JS | Glitch"  
[GlitchMemoryInspectorDemoWasmHtml]: https://memory-inspector.glitch.me/demo-wasm.html "Memoria en Wasm | Glitch"  

[GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml]: https://microsoft-edge-chromium-devtools.glitch.me/css-dbg-stories/css-scroll-snap.html "Desplácese Acoplar de demostración | Glitch"  

[GlitchPermissionPolicyDemoMain]: http://permission-policy-demo.glitch.me "Directiva de permisos de OOPIF | Glitch"  

[GnuSoftwareGzipManual]: https://www.gnu.org/software/gzip/manual "gzip: el programa de compresión de datos | Sistema operativo GNU"  

[HttpwgSpecsRfc7231HtmlHeaderVary]: https://httpwg.org/specs/rfc7231.html#header.vary "Vary: protocolo de transferencia de hipertexto (HTTP/1.1): semántica y contenido | Grupo de trabajo HTTP de IETF"  

[JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]: https://webpack.js.org/guides/code-splitting/#:~:text=There%20are%20three%20general%20approaches%20to%20code%20splitting,Split%20code%20via%20inline%20function%20calls%20within%20modules. "Hay tres enfoques generales para la división de código disponibles: Puntos de entrada: Código dividido manualmente mediante la configuración de entrada.  Impedir duplicación: use dependencias de entrada o SplitChunksPlugin para desduplicar y dividir fragmentos.  Importaciones dinámicas: divida el código mediante llamadas de función en línea dentro de los módulos. - División de código | webpack"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propiedades personalizadas de CSS (variables) | MDN"  

[MdnDocsWebJavascriptReferenceOperatorsIn]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/in "en operador | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Generador de imágenes | PWABuilder"  

[RollupjsMain]: https://rollupjs.org "rollup.js"  

[V8DevFeaturesPrivateBrandChecks]: https://v8.dev/features/private-brand-checks "Marca privada comprueba a.k.a. #foo en obj | V8"  
[V8DevFeaturesClassFieldsPrivateClassFields]: https://v8.dev/features/class-fields#private-class-fields "Campos de clase privada: campos de clase pública y privada | V8"  

[WebpackJsMain]: https://webpack.js.org "webpack"  

> [!NOTE]
> <span data-ttu-id="4057e-398">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4057e-398">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4057e-399">La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-91) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="4057e-399">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-91) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4057e-401">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4057e-401">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  

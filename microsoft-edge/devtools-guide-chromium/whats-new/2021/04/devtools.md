---
description: Wavy subraya los problemas de código destacado en la herramienta Elementos, escala de tiempo de actualización del trabajador de servicio y mucho más.
title: Novedades de DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 3a2be4d309432de4421af73ca7b4d21734ad5221
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514489"
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
# <a name="whats-new-in-devtools-microsoft-edge-91"></a><span data-ttu-id="93df8-104">Novedades de DevTools (Microsoft Edge 91)</span><span class="sxs-lookup"><span data-stu-id="93df8-104">What's New In DevTools (Microsoft Edge 91)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a><span data-ttu-id="93df8-105">Wavy subraya los problemas de código destacado y las mejoras en la herramienta Elementos</span><span class="sxs-lookup"><span data-stu-id="93df8-105">Wavy underlines highlight code issues and improvements in Elements tool</span></span>  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

<span data-ttu-id="93df8-106">En la mayoría de los identificadores modernos, los subrayados ondulados debajo del texto indican errores de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="93df8-106">In most modern IDEs, wavy underlines under text indicate syntax errors.</span></span>   <span data-ttu-id="93df8-107">En Microsoft Edge versión 91 o posterior, los subrayados ondulados se muestran en HTML en la vista **DOM** de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="93df8-107">In Microsoft Edge version 91 or later, wavy underlines display under HTML in the **DOM** view of the **Elements** tool.</span></span>  <span data-ttu-id="93df8-108">Los subrayados ondulados indican problemas de código y sugerencias relacionadas con la accesibilidad, la compatibilidad, el rendimiento, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="93df8-108">The wavy underlines indicate code issues and suggestions related to accessibility, compatibility, performance, and so on.</span></span>  <span data-ttu-id="93df8-109">Para obtener más información acerca de cómo revisar y editar problemas, vaya a Buscar y corregir problemas con la herramienta [Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="93df8-109">For more information about how to review and edit issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

<span data-ttu-id="93df8-110">Para abrir la **herramienta Problemas** y obtener más información sobre el problema y cómo solucionarlo, complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="93df8-110">To open the **Issues** tool and learn more about the issue and how to fix it, complete one of the following actions.</span></span>  

*   <span data-ttu-id="93df8-111">Seleccione y mantenga presionado y, a `Shift` continuación, elija cualquier subrayado ondulado.</span><span class="sxs-lookup"><span data-stu-id="93df8-111">Select and hold `Shift`, and then choose any wavy underline.</span></span>  
*   <span data-ttu-id="93df8-112">Complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="93df8-112">Complete the following actions.</span></span>  
    1.  <span data-ttu-id="93df8-113">Mantenga el mouse sobre cualquier subrayado ondulado.</span><span class="sxs-lookup"><span data-stu-id="93df8-113">Hover on any wavy underline.</span></span>  
    1.  <span data-ttu-id="93df8-114">Abra el menú contextual \(haga clic con el botón derecho\).</span><span class="sxs-lookup"><span data-stu-id="93df8-114">Open the contextual menu \(right-click\).</span></span>  
    1.  <span data-ttu-id="93df8-115">Elija **Mostrar en Problemas**.</span><span class="sxs-lookup"><span data-stu-id="93df8-115">Choose **Show in Issues**.</span></span>  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Elija el error subrayado en la herramienta Elementos" lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         <span data-ttu-id="93df8-117">Elija el error subrayado en la **herramienta** Elementos</span><span class="sxs-lookup"><span data-stu-id="93df8-117">Choose the underlined error in the **Elements** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Mostrar detalles de error en la herramienta Problemas" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         <span data-ttu-id="93df8-119">Mostrar detalles de error en la **herramienta Problemas**</span><span class="sxs-lookup"><span data-stu-id="93df8-119">Display error details in the **Issues** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="93df8-120">Aprenda más sobre DevTools con la información sobre herramientas informativas</span><span class="sxs-lookup"><span data-stu-id="93df8-120">Learn about DevTools with informative tooltips</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

<span data-ttu-id="93df8-121">La característica DevTools Tooltips le ayuda a obtener información sobre todas las diferentes herramientas y paneles de DevTools.</span><span class="sxs-lookup"><span data-stu-id="93df8-121">The DevTools Tooltips feature helps you learn about all the different tools and panes in DevTools.</span></span>  <span data-ttu-id="93df8-122">Para desactivar la información sobre herramientas, seleccione `Esc` .</span><span class="sxs-lookup"><span data-stu-id="93df8-122">To turn off Tooltips, select `Esc`.</span></span>  <span data-ttu-id="93df8-123">Para activar información sobre herramientas, complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="93df8-123">To turn on Tooltips, complete one of the following actions.</span></span>  

*   <span data-ttu-id="93df8-124">Seleccione `Ctrl` + `Shift` + `H` \(Windows/Linux\) o `Cmd` + `Shift` + `H` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="93df8-124">Select `Ctrl`+`Shift`+`H` \(Windows/Linux\) or `Cmd`+`Shift`+`H` \(macOS\).</span></span>  
*   <span data-ttu-id="93df8-125">[Abra el menú comando y,][DevtoolsCommandMenuIndexOpenCommandMenu] a continuación, escriba `tooltips` .</span><span class="sxs-lookup"><span data-stu-id="93df8-125">[Open the Command Menu][DevtoolsCommandMenuIndexOpenCommandMenu] and then type `tooltips`.</span></span>  
*   <span data-ttu-id="93df8-126">Elija **Personalizar y controlar DevTools** \( \) > Ayuda para alternar la información sobre herramientas de `...` \*\*\*\*  >  **DevTools**.</span><span class="sxs-lookup"><span data-stu-id="93df8-126">Choose **Customize and control DevTools** \(`...`\) > **Help** > **Toggle the DevTools Tooltips**.</span></span>  

<span data-ttu-id="93df8-127">Además, si activa el experimento Modo de enfoque y Información sobre herramientas [de DevTools,][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] también puede elegir el botón Alternar la información sobre herramientas **de DevTools** \( \) en la parte inferior de la barra de `?` **actividades**.</span><span class="sxs-lookup"><span data-stu-id="93df8-127">Also, if you turn on the [Focus Mode and DevTools Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] experiment, you may also choose the **Toggle the DevTools Tooltips** \(`?`\) button at the bottom of the **Activity Bar**.</span></span>  

<span data-ttu-id="93df8-128">Para mostrar más información sobre cómo usar DevTools, active Información sobre herramientas y, a continuación, mantenga el mouse en cada región de esquema de DevTools.</span><span class="sxs-lookup"><span data-stu-id="93df8-128">To display more information about how to use the DevTools, turn on Tooltips, and then hover on each outlined region of the DevTools.</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Mantenga el mouse en cualquier lugar de la región resaltada de la herramienta Problemas para mostrar más detalles" lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   <span data-ttu-id="93df8-130">Mantenga el mouse en cualquier lugar de la región resaltada de la **herramienta Problemas** para mostrar más detalles</span><span class="sxs-lookup"><span data-stu-id="93df8-130">Hover on anywhere in the highlighted region of the **Issues** tool to display more details</span></span>  
:::image-end:::  

## <a name="service-worker-update-timeline"></a><span data-ttu-id="93df8-131">Escala de tiempo de actualización del trabajador de servicio</span><span class="sxs-lookup"><span data-stu-id="93df8-131">Service worker update timeline</span></span>  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

<span data-ttu-id="93df8-132">En Microsoft Edge versión 91 o posterior, si es un desarrollador de aplicación web progresiva o trabajador de servicio, puede mostrar el ciclo de vida de actualización de los trabajadores de servicio como una escala de tiempo en la herramienta **Aplicación.**</span><span class="sxs-lookup"><span data-stu-id="93df8-132">In Microsoft Edge version 91 or later, if you are a Progressive Web App or Service Worker developer, you may display the update lifecycle of your Service Workers as a timeline in the **Application** tool.</span></span>  <span data-ttu-id="93df8-133">Esta característica le ayuda a comprender el tiempo que el trabajador de servicio pasa en cada una de las siguientes fases.</span><span class="sxs-lookup"><span data-stu-id="93df8-133">This feature helps you understand the time your Service Worker spends in each of the following stages.</span></span>  

*   **<span data-ttu-id="93df8-134">Instalar</span><span class="sxs-lookup"><span data-stu-id="93df8-134">Install</span></span>**  
*   **<span data-ttu-id="93df8-135">Esperar</span><span class="sxs-lookup"><span data-stu-id="93df8-135">Wait</span></span>**  
*   **<span data-ttu-id="93df8-136">Activar</span><span class="sxs-lookup"><span data-stu-id="93df8-136">Activate</span></span>**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Revisar la escala de tiempo del ciclo de actualización para el trabajador de servicio" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   <span data-ttu-id="93df8-138">Revisar la **escala de** tiempo del ciclo **de actualización** para el trabajador de servicio</span><span class="sxs-lookup"><span data-stu-id="93df8-138">Review the **Timeline** in the **Update Cycle** for your Service Worker</span></span>  
:::image-end:::  

<span data-ttu-id="93df8-139">Para obtener más información sobre el ciclo de vida de los trabajadores de servicio, vaya a [El ciclo de vida del trabajador de servicio][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span><span class="sxs-lookup"><span data-stu-id="93df8-139">For more information about the lifecycle of your Service Workers, navigate to [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span></span>  <span data-ttu-id="93df8-140">Para obtener más información acerca de las herramientas de depuración para las aplicaciones web progresivas y los trabajadores de servicio en DevTools, vaya a [Mejoras del trabajador de servicio][DevtoolsServiceWorkerIndex].</span><span class="sxs-lookup"><span data-stu-id="93df8-140">For more information about debugging tools for Progressive Web Apps and Service Workers in the DevTools, navigate to [Service Worker improvements][DevtoolsServiceWorkerIndex].</span></span>  <span data-ttu-id="93df8-141">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto Chromium, vaya al problema [1066604][CR1066604].</span><span class="sxs-lookup"><span data-stu-id="93df8-141">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1066604][CR1066604].</span></span>  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a><span data-ttu-id="93df8-142">Las aplicaciones web progresivas ya no muestran advertencias para iconos que no son cuadrados</span><span class="sxs-lookup"><span data-stu-id="93df8-142">Progressive Web Apps no longer display warnings for non-square icons</span></span>  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

<span data-ttu-id="93df8-143">En Microsoft Edge versión [90][DevtoolsWhatsNew202102Devtools] o anterior, si incluyó un icono que no \*\*\*\* es cuadrado \*\*\*\* en el Manifiesto de aplicación web de su PWA, la sección Manifiesto de la herramienta Aplicación muestra una advertencia en Errores y **advertencias** para cada icono que no sea cuadrado.</span><span class="sxs-lookup"><span data-stu-id="93df8-143">In [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] or earlier, if you included a non-square icon in the Web App Manifest of your PWA, the **Manifest** section in the **Application** tool displayed a warning under **Errors and Warnings** for each non-square icon.</span></span>  <span data-ttu-id="93df8-144">En Microsoft Edge versión 91 \*\*\*\* o posterior, la sección Manifiesto de la herramienta Aplicación no muestra advertencias si proporciona al menos un icono cuadrado. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93df8-144">In Microsoft Edge version 91 or later, the **Manifest** section in the **Application** tool displays no warnings if you provide at least one square icon.</span></span>  <span data-ttu-id="93df8-145">Si no proporciona ningún icono cuadrado, una advertencia muestra el siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="93df8-145">If you don't provide any square icons, a warning displays the following message.</span></span>  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="En Microsoft Edge versión 90 o anterior, se muestra un error para cada icono que no es cuadrado" lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="93df8-147">En Microsoft Edge versión 90 o anterior, se muestra un error para cada icono que no es cuadrado</span><span class="sxs-lookup"><span data-stu-id="93df8-147">In Microsoft Edge version 90 or earlier, an error displays for each icon that is non-square</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="En Microsoft Edge versión 91 o posterior, no se muestra ningún error cuando se proporciona al menos un icono cuadrado" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="93df8-149">En Microsoft Edge versión 91 o posterior, no se muestra ningún error cuando se proporciona al menos un icono cuadrado</span><span class="sxs-lookup"><span data-stu-id="93df8-149">In Microsoft Edge version 91 or later, no error displays when you provide at least one square icon</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="93df8-150">Para revisar errores y advertencias en el manifiesto de la aplicación web, vaya a la **herramienta Aplicación** y elija la **sección** Manifiesto.</span><span class="sxs-lookup"><span data-stu-id="93df8-150">To review errors and warnings in your Web App Manifest, navigate to the **Application** tool and choose the **Manifest** section.</span></span>  <span data-ttu-id="93df8-151">Los errores y advertencias se enumeran en el **encabezado Errores y advertencias.**</span><span class="sxs-lookup"><span data-stu-id="93df8-151">Errors and warnings are listed under the **Errors and Warnings** heading.</span></span>  <span data-ttu-id="93df8-152">Para obtener más información sobre el manifiesto de aplicación web, vaya a Usar el manifiesto de aplicación [web para integrar la aplicación web progresiva en el sistema operativo][ProgressiveWebAppsWebappmanifests].</span><span class="sxs-lookup"><span data-stu-id="93df8-152">For more information about the Web App Manifest, navigate to [Use the Web App Manifest to integrate your Progressive Web App into the Operating System][ProgressiveWebAppsWebappmanifests].</span></span>  <span data-ttu-id="93df8-153">Para crear iconos para incluir en el manifiesto de la aplicación web, vaya al Generador de [imágenes de PWABuilder][PwabuilderImagegenerator].</span><span class="sxs-lookup"><span data-stu-id="93df8-153">To create icons to include in your Web App Manifest, navigate to the [PWABuilder Image Generator][PwabuilderImagegenerator].</span></span>  <span data-ttu-id="93df8-154">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto Chromium, vaya al problema [1185945][CR1185945].</span><span class="sxs-lookup"><span data-stu-id="93df8-154">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1185945][CR1185945].</span></span>  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a><span data-ttu-id="93df8-155">Localized DevTools ahora es compatible con exploradores basados en Chromium</span><span class="sxs-lookup"><span data-stu-id="93df8-155">Localized DevTools now supported in Chromium-based browsers</span></span>  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

<span data-ttu-id="93df8-156">A partir [de la versión 81 de Microsoft Edge,][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]Microsoft Edge DevTools se muestra en su propio idioma.</span><span class="sxs-lookup"><span data-stu-id="93df8-156">Starting in [Microsoft Edge version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools displays in your own language.</span></span>  <span data-ttu-id="93df8-157">Muchos desarrolladores usan otras herramientas de desarrollador como StackOverflow y Visual Studio Code en su idioma nativo, no solo en inglés.</span><span class="sxs-lookup"><span data-stu-id="93df8-157">Many developers use other developer tools like StackOverflow and Visual Studio Code in their native language, not just in English.</span></span>  <span data-ttu-id="93df8-158">El equipo de Microsoft Edge DevTools, el equipo de Chrome DevTools y el equipo de Google Lighthouse colaboraron para proporcionar la misma experiencia en todos los exploradores basados en Chromium.</span><span class="sxs-lookup"><span data-stu-id="93df8-158">The Microsoft Edge DevTools team, Chrome DevTools team, and the Google Lighthouse team collaborated to provide the same experience in all Chromium-based browsers.</span></span>  <span data-ttu-id="93df8-159">Para obtener más información sobre cómo usar DevTools en su idioma, vaya a [Cambiar la configuración de idioma de DevTools][DevtoolsCustomizeLocalization].</span><span class="sxs-lookup"><span data-stu-id="93df8-159">For more information about how to use DevTools in your language, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  <span data-ttu-id="93df8-160">Para obtener más información sobre la colaboración en esta característica en el proyecto de código abierto Chromium, vaya a [1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="93df8-160">For more information about the collaboration on this feature in the Chromium open-source project, navigate to [1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Explorador de Microsoft Edge y DevTools establecidos en japonés" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   <span data-ttu-id="93df8-162">Explorador de Microsoft Edge y DevTools establecidos en japonés</span><span class="sxs-lookup"><span data-stu-id="93df8-162">Microsoft Edge browser and DevTools set to Japanese</span></span>  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a><span data-ttu-id="93df8-163">Usar el teclado para navegar a variables CSS</span><span class="sxs-lookup"><span data-stu-id="93df8-163">Use the keyboard to navigate to CSS variables</span></span>  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

<span data-ttu-id="93df8-164">A partir [de la versión 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]de Microsoft Edge, el panel **Estilos** muestra variables CSS y proporciona un vínculo directamente a la definición de cada variable.</span><span class="sxs-lookup"><span data-stu-id="93df8-164">Starting in [Microsoft Edge version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], the **Styles** pane displays CSS variables and provides a link directly to the definition of each variable.</span></span>  <span data-ttu-id="93df8-165">En Microsoft Edge versión 91 o posterior, puede usar las teclas de flecha para navegar fácilmente a variables CSS.</span><span class="sxs-lookup"><span data-stu-id="93df8-165">In Microsoft Edge version 91 or later, you may use the arrow keys to easily navigate to CSS variables.</span></span>  <span data-ttu-id="93df8-166">Para abrir la definición en el panel **Estilos,** mantenga el mouse en una variable y, a continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="93df8-166">To open the definition in the **Styles** pane, hover on a variable, and then select `Enter`.</span></span>  <span data-ttu-id="93df8-167">Para obtener más información acerca de las variables CSS, vaya [a Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span><span class="sxs-lookup"><span data-stu-id="93df8-167">For more information about CSS variables, navigate to [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span></span>  <span data-ttu-id="93df8-168">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto Chromium, vaya al problema [1187735][CR1187735].</span><span class="sxs-lookup"><span data-stu-id="93df8-168">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1187735][CR1187735].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Variable CSS --theme-body-background resaltada en el panel Estilos" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   <span data-ttu-id="93df8-170">Variable `--theme-body-background` CSS resaltada en el **panel Estilos**</span><span class="sxs-lookup"><span data-stu-id="93df8-170">The `--theme-body-background` CSS variable highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a><span data-ttu-id="93df8-171">Los problemas se ordenan automáticamente por gravedad</span><span class="sxs-lookup"><span data-stu-id="93df8-171">Issues are automatically sorted by severity</span></span>  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

<span data-ttu-id="93df8-172">La **herramienta Problemas** muestra recomendaciones para mejorar el sitio web, incluida la accesibilidad, el rendimiento, la seguridad, entre otros.</span><span class="sxs-lookup"><span data-stu-id="93df8-172">The **Issues** tool displays recommendations to improve your website, including accessibility, performance, security, and so on.</span></span> <span data-ttu-id="93df8-173">En función de sus comentarios, los problemas ahora se ordenan automáticamente por gravedad.</span><span class="sxs-lookup"><span data-stu-id="93df8-173">Based on your feedback, issues are now automatically sorted by severity.</span></span>  <span data-ttu-id="93df8-174">En cada categoría de comentarios, cada problema marcado como **error** aparece primero, seguido de cada problema marcado como advertencia **y,** a continuación, cada problema marcado como **sugerencia**.</span><span class="sxs-lookup"><span data-stu-id="93df8-174">In each feedback category, each issue marked as an **Error** appears first, followed each issue marked as a **Warning**, then each issue marked as a **Tip**.</span></span>  <span data-ttu-id="93df8-175">Para ayudarle a refinar sus problemas, se planean opciones de filtro adicionales para una actualización futura.</span><span class="sxs-lookup"><span data-stu-id="93df8-175">To help you refine your issues, extra filter options are planned for a future update.</span></span>  <span data-ttu-id="93df8-176">Para obtener más información acerca de cómo revisar los problemas, vaya a [Buscar y corregir problemas con la herramienta Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="93df8-176">For more information about how to review issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="La herramienta Problemas muestra los problemas ordenados por gravedad" lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   <span data-ttu-id="93df8-178">La **herramienta Problemas** muestra los problemas ordenados por gravedad</span><span class="sxs-lookup"><span data-stu-id="93df8-178">The **Issues** tool displays sorted issues by severity</span></span>  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a><span data-ttu-id="93df8-179">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.7</span><span class="sxs-lookup"><span data-stu-id="93df8-179">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.7</span></span>  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

<span data-ttu-id="93df8-180">Microsoft [Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 proporciona devTools de Microsoft Edge versión [88][DevtoolsWhatsNew202011Devtools].</span><span class="sxs-lookup"><span data-stu-id="93df8-180">The [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 provides the DevTools from [Microsoft Edge version 88][DevtoolsWhatsNew202011Devtools].</span></span>  <span data-ttu-id="93df8-181">Esta extensión ahora es compatible ARM dispositivos y ya no depende de [la extensión Depurador para Microsoft Edge.][VisualstudioMarketplaceMsjsdiagDebuggerForEdge]</span><span class="sxs-lookup"><span data-stu-id="93df8-181">This extension now supports ARM devices and no longer depends on the [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extension.</span></span>  <span data-ttu-id="93df8-182">La versión 1.1.7 incluye las siguientes correcciones de errores y mejoras.</span><span class="sxs-lookup"><span data-stu-id="93df8-182">Version 1.1.7 includes the following bug fixes and improvements.</span></span>  

*   <span data-ttu-id="93df8-183">Se actualizó la confiabilidad del cierre de destino.</span><span class="sxs-lookup"><span data-stu-id="93df8-183">Updated the reliability of target closure.</span></span>  
*   <span data-ttu-id="93df8-184">Se actualizó el panel lateral para que se actualice automáticamente al depurar los destinos que se crean o destruyen.</span><span class="sxs-lookup"><span data-stu-id="93df8-184">Updated the side panel to automatically refreshes when you debug targets that are created or destroyed.</span></span>  
*   <span data-ttu-id="93df8-185">Se agregó un nuevo menú contextual que le ofrece un acceso más rápido a la configuración de extensión y al registro de cambios más reciente.</span><span class="sxs-lookup"><span data-stu-id="93df8-185">Added a new contextual menu that gives you faster access to the extension settings and the latest Changelog.</span></span>  
*   <span data-ttu-id="93df8-186">Se actualizó y simplificó la versión de la documentación de extensión, incluidas las características más nuevas.</span><span class="sxs-lookup"><span data-stu-id="93df8-186">Updated and simplified the release of extension documentation including the newest features.</span></span>  
    
<span data-ttu-id="93df8-187">Para actualizar manualmente a la versión 1.1.7, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="93df8-187">To manually update to version 1.1.7, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="93df8-188">Puede archivar los problemas y contribuir con la extensión en el [repositorio de GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="93df8-188">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

<!--## Announcements from the Chromium project  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Ipsum et Chromium  

Lorem al lorem et Chromium  To review the history of this feature in the Chromium open-source project, navigate to Issue [xxxxxxx][CRxxxxxxx].  

:::image type="complex" source="../../media/2021/04/lorem-et-chromium.msft.png" alt-text="Ipsum et Chromium" lightbox="../../media/2021/04/lorem-et-chromium.msft.png":::
   Ipsum et Chromium  
:::image-end:::  -->  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="93df8-189">Descargar los canales de versión preliminar de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="93df8-189">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="93df8-190">Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="93df8-190">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="93df8-191">Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="93df8-191">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="93df8-192">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="93df8-192">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Uso de DevTools en otros idiomas: novedades de DevTools (Microsoft Edge 81) | Microsoft Docs"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Novedades de DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools#css-variable-definitions-in-styles-pane "Definiciones de variables CSS en el panel Estilos: novedades de DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Novedades de DevTools (Microsoft Edge 90) | Microsoft Docs"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Agrupar herramientas en modo de enfoque: novedades de DevTools (Microsoft Edge 90) | Microsoft Docs"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Abra el menú Comando: ejecute comandos con el menú Comando de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Cambiar la configuración de idioma de DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsServiceWorkerIndex]: /microsoft-edge/devtools-guide-chromium/service-workers/index "Mejoras de service worker | Microsoft Docs"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: /microsoft-edge/progressive-web-apps-chromium/serviceworker#the-service-worker-lifecycle "Ciclo de vida del trabajador de servicio: usar los trabajadores de servicio para administrar las solicitudes de red y las notificaciones de inserción | Microsoft Docs"  
[ProgressiveWebAppsWebappmanifests]: /microsoft-edge/progressive-web-apps-chromium/webappmanifests "Usa el manifiesto de aplicación web para integrar la aplicación web progresiva en el sistema operativo | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de versiones preliminares de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Marketplace de extensiones | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  
[CR1066604]: https://crbug.com/1066604 "Problema 1066604: DevTools: Vea detalles sobre ServiceWorker para instalar y activar eventos | Errores de Chromium"  
[CR1136655]: https://crbug.com/1136655 "Problema 1136655: Devtools: Localización V2 | Errores de Chromium"  
[CR1185945]: https://crbug.com/1185945 "Problema 1185945: La advertencia de manifiesto implica que todos los iconos deben ser cuadrados | Errores de Chromium"  
[CR1187735]: https://crbug.com/1187735 "Problema 1187735: Accesibilidad: MAS2.1.1: Teclado: No se puede invocar la función 'Var(..)' con el teclado | Errores de Chromium"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propiedades personalizadas de CSS (variables) | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Generador de imágenes | PWABuilder"  

<!--  > [!NOTE]
> Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].  
> The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-91) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen
-->

---
description: Mejoras en la accesibilidad, con DevTools en otros idiomas y mucho más.
title: Novedades de DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7758b7f8ed55bb766abc56d6dd29ec124617e7ff
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408314"
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
# <a name="whats-new-in-devtools-microsoft-edge-80"></a><span data-ttu-id="0831c-104">Novedades de DevTools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="0831c-104">What's new in DevTools (Microsoft Edge 80)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0831c-105">Anuncios del equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0831c-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="0831c-106">Las siguientes secciones son una lista de anuncios que puede que falte del equipo de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="0831c-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="0831c-107">Echa un vistazo a los anuncios para probar nuevas características en DevTools, microsoft Visual Studio code extensions y mucho más.</span><span class="sxs-lookup"><span data-stu-id="0831c-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="0831c-108">Para mantenerse al día de todas las características más recientes y más importantes de las herramientas para desarrolladores, descargue los canales de vista previa de [Microsoft Edge][MicrosoftEdgePreviewChannels] y [síganos en Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="0831c-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="accessibility-improvements-to-the-devtools"></a><span data-ttu-id="0831c-109">Mejoras de accesibilidad a DevTools</span><span class="sxs-lookup"><span data-stu-id="0831c-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="0831c-110">El equipo de DevTools ha contribuido con 170 cambios a Chromium para solucionar problemas de contraste de color, teclado y lector de pantalla de alto impacto en DevTools.</span><span class="sxs-lookup"><span data-stu-id="0831c-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="0831c-111">Cada desarrollador que esté creando la web debe poder usar DevTools.</span><span class="sxs-lookup"><span data-stu-id="0831c-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="La herramienta Rendimiento de DevTools con las mejoras de navegación del teclado y lector de pantalla" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="0831c-113">La **herramienta Rendimiento** de DevTools con las mejoras de navegación del teclado y lector de pantalla</span><span class="sxs-lookup"><span data-stu-id="0831c-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-114">¿Desea obtener información sobre cómo hacer que la página web sea accesible para todos los usuarios?</span><span class="sxs-lookup"><span data-stu-id="0831c-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="0831c-115">Descargue las [extensiones Accessibility Insights][AccessibilityInsights] y [webhint][WebhintBrowserExtension] para Microsoft Edge para empezar.</span><span class="sxs-lookup"><span data-stu-id="0831c-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="0831c-116">Si usas lectores de pantalla o el teclado para [][PostTweetEdgeDevTools] navegar por devTools, envía tus comentarios tuiteando o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.</span><span class="sxs-lookup"><span data-stu-id="0831c-116">If you use screen readers or the keyboard to navigate around the DevTools, send your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="0831c-117">Problema de [chromium #963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="0831c-117">Chromium issue [#963183][CR963183]</span></span>  

### <a name="using-the-devtools-in-other-languages"></a><span data-ttu-id="0831c-118">Uso de DevTools en otros idiomas</span><span class="sxs-lookup"><span data-stu-id="0831c-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="0831c-119">Muchos desarrolladores usan otras herramientas de desarrollador, como StackOverflow y Visual Studio Code, en su idioma nativo, no solo en inglés.</span><span class="sxs-lookup"><span data-stu-id="0831c-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="0831c-120">Estamos encantados de anunciar la localización de DevTools, que ahora puedes usar en uno de los 10 idiomas además del inglés:</span><span class="sxs-lookup"><span data-stu-id="0831c-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="0831c-121">Chino \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="0831c-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0831c-122">Chino \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="0831c-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0831c-123">Francés : fran&#231;ais</span><span class="sxs-lookup"><span data-stu-id="0831c-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0831c-124">Alemán - deutsch</span><span class="sxs-lookup"><span data-stu-id="0831c-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0831c-125">Italiano - italiano</span><span class="sxs-lookup"><span data-stu-id="0831c-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0831c-126">Japonés - &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="0831c-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0831c-127">Coreano - &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="0831c-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0831c-128">Portugués : portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="0831c-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0831c-129">Ruso – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="0831c-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0831c-130">Español - espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="0831c-130">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文（简体）| Chinese (Traditional) - 中文（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="0831c-131">Vaya a y establezca la marca Habilitar herramientas de `edge://flags` **desarrollo** localizadas en **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="0831c-131">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="0831c-132">También establece la **marca de experimentos de Herramientas para desarrolladores** en **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="0831c-132">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="0831c-133">Reinicie Microsoft Edge y abra DevTools.</span><span class="sxs-lookup"><span data-stu-id="0831c-133">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Select `F1` in the DevTools or navigate to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="0831c-134">Las DevTools coinciden con el idioma que usa para Microsoft Edge en `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="0831c-134">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="DevTools en alemán" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   <span data-ttu-id="0831c-136">DevTools en alemán</span><span class="sxs-lookup"><span data-stu-id="0831c-136">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-137">Si quieres usar DevTools en un idioma diferente al que está [disponible,][PostTweetEdgeDevTools] envíanos un tweet o elige el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.</span><span class="sxs-lookup"><span data-stu-id="0831c-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or choose the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="0831c-138">Problema de [chromium #941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="0831c-138">Chromium issue [#941561][CR941561]</span></span>  

### <a name="webhint-microsoft-edge-extension"></a><span data-ttu-id="0831c-139">extensión webhint de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0831c-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="0831c-140">La extensión webhint de Microsoft Edge le permite examinar fácilmente su página web y obtener comentarios sobre accesibilidad, compatibilidad del explorador, seguridad, rendimiento y mucho más dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="0831c-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="0831c-141">Leer más en [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="0831c-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="La herramienta Sugerencias en DevTools cuando se instala la extensión del explorador webhint" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   <span data-ttu-id="0831c-143">La **herramienta Sugerencias** en DevTools cuando se instala la extensión del explorador webhint</span><span class="sxs-lookup"><span data-stu-id="0831c-143">The **Hints** tool in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-144">[Pruebe la extensión del explorador webhint en Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="0831c-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="0831c-145">Una vez instalada la extensión, abra DevTools y elija la **herramienta Sugerencias.**</span><span class="sxs-lookup"><span data-stu-id="0831c-145">Once you install the extension, open the DevTools and choose the **Hints** tool.</span></span>  <span data-ttu-id="0831c-146">Desde aquí, ejecute un examen de sitio personalizable.</span><span class="sxs-lookup"><span data-stu-id="0831c-146">From here, run a customizable site scan.</span></span>  <span data-ttu-id="0831c-147">Dirígete a [webhint.io][WebhintBrowserExtension] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0831c-147">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <a name="3d-view"></a><span data-ttu-id="0831c-148">Vista 3D</span><span class="sxs-lookup"><span data-stu-id="0831c-148">3D View</span></span>  

<span data-ttu-id="0831c-149">Use la **vista 3D** para depurar la aplicación web navegando por el modelo de objetos de documento [\(DOM\)][MDNDocumentObjectModel] o el contexto de apilamiento [de índice z.][MDNZIndex]</span><span class="sxs-lookup"><span data-stu-id="0831c-149">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="La vista 3D en DevTools" lightbox="../../images/2019/12/3dview.msft.png":::
   <span data-ttu-id="0831c-151">La **vista 3D en** DevTools</span><span class="sxs-lookup"><span data-stu-id="0831c-151">The **3D View** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-152">Para obtener acceso a la vista 3D, vaya a y asegúrese de que la marca de experimentos de `edge://flags` **Developer Tools** está establecida en **Enabled**.</span><span class="sxs-lookup"><span data-stu-id="0831c-152">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="0831c-153">Reinicie Microsoft Edge y abra DevTools.</span><span class="sxs-lookup"><span data-stu-id="0831c-153">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="0831c-154">Seleccione en la sección DevTools o abra la sección Experimentos de configuración y active la casilla Habilitar vista `F1`   >   **3D.**</span><span class="sxs-lookup"><span data-stu-id="0831c-154">Select `F1` in the DevTools or open the **Settings** > **Experiments** section, and turn on the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="0831c-155">Ahora, seleccione `Ctrl`  +  `Shift`  +  `P` , escriba en **Vista 3D** y **seleccione Mostrar vista 3D**.</span><span class="sxs-lookup"><span data-stu-id="0831c-155">Now, select `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="0831c-156">Estamos trabajando en la interfaz de usuario y agregando más funcionalidad a la vista 3D, así que envíenos sus [comentarios.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="0831c-156">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="0831c-157">Problema de [chromium #987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="0831c-157">Chromium issue [#987787][CR987787]</span></span>

### <a name="visual-studio-code-extensions"></a><span data-ttu-id="0831c-158">Visual Studio de código</span><span class="sxs-lookup"><span data-stu-id="0831c-158">Visual Studio Code extensions</span></span>  

<span data-ttu-id="0831c-159">El equipo de DevTools también ha publicado algunas extensiones para [Visual Studio Code][VisualStudioCode] que te permiten usar la potencia de DevTools directamente desde el editor de texto.</span><span class="sxs-lookup"><span data-stu-id="0831c-159">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor.</span></span> <span data-ttu-id="0831c-160">Consulte las siguientes extensiones.</span><span class="sxs-lookup"><span data-stu-id="0831c-160">Check out the following extensions.</span></span>  

#### <a name="elements-for-microsoft-edge"></a><span data-ttu-id="0831c-161">Elementos para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0831c-161">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="0831c-162">Usa la herramienta Elementos desde dentro de Visual Studio código agregando la [extensión Elements for Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="0831c-162">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="La herramienta Elementos de Visual Studio código mediante la extensión Elementos para Microsoft Edge" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   <span data-ttu-id="0831c-164">La **herramienta Elementos** de Visual Studio código mediante la extensión Elementos para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0831c-164">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-165">Para obtener más información, consulte [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="0831c-165">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <a name="debugger-for-microsoft-edge"></a><span data-ttu-id="0831c-166">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0831c-166">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="0831c-167">Con la extensión de código Visual Studio Depurador para [Microsoft Edge,][VisualStudioMarketplaceDebuggerEdge] depura JavaScript que se ejecuta en Microsoft Edge directamente desde Visual Studio código.</span><span class="sxs-lookup"><span data-stu-id="0831c-167">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="El depurador para la extensión de Microsoft Edge en Visual Studio código" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   <span data-ttu-id="0831c-169">El depurador para la extensión de Microsoft Edge en Visual Studio código</span><span class="sxs-lookup"><span data-stu-id="0831c-169">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-170">Para obtener más información, [consulte cómo depurar Microsoft Edge desde Visual Studio code][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="0831c-170">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <a name="webhint"></a><span data-ttu-id="0831c-171">webhint</span><span class="sxs-lookup"><span data-stu-id="0831c-171">webhint</span></span>  

<span data-ttu-id="0831c-172">La extensión de Visual Studio [Webhint][VisualStudioMarketplaceWebhintExtension] usa para mejorar la página `webhint` web mientras la escribe.</span><span class="sxs-lookup"><span data-stu-id="0831c-172">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="0831c-173">Esta extensión ejecuta e informa de diagnósticos en los archivos del área de trabajo en función del `webhint` análisis.</span><span class="sxs-lookup"><span data-stu-id="0831c-173">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="La extensión de Visual Studio webhint analiza un archivo .tsx en Visual Studio code" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="0831c-175">La extensión de Visual Studio webhint analiza un `.tsx` archivo en Visual Studio código</span><span class="sxs-lookup"><span data-stu-id="0831c-175">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-176">[Obtenga más información sobre la Visual Studio webhint][WebhintVisualStudioCodeExtension]code .</span><span class="sxs-lookup"><span data-stu-id="0831c-176">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <a name="visual-studio-integration"></a><span data-ttu-id="0831c-177">Visual Studio integración</span><span class="sxs-lookup"><span data-stu-id="0831c-177">Visual Studio integration</span></span>  

<span data-ttu-id="0831c-178">En Visual Studio versión 16.2 o posterior de 2019, use el depurador Visual Studio para depurar JavaScript que se ejecuta en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0831c-178">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="0831c-179">[Descargue Visual Studio 2019 para][MicrosoftVisualStudioDownloads] probar esta característica.</span><span class="sxs-lookup"><span data-stu-id="0831c-179">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out.</span></span>  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canary, Dev o Beta" lightbox="../../images/2019/12/vs.msft.png":::
   <span data-ttu-id="0831c-181">Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canary, Dev o Beta</span><span class="sxs-lookup"><span data-stu-id="0831c-181">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-182">[Lea nuestra entrada de blog para obtener información sobre cómo depurar Microsoft Edge desde Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="0831c-182">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <a name="tracking-prevention-console-messages"></a><span data-ttu-id="0831c-183">Seguimiento de mensajes de consola de prevención</span><span class="sxs-lookup"><span data-stu-id="0831c-183">Tracking prevention Console messages</span></span>  

<span data-ttu-id="0831c-184">La prevención de seguimiento es una característica única de Microsoft Edge que impide que un sitio web le realice un seguimiento antes de visitarla.</span><span class="sxs-lookup"><span data-stu-id="0831c-184">Tracking prevention is a unique feature in Microsoft Edge that blocks you from being tracked by a website before you visited it.</span></span>  <span data-ttu-id="0831c-185">La configuración predeterminada de prevención de seguimiento es el modo equilibrado, que bloquea los rastreadores de terceros y los rastreadores malintencionados conocidos para una experiencia que equilibra la privacidad y la compatibilidad web.</span><span class="sxs-lookup"><span data-stu-id="0831c-185">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="0831c-186">Para obtener más información sobre la compatibilidad de la página web cuando se bloquean  determinados rastreadores, el equipo de Microsoft Edge agregó mensajes de advertencia en la consola cuando se bloquea un rastreador.</span><span class="sxs-lookup"><span data-stu-id="0831c-186">To give you more insight into the compatibility of your web page when certain trackers are blocked, The Microsoft Edge team added warning messages in the **Console** when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Mensajes en la consola cuando la prevención de seguimiento bloquea el acceso al almacenamiento de un rastreador" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   <span data-ttu-id="0831c-188">Mensajes en la **consola cuando** la prevención de seguimiento bloquea el acceso al almacenamiento de un rastreador</span><span class="sxs-lookup"><span data-stu-id="0831c-188">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-189">[Obtenga más información sobre la prevención de seguimiento y el equilibrio entre privacidad y compatibilidad web.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="0831c-189">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="0831c-190">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="0831c-190">Announcements from the Chromium project</span></span>  

<span data-ttu-id="0831c-191">En las secciones siguientes se anuncian características adicionales disponibles en Microsoft Edge 80 que se contribuyeron al proyecto chromium de código abierto.</span><span class="sxs-lookup"><span data-stu-id="0831c-191">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <a name="support-for-let-and-class-redeclarations-in-the-console"></a><span data-ttu-id="0831c-192">Compatibilidad con las declaraciones de let y class en la consola</span><span class="sxs-lookup"><span data-stu-id="0831c-192">Support for let and class redeclarations in the Console</span></span>  

<span data-ttu-id="0831c-193">La **consola** ahora admite las declaraciones de y `let` las `class` instrucciones.</span><span class="sxs-lookup"><span data-stu-id="0831c-193">The **Console** now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="0831c-194">La incapacidad de volver a declarar era una molestia común para los desarrolladores web que usan la consola para experimentar con el nuevo código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0831c-194">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="0831c-195">La declaración de una instrucción or en un script fuera de la consola o dentro de una sola entrada `let` `class` de consola sigue provocando un `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="0831c-195">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="0831c-196">Por ejemplo, anteriormente, al volver a declarar una variable local con , la `let` consola produjo un error:</span><span class="sxs-lookup"><span data-stu-id="0831c-196">For example, previously, when re-declaring a local variable with `let`, the Console threw an error:</span></span>  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="La consola de Microsoft Edge 79 que muestra que se produce un error en la reeclaración de let" lightbox="../../images/2019/12/letbefore.msft.png":::
   <span data-ttu-id="0831c-198">La **consola** de Microsoft Edge 79 que muestra que se produce un error en la nueva declaración de let</span><span class="sxs-lookup"><span data-stu-id="0831c-198">The **Console** in Microsoft Edge 79 showing that the let re-declaration fails</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-199">Ahora, la consola permite la nueva declaración:</span><span class="sxs-lookup"><span data-stu-id="0831c-199">Now, the Console allows the redeclaration:</span></span>  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="La consola de Microsoft Edge 80 que muestra que la nueva declaración de let se realiza correctamente" lightbox="../../images/2019/12/letafter.msft.png":::
   <span data-ttu-id="0831c-201">La **consola** de Microsoft Edge 80 que muestra que la nueva declaración de let se realiza correctamente</span><span class="sxs-lookup"><span data-stu-id="0831c-201">The **Console** in Microsoft Edge 80 showing that the let re-declaration succeeds</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-202">Problema de [chromium #1004193][CR1004193]</span><span class="sxs-lookup"><span data-stu-id="0831c-202">Chromium issue [#1004193][CR1004193]</span></span>  

### <a name="improved-webassembly-debugging"></a><span data-ttu-id="0831c-203">Depuración de WebAssembly mejorada</span><span class="sxs-lookup"><span data-stu-id="0831c-203">Improved WebAssembly debugging</span></span>  

<span data-ttu-id="0831c-204">DevTools ha comenzado a admitir el estándar de depuración [DESANADO,][DwarfHome]lo que significa una mayor compatibilidad para pasar por encima del código, establecer puntos de interrupción y resolver seguimientos de pila en los idiomas de origen dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="0831c-204">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### <a name="network-panel-updates"></a><span data-ttu-id="0831c-205">Actualizaciones del panel de red</span><span class="sxs-lookup"><span data-stu-id="0831c-205">Network panel updates</span></span>  

#### <a name="request-initiator-chains-in-the-initiator-panel"></a><span data-ttu-id="0831c-206">Solicitar cadenas de iniciador en el panel Iniciador</span><span class="sxs-lookup"><span data-stu-id="0831c-206">Request Initiator Chains in the Initiator panel</span></span>  

<span data-ttu-id="0831c-207">Ahora puede ver los iniciadores y las dependencias de una solicitud de red como una lista anidada.</span><span class="sxs-lookup"><span data-stu-id="0831c-207">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="0831c-208">Esto puede ayudarle a comprender por qué se solicitó un recurso o qué actividad de red causó un determinado recurso \(como un script\).</span><span class="sxs-lookup"><span data-stu-id="0831c-208">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Una cadena de iniciador de solicitud en el panel Iniciador" lightbox="../../images/2019/12/initiators.msft.png":::
   <span data-ttu-id="0831c-210">Una cadena de iniciador de solicitud en el panel **Iniciador**</span><span class="sxs-lookup"><span data-stu-id="0831c-210">A Request Initiator Chain in the **Initiator** panel</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-211">Después [de registrar la actividad de red en el panel][DevToolsNetworkIndex]Red, elija un recurso y, a continuación, vaya al panel Iniciador para ver la Cadena de **iniciador de solicitud**: </span><span class="sxs-lookup"><span data-stu-id="0831c-211">After [logging network activity in the Network panel][DevToolsNetworkIndex], choose a resource and then navigate to the **Initiator** panel to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="0831c-212">El **recurso inspeccionado** es negrita.</span><span class="sxs-lookup"><span data-stu-id="0831c-212">The **inspected resource** is bold.</span></span>  <span data-ttu-id="0831c-213">En la captura de pantalla anterior, `ai.2.min.js` está el recurso inspeccionado.</span><span class="sxs-lookup"><span data-stu-id="0831c-213">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="0831c-214">Los recursos que se encuentran encima del recurso inspeccionado son **los iniciadores**.</span><span class="sxs-lookup"><span data-stu-id="0831c-214">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="0831c-215">En la captura de pantalla anterior, `https://www.microsoftedgeinsider.com` está el iniciador de `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="0831c-215">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="0831c-216">En otras palabras, `https://www.microsoftedgeinsider.com` causó la solicitud de red para `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="0831c-216">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="0831c-217">Los recursos debajo del recurso inspeccionado son las **dependencias**.</span><span class="sxs-lookup"><span data-stu-id="0831c-217">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="0831c-218">En la captura de pantalla anterior, `https://dc.services.visualstudio.com/v2/track` es una dependencia de `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="0831c-218">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="0831c-219">En otras palabras, `ai.2.min.js` causó la solicitud de red para `https://dc.services.visualstudio.com/v2/track` .</span><span class="sxs-lookup"><span data-stu-id="0831c-219">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="0831c-220">También se puede tener acceso a la información del iniciador y la dependencia manteniendo presionado y, a `Shift` continuación, manteniendo el mouse sobre los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="0831c-220">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="0831c-221">Vaya a [Ver iniciadores y dependencias][DevToolsNetworkReferenceViewInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="0831c-221">Navigate to [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="0831c-222">Problema de [chromium #842488][CR842488]</span><span class="sxs-lookup"><span data-stu-id="0831c-222">Chromium issue [#842488][CR842488]</span></span>  

#### <a name="highlight-the-selected-network-request-in-the-overview"></a><span data-ttu-id="0831c-223">Resalte la solicitud de red seleccionada en información general</span><span class="sxs-lookup"><span data-stu-id="0831c-223">Highlight the selected network request in the Overview</span></span>  

<span data-ttu-id="0831c-224">Después de elegir un recurso de red para inspeccionarlo, el panel Red coloca ahora un borde azul alrededor de ese recurso en **overview**.</span><span class="sxs-lookup"><span data-stu-id="0831c-224">After you choose a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="0831c-225">Esto puede ayudarle a detectar si la solicitud de red se está produciendo antes o después de lo esperado.</span><span class="sxs-lookup"><span data-stu-id="0831c-225">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="El panel Información general que resalta el recurso inspeccionado" lightbox="../../images/2019/12/overview.msft.png":::
   <span data-ttu-id="0831c-227">El **panel Información** general que resalta el recurso inspeccionado</span><span class="sxs-lookup"><span data-stu-id="0831c-227">The **Overview** pane highlighting the inspected resource</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-228">Problema de [chromium #988253][CR988253]</span><span class="sxs-lookup"><span data-stu-id="0831c-228">Chromium issue [#988253][CR988253]</span></span>  

#### <a name="url-and-path-columns-in-the-network-panel"></a><span data-ttu-id="0831c-229">Columnas de dirección URL y ruta de acceso en el panel Red</span><span class="sxs-lookup"><span data-stu-id="0831c-229">URL and path columns in the Network panel</span></span>  

<span data-ttu-id="0831c-230">Use las nuevas columnas **Path** y **URL** de la **herramienta Red** para mostrar la ruta de acceso absoluta o la dirección URL completa de cada recurso de red.</span><span class="sxs-lookup"><span data-stu-id="0831c-230">Use the new **Path** and **URL** columns in the **Network** tool to display the absolute path or full URL of each network resource.</span></span>  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="Las nuevas columnas Ruta de acceso y dirección URL en el panel Red" lightbox="../../images/2019/12/columns.msft.png":::
   <span data-ttu-id="0831c-232">Las nuevas columnas Ruta de acceso y DIRECCIÓN URL de la **herramienta Red**</span><span class="sxs-lookup"><span data-stu-id="0831c-232">The new Path and URL columns in the **Network** tool</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-233">Para mostrar las nuevas columnas, mantenga el mouse en el encabezado de la tabla **Cascada,** abra el menú contextual \(righ-click\) y elija **Ruta** de acceso o **dirección URL**.</span><span class="sxs-lookup"><span data-stu-id="0831c-233">To display the new columns, hover on the **Waterfall** table header, open the contextual menu \(righ-click\), and choose **Path** or **URL**.</span></span>  

<span data-ttu-id="0831c-234">Problema de chromium [#993366][CR993366]</span><span class="sxs-lookup"><span data-stu-id="0831c-234">Chromium issue [#993366][CR993366]</span></span>  

#### <a name="updated-user-agent-strings"></a><span data-ttu-id="0831c-235">Cadenas User-Agent actualizadas</span><span class="sxs-lookup"><span data-stu-id="0831c-235">Updated User-Agent strings</span></span>  

<span data-ttu-id="0831c-236">DevTools admite la configuración de una cadena User-Agent a través del panel **Condiciones de** red.</span><span class="sxs-lookup"><span data-stu-id="0831c-236">DevTools supports setting a custom User-Agent string through the **Network Conditions** panel.</span></span>  <span data-ttu-id="0831c-237">La User-Agent la cadena afecta al encabezado HTTP adjunto a los recursos de red `User-Agent` y también al valor de `navigator.userAgent` .</span><span class="sxs-lookup"><span data-stu-id="0831c-237">The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="0831c-238">Las cadenas User-Agent se han actualizado para reflejar las versiones modernas del explorador.</span><span class="sxs-lookup"><span data-stu-id="0831c-238">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="Menú Agente de usuario en el panel Condiciones de red" lightbox="../../images/2019/12/useragent.msft.png":::
   <span data-ttu-id="0831c-240">Menú Agente de usuario en el panel **Condiciones de red**</span><span class="sxs-lookup"><span data-stu-id="0831c-240">The User Agent menu in the **Network Conditions** panel</span></span>  
:::image-end:::  

<span data-ttu-id="0831c-241">Para obtener **acceso a las condiciones de**red, abra el menú [comando][DevToolsCommandMenuIndex] y ejecute el `Show Network Conditions` comando.</span><span class="sxs-lookup"><span data-stu-id="0831c-241">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="0831c-242">También puedes establecer [cadenas User-Agent en modo dispositivo][DevToolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="0831c-242">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="0831c-243">Problema de [chromium #1029031][CR1029031]</span><span class="sxs-lookup"><span data-stu-id="0831c-243">Chromium issue [#1029031][CR1029031]</span></span>  

### <a name="audits-panel-updates"></a><span data-ttu-id="0831c-244">Actualizaciones del panel Auditorías</span><span class="sxs-lookup"><span data-stu-id="0831c-244">Audits panel updates</span></span>  

#### <a name="new-configuration-ui"></a><span data-ttu-id="0831c-245">Nueva interfaz de usuario de configuración</span><span class="sxs-lookup"><span data-stu-id="0831c-245">New configuration UI</span></span>  

<span data-ttu-id="0831c-246">La interfaz de usuario de configuración tiene un diseño nuevo y dinámico y se han simplificado las opciones de configuración de limitación.</span><span class="sxs-lookup"><span data-stu-id="0831c-246">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="0831c-247">Para obtener más información sobre los cambios de la interfaz de usuario de limitación, vaya a [Limitación del panel auditorías][GitHubGoogleChromeDevToolsAuditsPanelThrottling].</span><span class="sxs-lookup"><span data-stu-id="0831c-247">For more information on the throttling UI changes, navigate to [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling].</span></span>  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="La nueva interfaz de usuario de configuración" lightbox="../../images/2019/12/start.msft.png":::
   <span data-ttu-id="0831c-249">La nueva interfaz de usuario de configuración</span><span class="sxs-lookup"><span data-stu-id="0831c-249">The new configuration UI</span></span>  
:::image-end:::  

### <a name="coverage-tool-updates"></a><span data-ttu-id="0831c-250">Actualizaciones de la herramienta de cobertura</span><span class="sxs-lookup"><span data-stu-id="0831c-250">Coverage tool updates</span></span>  

#### <a name="per-function-or-per-block-coverage-modes"></a><span data-ttu-id="0831c-251">Modos de cobertura por función o por bloque</span><span class="sxs-lookup"><span data-stu-id="0831c-251">Per-function or per-block coverage modes</span></span>  

<span data-ttu-id="0831c-252">La [herramienta Cobertura][DevToolsCoverageIndex] tiene un nuevo menú desplegable que le permite especificar si los datos de cobertura de código deben recopilarse por **función** o **por bloque**.</span><span class="sxs-lookup"><span data-stu-id="0831c-252">The [Coverage][DevToolsCoverageIndex] tool has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="0831c-253">**La cobertura por** bloque es más detallada, pero también mucho más costosa de recopilar.</span><span class="sxs-lookup"><span data-stu-id="0831c-253">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="0831c-254">DevTools usa **la cobertura por** función de forma predeterminada ahora.</span><span class="sxs-lookup"><span data-stu-id="0831c-254">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="0831c-255">Es posible que observe grandes diferencias de cobertura de código en los archivos HTML en función de si usa **por función** o por **modo de** bloque.</span><span class="sxs-lookup"><span data-stu-id="0831c-255">You may notice large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="0831c-256">Cuando se **usa por modo** de función, los scripts en línea en archivos HTML se tratan como funciones.</span><span class="sxs-lookup"><span data-stu-id="0831c-256">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="0831c-257">Si el script se ejecuta en absoluto, DevTools marca todo el script como código usado.</span><span class="sxs-lookup"><span data-stu-id="0831c-257">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="0831c-258">Solo si el script no se ejecuta en absoluto, DevTools marca el script como código no usado.</span><span class="sxs-lookup"><span data-stu-id="0831c-258">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="Menú desplegable del modo de cobertura" lightbox="../../images/2019/12/modes.msft.png":::
   <span data-ttu-id="0831c-260">Menú desplegable del modo de cobertura</span><span class="sxs-lookup"><span data-stu-id="0831c-260">The coverage mode dropdown menu</span></span>  
:::image-end:::  

#### <a name="coverage-must-now-be-initiated-by-a-page-refresh"></a><span data-ttu-id="0831c-261">La cobertura debe iniciarse ahora mediante una actualización de página</span><span class="sxs-lookup"><span data-stu-id="0831c-261">Coverage must now be initiated by a page refresh</span></span>  

<span data-ttu-id="0831c-262">Se ha quitado la cobertura de código de alternar sin una actualización de página porque los datos de cobertura no son confiables.</span><span class="sxs-lookup"><span data-stu-id="0831c-262">Toggling code coverage without a page refresh has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="0831c-263">Por ejemplo, una función puede ser notificada como no usada si el tiempo de ejecución estaba hace mucho tiempo y el recolector de elementos no utilizados V8 la ha limpiado.</span><span class="sxs-lookup"><span data-stu-id="0831c-263">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="0831c-264">Problema de [chromium #1004203][CR1004203]</span><span class="sxs-lookup"><span data-stu-id="0831c-264">Chromium issue [#1004203][CR1004203]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="0831c-265">Descargar los canales de vista previa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0831c-265">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="0831c-266">Si estás en Windows o macOS, considera usar los canales de vista [previa de Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0831c-266">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="0831c-267">Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="0831c-267">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="0831c-268">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0831c-268">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

<!--[../../images/2019/12/wasm.msft.png]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevToolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Busque código JavaScript y CSS sin usar con la herramienta Cobertura en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular una ventanilla móvil: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsNetworkIndex]: /microsoft-edge/devtools-guide-chromium/network/index "Inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#view-initiators-and-dependencies "Ver iniciadores y dependencias: referencia de análisis de red | Microsoft Docs"  
[DevGuideEdgeHtmlWhatsNew]: /microsoft-edge/dev-guide/whats-new "Novedades de EdgeHTML | Microsoft Docs"  
[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Depurador para Microsoft Edge Visual Studio de código | Microsoft Docs"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Elementos para microsoft Edge Visual Studio de código | Microsoft Docs"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Agregue el campo Iniciador a la pestaña Encabezados | Errores de Chromium"  
[CR988253]: https://crbug.com/988253 "Bug DevTools: ninguna asociación entre la solicitud de red y el gráfico de escala de tiempo | Errores de Chromium"  
[CR993366]: https://crbug.com/993366 "Muestre la parte de ruta de acceso de la dirección URL en la lista de solicitudes de panel de red | Errores de Chromium"  
[CR1004193]: https://crbug.com/1004193 "Modo REPL para V8 | Errores de Chromium"  
[CR1004203]: https://crbug.com/1004203 "Hacer que la cobertura de código sea | Errores de Chromium"  
[CR1029031]: https://crbug.com/1029031 "Las cadenas UA se están volviendo obsoletas | Errores de Chromium" 
[CR963183]: https://crbug.com/963183 "DevTools no son compatibles con WCAG | Errores de Chromium"
[CR941561]: https://crbug.com/941561 "Localizabilidad del | Errores de Chromium"
[CR987787]: https://crbug.com/987787 "Dom 3D View | Errores de Chromium"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Accessibility Insights"  

[DwarfHome]: https://dwarfstd.org "Casa enana"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "Limitación del panel de auditorías de DevTools: GoogleChrome/| GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nuevo problema: MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canales de vista previa de Microsoft Edge"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Complementos insider de Microsoft Edge"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Depurar JavaScript en Microsoft Edge desde Visual Studio | Visual Studio Blog"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Descargar Visual Studio 2019 para Windows \& Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objetos de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "Z-index | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools cuenta de Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio código"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge: Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos para Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint: Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extensión de explorador Webhint | documentación de webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio de código | documentación de webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Mejorar la prevención de seguimiento en la entrada de blog de Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "La web que queremos"

> [!NOTE]
> <span data-ttu-id="0831c-308">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0831c-308">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0831c-309">La página original se encuentra [aquí](https://developers.google.com/web/updates/2019/12/devtools/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="0831c-309">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0831c-311">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0831c-311">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
description: Vista 3D, integración de Visual Studio con Microsoft Edge y mucho más.
title: Novedades de DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 3081ebb256a9ede637aaaddc3c3cdf7a70a201bb
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015478"
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

# <span data-ttu-id="92bc9-104">Novedades de DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="92bc9-104">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <span data-ttu-id="92bc9-105">Anuncios del equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="92bc9-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="92bc9-106">Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo de DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="92bc9-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="92bc9-107">Compruébelos para probar nuevas características en DevTools, Visual Studio Code Extensions y mucho más.</span><span class="sxs-lookup"><span data-stu-id="92bc9-107">Check them out to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="92bc9-108">Para mantenerte al tanto de las últimas y mejores características de las herramientas para desarrolladores, descarga los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] y mantente [en Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="92bc9-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="92bc9-109">Mejoras de accesibilidad para el DevTools</span><span class="sxs-lookup"><span data-stu-id="92bc9-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="92bc9-110">El equipo de DevTools ha contribuido a 170 cambios en cromo para solucionar problemas de alto impacto en el contraste de color, el teclado y el lector de pantalla en el DevTools.</span><span class="sxs-lookup"><span data-stu-id="92bc9-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="92bc9-111">Cada desarrollador que crea la web debe poder usar el DevTools.</span><span class="sxs-lookup"><span data-stu-id="92bc9-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="La herramienta de rendimiento en el DevTools con la navegación con el teclado y las mejoras del lector de pantalla" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="92bc9-113">La herramienta de **rendimiento** en el DevTools con la navegación con el teclado y las mejoras del lector de pantalla</span><span class="sxs-lookup"><span data-stu-id="92bc9-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-114">¿Desea saber cómo hacer que su página web sea accesible para todos los usuarios?</span><span class="sxs-lookup"><span data-stu-id="92bc9-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="92bc9-115">Descargue [Insight Insights][AccessibilityInsights] y extensiones [Webhint][WebhintBrowserExtension] para Microsoft Edge para comenzar.</span><span class="sxs-lookup"><span data-stu-id="92bc9-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="92bc9-116">Si usa lectores de pantalla o el teclado para desplazarse por la DevTools, envíenos sus comentarios con un [Tweet][PostTweetEdgeDevTools] o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="92bc9-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="92bc9-117">[#963183][CR963183] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="92bc9-117">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="92bc9-118">Usar el DevTools en otros idiomas</span><span class="sxs-lookup"><span data-stu-id="92bc9-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="92bc9-119">Muchos programadores usan otras herramientas de desarrollo, como StackOverflow y Visual Studio, en su idioma nativo, no solo en inglés.</span><span class="sxs-lookup"><span data-stu-id="92bc9-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="92bc9-120">Nos complace anunciar la localización de la DevTools, que ahora puedes usar en uno de los 10 idiomas además del inglés:</span><span class="sxs-lookup"><span data-stu-id="92bc9-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="92bc9-121">Chino \ (simplificado \)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="92bc9-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="92bc9-122">Chino (tradicional \)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="92bc9-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="92bc9-123">Francés: Francisco&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="92bc9-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="92bc9-124">Alemán-Deutsch</span><span class="sxs-lookup"><span data-stu-id="92bc9-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="92bc9-125">Italiano-Italiano</span><span class="sxs-lookup"><span data-stu-id="92bc9-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="92bc9-126"> &#26085;&#26412;&#35486; japonés</span><span class="sxs-lookup"><span data-stu-id="92bc9-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="92bc9-127">Coreano:  &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="92bc9-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="92bc9-128">Portugués-Portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="92bc9-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="92bc9-129">Ruso:  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="92bc9-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="92bc9-130">Español-Espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="92bc9-130">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="92bc9-131">El DevTools coincide automáticamente con el idioma que usas para Microsoft Edge en `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="92bc9-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="92bc9-132">Si desea que Microsoft Edge esté en un idioma y que su DevTools permanezca en inglés, presione `F1` la DevTools para abrir la [configuración][Settings] y deshabilitar el **idioma del explorador**.</span><span class="sxs-lookup"><span data-stu-id="92bc9-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, press `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="El DevTools en alemán" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   <span data-ttu-id="92bc9-134">El DevTools en alemán</span><span class="sxs-lookup"><span data-stu-id="92bc9-134">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-135">Los mensajes de **consola** no se localizan.</span><span class="sxs-lookup"><span data-stu-id="92bc9-135">**Console** messages are not localized.</span></span>  <span data-ttu-id="92bc9-136">Solo las cadenas usadas en la interfaz de usuario de DevTools se muestran en el idioma que usas para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="92bc9-136">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="92bc9-137">Si desea usar la DevTools en un idioma diferente al de los que están disponibles, [Tweet][PostTweetEdgeDevTools] o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="92bc9-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="92bc9-138">[#941561][CR941561] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="92bc9-138">Chromium issue [#941561][CR941561]</span></span>  

### <span data-ttu-id="92bc9-139">extensión webhint de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="92bc9-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="92bc9-140">La extensión webhint de Microsoft Edge te permite examinar fácilmente tu página web y obtener comentarios sobre la accesibilidad, la compatibilidad de explorador, la seguridad, el rendimiento y mucho más dentro de la DevTools.</span><span class="sxs-lookup"><span data-stu-id="92bc9-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="92bc9-141">Para obtener más información, consulte [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="92bc9-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="La pestaña sugerencias de la DevTools cuando está instalada la extensión de explorador webhint" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   <span data-ttu-id="92bc9-143">La pestaña **sugerencias** de la DevTools cuando está instalada la extensión de explorador webhint</span><span class="sxs-lookup"><span data-stu-id="92bc9-143">The **Hints** tab in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-144">[Prueba la extensión de explorador webhint en Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="92bc9-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="92bc9-145">Una vez que haya instalado la extensión, abra el DevTools y seleccione la pestaña sugerencias.  Desde aquí, ejecute un examen de sitios personalizable.</span><span class="sxs-lookup"><span data-stu-id="92bc9-145">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="92bc9-146">Visita [webhint.IO][WebhintBrowserExtension] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="92bc9-146">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <span data-ttu-id="92bc9-147">Vista 3D</span><span class="sxs-lookup"><span data-stu-id="92bc9-147">3D View</span></span>  

<span data-ttu-id="92bc9-148">Use la **vista 3D** para depurar la aplicación web desplazándose por el [modelo de objeto de documento \ (Dom \)][MDNDocumentObjectModel] o el contexto de apilamiento [de índice z][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="92bc9-148">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="Vista 3D en el DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   <span data-ttu-id="92bc9-150">Vista 3D en el DevTools</span><span class="sxs-lookup"><span data-stu-id="92bc9-150">The 3D View in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-151">Para acceder a la vista 3D, pulse `Ctrl`  +  `Shift`  +  `P` , escriba en la **vista 3D** y seleccione **Mostrar vista en 3D**.</span><span class="sxs-lookup"><span data-stu-id="92bc9-151">To access the 3D View, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="92bc9-152">Trabajamos en la interfaz de usuario y agregamos más funcionalidad a la vista 3D; por lo tanto, envíanos tus [comentarios](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="92bc9-152">We're working on the UI and adding more functionality to the 3D View, so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="92bc9-153">[#987787][CR987787] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="92bc9-153">Chromium issue [#987787][CR987787]</span></span>  

### <span data-ttu-id="92bc9-154">Extensiones de código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="92bc9-154">Visual Studio Code extensions</span></span>  

<span data-ttu-id="92bc9-155">El equipo de DevTools también ha publicado algunas extensiones para [código Visual Studio][VisualStudioCode] que te permiten usar la potencia de DevTools directamente desde tu editor de texto.</span><span class="sxs-lookup"><span data-stu-id="92bc9-155">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="92bc9-156">Consulta las siguientes extensiones:</span><span class="sxs-lookup"><span data-stu-id="92bc9-156">Check out the extensions below:</span></span>  

#### <span data-ttu-id="92bc9-157">Elementos de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="92bc9-157">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="92bc9-158">Use la herramienta elementos de Visual Studio para agregar los elementos de la extensión de código de Visual Studio [Microsoft Edge \ (cromo \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] .</span><span class="sxs-lookup"><span data-stu-id="92bc9-158">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="La herramienta elementos en Visual Studio código que usa los elementos de la extensión de Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   <span data-ttu-id="92bc9-160">La herramienta **elementos** en Visual Studio código que usa los elementos de la extensión de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="92bc9-160">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-161">Para obtener más información, consulta [los elementos de la extensión de código de Microsoft Edge Visual Studio][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="92bc9-161">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="92bc9-162">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="92bc9-162">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="92bc9-163">Con el [depurador de la extensión de código de Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio, depura JavaScript ejecutándose directamente en Microsoft Edge desde el código de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="92bc9-163">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="El depurador para la extensión de Microsoft Edge en Visual Studio Code" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   <span data-ttu-id="92bc9-165">El depurador para la extensión de Microsoft Edge en Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="92bc9-165">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-166">Para obtener más información, consulte [Cómo depurar Microsoft Edge desde código de Visual Studio][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="92bc9-166">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="92bc9-167">webhint</span><span class="sxs-lookup"><span data-stu-id="92bc9-167">webhint</span></span>  

<span data-ttu-id="92bc9-168">La extensión de código [webhint][VisualStudioMarketplaceWebhintExtension] de Visual Studio usa `webhint` para mejorar la página web mientras estás escribiendo.</span><span class="sxs-lookup"><span data-stu-id="92bc9-168">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="92bc9-169">Esta extensión ejecuta y notifica diagnósticos en los archivos de área de trabajo según el `webhint` análisis.</span><span class="sxs-lookup"><span data-stu-id="92bc9-169">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="Extensión de código webhint de Visual Studio que analiza un archivo. TSX en código de Visual Studio" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="92bc9-171">Extensión de código webhint de Visual Studio que analiza un `.tsx` archivo en código Visual Studio</span><span class="sxs-lookup"><span data-stu-id="92bc9-171">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-172">[Más información sobre la extensión webhint de Visual Studio Code][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="92bc9-172">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="92bc9-173">Integración con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="92bc9-173">Visual Studio integration</span></span>  

<span data-ttu-id="92bc9-174">En Visual Studio 2019 versión 16,2 o posterior, usa el depurador de Visual Studio para depurar JavaScript que se ejecuta en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="92bc9-174">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="92bc9-175">[Descarga Visual Studio 2019][MicrosoftVisualStudioDownloads] para probar esta característica.</span><span class="sxs-lookup"><span data-stu-id="92bc9-175">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta" lightbox="../../images/2020/01/vs.msft.png":::
   <span data-ttu-id="92bc9-177">Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta</span><span class="sxs-lookup"><span data-stu-id="92bc9-177">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-178">[Obtenga más información sobre la depuración de Microsoft Edge desde Visual Studio][MicrosoftVisualStudio].</span><span class="sxs-lookup"><span data-stu-id="92bc9-178">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <span data-ttu-id="92bc9-179">Mensajes de la consola de prevención de seguimiento</span><span class="sxs-lookup"><span data-stu-id="92bc9-179">Tracking prevention Console messages</span></span>  

<span data-ttu-id="92bc9-180">La prevención de seguimiento es una característica exclusiva de Microsoft Edge que le protege de ser rastreada por los sitios web que no ha visitado antes.</span><span class="sxs-lookup"><span data-stu-id="92bc9-180">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="92bc9-181">La configuración predeterminada de prevención de rastreo es el modo equilibrado, que bloquea los rastreadores de terceros y los rastreadores maliciosos conocidos para obtener una experiencia que equilibre la compatibilidad de la privacidad y la Web.</span><span class="sxs-lookup"><span data-stu-id="92bc9-181">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="92bc9-182">Para obtener más información sobre la compatibilidad de su página web cuando se bloquean determinados rastreadores, también hemos añadido mensajes de advertencia en la consola cuando se bloquea un rastreador.</span><span class="sxs-lookup"><span data-stu-id="92bc9-182">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Mensajes en la consola cuando el seguimiento de prevención bloquea el acceso al almacenamiento de un rastreador" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   <span data-ttu-id="92bc9-184">Mensajes en la consola cuando el seguimiento de prevención bloquea el acceso al almacenamiento de un rastreador</span><span class="sxs-lookup"><span data-stu-id="92bc9-184">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-185">[Obtenga más información acerca de la prevención de seguimiento y el equilibrio entre privacidad y compatibilidad web][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="92bc9-185">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="92bc9-186">Anuncios del proyecto de cromo</span><span class="sxs-lookup"><span data-stu-id="92bc9-186">Announcements from the Chromium project</span></span>  

<span data-ttu-id="92bc9-187">En las siguientes secciones se anuncian características adicionales disponibles en Microsoft Edge 81 que se han contribuido al proyecto de código abierto.</span><span class="sxs-lookup"><span data-stu-id="92bc9-187">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="92bc9-188">Compatibilidad de moto G4 en el modo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="92bc9-188">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="92bc9-189">Después de [Habilitar la barra de herramientas del dispositivo][DeviceToolbar], simule las dimensiones de una ventanilla de moto G4 en la lista de **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="92bc9-189">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulación de una ventanilla de moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   <span data-ttu-id="92bc9-191">Simulación de una ventanilla de moto G4</span><span class="sxs-lookup"><span data-stu-id="92bc9-191">Simulating a Moto G4 viewport</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-192">Haga clic en [Mostrar marco del dispositivo][DeviceFrame] para mostrar el hardware de moto G4 en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="92bc9-192">Click [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Mostrar el hardware de moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   <span data-ttu-id="92bc9-194">Mostrar el hardware de moto G4</span><span class="sxs-lookup"><span data-stu-id="92bc9-194">Showing the Moto G4 hardware</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-195">Características relacionadas:</span><span class="sxs-lookup"><span data-stu-id="92bc9-195">Related features:</span></span>  

*   <span data-ttu-id="92bc9-196">Abra el [menú de comandos][CommandMenu] y ejecute el `Capture screenshot` comando para tomar una captura de pantalla de la ventanilla que incluye el hardware moto G4 (después de habilitar **Mostrar marco de dispositivo**).</span><span class="sxs-lookup"><span data-stu-id="92bc9-196">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="92bc9-197">[Limite la red y la CPU][ThrottleNetworkAndCpu] para simular de forma más precisa las condiciones de navegación web de un usuario móvil.</span><span class="sxs-lookup"><span data-stu-id="92bc9-197">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="92bc9-198">[#924693][CR924693] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="92bc9-198">Chromium issue [#924693][CR924693]</span></span>  

### <span data-ttu-id="92bc9-199">Actualizaciones relacionadas con cookies</span><span class="sxs-lookup"><span data-stu-id="92bc9-199">Cookie-related updates</span></span>  

#### <span data-ttu-id="92bc9-200">Cookies bloqueados en el panel cookies</span><span class="sxs-lookup"><span data-stu-id="92bc9-200">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="92bc9-201">El panel cookies en el panel de la aplicación ahora muestra las cookies bloqueadas con un fondo amarillo.</span><span class="sxs-lookup"><span data-stu-id="92bc9-201">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqueados en el panel de cookies del panel de aplicaciones" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   <span data-ttu-id="92bc9-203">Cookies bloqueados en el panel de cookies del panel de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="92bc9-203">Blocked cookies in the Cookies pane of the Application panel</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-204">[#1030258][CR1030258] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="92bc9-204">Chromium issue [#1030258][CR1030258]</span></span>  <!-- inaccessible  -->  

#### <span data-ttu-id="92bc9-205">Prioridad de la cookie en el panel de cookies</span><span class="sxs-lookup"><span data-stu-id="92bc9-205">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="92bc9-206">Las tablas de cookies de los paneles red y aplicación ahora incluyen una columna de **prioridad** .</span><span class="sxs-lookup"><span data-stu-id="92bc9-206">The Cookies tables in the Network and Application panels now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="92bc9-207">Los exploradores basados en cromo, como Microsoft Edge, son los únicos exploradores que admiten la prioridad de las cookies.</span><span class="sxs-lookup"><span data-stu-id="92bc9-207">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="92bc9-208">[#1026879][CR1026879] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="92bc9-208">Chromium issue [#1026879][CR1026879]</span></span>  

#### <span data-ttu-id="92bc9-209">Editar todos los valores de cookies</span><span class="sxs-lookup"><span data-stu-id="92bc9-209">Edit all cookie values</span></span>  

<span data-ttu-id="92bc9-210">Ahora todas las celdas de las tablas de cookies se pueden editar, excepto las celdas de la columna **tamaño** , porque esa columna representa el tamaño de red de la cookie, en bytes.</span><span class="sxs-lookup"><span data-stu-id="92bc9-210">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="92bc9-211">Vea [los campos][CookiesFields] para obtener una explicación de cada columna.</span><span class="sxs-lookup"><span data-stu-id="92bc9-211">See [Fields][CookiesFields] for an explanation of each column.</span></span>  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Editar un valor de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   <span data-ttu-id="92bc9-213">Editar un valor de cookie</span><span class="sxs-lookup"><span data-stu-id="92bc9-213">Editing a cookie value</span></span>  
:::image-end:::  

#### <span data-ttu-id="92bc9-214">Copiar como Node.js fetch para incluir datos de cookies</span><span class="sxs-lookup"><span data-stu-id="92bc9-214">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="92bc9-215">Haga clic con el botón secundario en una solicitud de red y seleccione **copiar**  >  **copia como Node.js fetch** para obtener una `fetch` expresión que incluya datos de cookies.</span><span class="sxs-lookup"><span data-stu-id="92bc9-215">Right-click a network request and select **Copy** > **Copy as Node.js fetch** to get a `fetch` expression that includes cookie data.</span></span>  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copiar como captura de Node.js" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   <span data-ttu-id="92bc9-217">Copiar como captura de Node.js</span><span class="sxs-lookup"><span data-stu-id="92bc9-217">Copy as Node.js fetch</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-218">[#1029826][CR1029826] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="92bc9-218">Chromium issue [#1029826][CR1029826]</span></span>  

### <span data-ttu-id="92bc9-219">Iconos más exactos del manifiesto de la aplicación Web</span><span class="sxs-lookup"><span data-stu-id="92bc9-219">More accurate web app manifest icons</span></span>  

<span data-ttu-id="92bc9-220">Anteriormente, el panel manifiesto del panel de aplicaciones enviaba sus propias solicitudes para mostrar los iconos del manifiesto de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="92bc9-220">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="92bc9-221">DevTools ahora muestra el mismo icono de manifiesto que usa Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="92bc9-221">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Iconos en el panel manifiesto" lightbox="../../images/2020/01/manifesticons.msft.png":::
   <span data-ttu-id="92bc9-223">Iconos en el panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="92bc9-223">Icons in the Manifest pane</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-224">[#985402][CR985402] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="92bc9-224">Chromium issue [#985402][CR985402]</span></span>  

### <span data-ttu-id="92bc9-225">Mantenga el mouse sobre las propiedades de contenido CSS para ver valores sin escape</span><span class="sxs-lookup"><span data-stu-id="92bc9-225">Hover over CSS content properties to see unescaped values</span></span>  

<span data-ttu-id="92bc9-226">Desplace el puntero sobre el valor de una `content` propiedad para ver la versión sin escape del valor.</span><span class="sxs-lookup"><span data-stu-id="92bc9-226">Hover over the value of a `content` property to see the unescaped version of the value.</span></span>  

<span data-ttu-id="92bc9-227">Por ejemplo, en esta [demostración][CSSContentDemo] , cuando Inspeccione el `p::after` seudoelemento, verá una cadena de escape en el panel Estilos:</span><span class="sxs-lookup"><span data-stu-id="92bc9-227">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element you see an escaped string in the Styles pane:</span></span>  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="La cadena de escape" lightbox="../../images/2020/01/escapedstring.msft.png":::
   <span data-ttu-id="92bc9-229">La cadena de escape</span><span class="sxs-lookup"><span data-stu-id="92bc9-229">The escaped string</span></span>  
:::image-end:::  

<span data-ttu-id="92bc9-230">Cuando pasa el puntero sobre el `content` valor, Ve el valor unescape:</span><span class="sxs-lookup"><span data-stu-id="92bc9-230">When you hover over the `content` value you see the unescaped value:</span></span>  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="Valor sin escape" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   <span data-ttu-id="92bc9-232">Valor sin escape</span><span class="sxs-lookup"><span data-stu-id="92bc9-232">The unescaped value</span></span>  
:::image-end:::  

### <span data-ttu-id="92bc9-233">Errores de mapas de origen más detallados en la consola</span><span class="sxs-lookup"><span data-stu-id="92bc9-233">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="92bc9-234">La consola ahora proporciona más información sobre por qué no se pudo cargar o analizar un mapa de origen.</span><span class="sxs-lookup"><span data-stu-id="92bc9-234">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="92bc9-235">Anteriormente, se ha proporcionado un error sin explicar qué falló.</span><span class="sxs-lookup"><span data-stu-id="92bc9-235">Previously it just provided an error without explaining what went wrong.</span></span>  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Un error de carga del mapa de origen en la consola" lightbox="../../images/2020/01/sourcemap.msft.png":::
   <span data-ttu-id="92bc9-237">Un error de carga del mapa de origen en la consola</span><span class="sxs-lookup"><span data-stu-id="92bc9-237">A source map loading error in the Console</span></span>  
:::image-end:::  

### <span data-ttu-id="92bc9-238">Configuración para deshabilitar el desplazamiento más allá del final de un archivo</span><span class="sxs-lookup"><span data-stu-id="92bc9-238">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="92bc9-239">Abrir [configuración][Settings] y deshabilitar **preferencias**  >  **orígenes**:  >  **permite desplazarse más allá del final del archivo** para deshabilitar el comportamiento predeterminado de la interfaz de usuario que permite desplazarse hasta el final de un archivo en el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="92bc9-239">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Deshabilitar la opción permitir el desplazamiento más allá del final del archivo" lightbox="../../images/2020/01/settings.msft.png":::
   <span data-ttu-id="92bc9-241">Deshabilitar la **opción permitir el desplazamiento más allá del final del archivo** en configuración</span><span class="sxs-lookup"><span data-stu-id="92bc9-241">Disabling **Allow scrolling past end of file** in Settings</span></span>  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="El desplazamiento más allá del final de un archivo ya está deshabilitado en el panel orígenes" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   <span data-ttu-id="92bc9-243">El desplazamiento más allá del final de un archivo ya está deshabilitado en el panel orígenes</span><span class="sxs-lookup"><span data-stu-id="92bc9-243">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
:::image-end:::  

## <span data-ttu-id="92bc9-244">Descargar los canales de Microsoft Edge Preview</span><span class="sxs-lookup"><span data-stu-id="92bc9-244">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="92bc9-245">Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="92bc9-245">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="92bc9-246">Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="92bc9-246">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="92bc9-247">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="92bc9-247">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular un área de visualización móvil: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft docs"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Mostrar fotograma de dispositivo: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft docs"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Limitar la red y la CPU: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft docs"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración-personalizar Microsoft Edge DevTools | Microsoft docs"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Microsoft docs"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Campos: ver, editar y eliminar cookies con Microsoft Edge DevTools | Microsoft docs"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Depurador para la extensión de código de Microsoft Edge Visual Studio"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Elementos de la extensión de código de Microsoft Edge Visual Studio"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canales de Microsoft Edge Preview"  

[VisualStudioCode]: https://aka.ms/vscode "Código de Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge-Marketplace de Visual Studio"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos de Microsoft Edge \ (cromo \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-catálogo de soluciones de Visual Studio"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Mejorar la prevención de seguimiento en la entrada de blog de Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Complementos de Insider de Microsoft Edge"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Descargar Visual Studio 2019 para Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publicar un tweet"  

[CR924693]: https://crbug.com/924693 "Solicitud de característica: agregar moto G4 a la lista de modos de dispositivo | Errores de cromo"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Errores de cromo"  
[CR1026879]: https://crbug.com/1026879 "La pestaña cookie en la consola de desarrollo ya no muestra la prioridad | Errores de cromo"  
[CR1029826]: https://crbug.com/1029826 "ficha red: > clic con el botón secundario para solicitar > copiar-> copia como fetch no copia cookies | Errores de cromo"  
[CR985402]: https://crbug.com/985402 "las cadenas de error del manifiesto de la aplicación web son confusas | Errores de cromo"  
[CR963183]: https://crbug.com/963183 "DevTools no son compatibles con WCAG | Errores de cromo"  
[CR941561]: https://crbug.com/941561 "Localizabilidad de la DevTools | Errores de cromo"  
[CR987787]: https://crbug.com/987787 "Vista 3D de Dom | Errores de cromo"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demostración de contenido CSS sin escape"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nuevo problema: MicrosoftDocs/Edge-Developer"  

[TheWebWeWant]: https://aka.ms/webwewant "La web que queremos"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Información de accesibilidad"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objetos de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "índice z | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools cuenta de Twitter"  

[Webhint]: https://aka.ms/webhint "sugerencia"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extensión de explorador webhint | documentación de webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Extensión de código webhint de Visual Studio | documentación de webhint"  

> [!NOTE]
> <span data-ttu-id="92bc9-284">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="92bc9-284">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="92bc9-285">La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/01/devtools/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="92bc9-285">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="92bc9-287">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="92bc9-287">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
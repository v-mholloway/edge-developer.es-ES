---
title: Novedades de DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6de8f7b11edb476f2656dd6f16e02413b1873ed8
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684716"
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







# <span data-ttu-id="b082e-103">Novedades de DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="b082e-103">What's New In DevTools (Microsoft Edge 81)</span></span>   



## <span data-ttu-id="b082e-104">Anuncios del equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b082e-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="b082e-105">Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo de DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b082e-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="b082e-106">Compruébelos para probar las nuevas características de la DevTools, las extensiones de código de VS y mucho más.</span><span class="sxs-lookup"><span data-stu-id="b082e-106">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="b082e-107">Para mantenerte al tanto de las últimas y mejores características de las herramientas para desarrolladores, descarga los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] y mantente [en Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="b082e-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="b082e-108">Mejoras de accesibilidad para el DevTools</span><span class="sxs-lookup"><span data-stu-id="b082e-108">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="b082e-109">El equipo de DevTools ha contribuido a 170 cambios en cromo para solucionar problemas de alto impacto en el contraste de color, el teclado y el lector de pantalla en el DevTools.</span><span class="sxs-lookup"><span data-stu-id="b082e-109">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="b082e-110">Cada desarrollador que crea la web debe poder usar el DevTools.</span><span class="sxs-lookup"><span data-stu-id="b082e-110">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="b082e-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="b082e-111">Figure 1</span></span>  
> <span data-ttu-id="b082e-112">La herramienta de rendimiento en el DevTools con la navegación con el teclado y las mejoras del lector de pantalla</span><span class="sxs-lookup"><span data-stu-id="b082e-112">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![La herramienta de rendimiento en el DevTools con la navegación con el teclado y las mejoras del lector de pantalla][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="b082e-114">¿Desea saber cómo hacer que su página web sea accesible para todos los usuarios?</span><span class="sxs-lookup"><span data-stu-id="b082e-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="b082e-115">Descargue [Insight Insights][AccessibilityInsights] y extensiones [Webhint][WebhintBrowserExtension] para Microsoft Edge para comenzar.</span><span class="sxs-lookup"><span data-stu-id="b082e-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="b082e-116">Si usa lectores de pantalla o el teclado para desplazarse por la DevTools, envíenos sus comentarios con un [Tweet][PostTweetEdgeDevTools] o haga clic en el icono de [comentarios](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="b082e-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="b082e-117">[#963183][crbug963183] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b082e-117">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="b082e-118">Usar el DevTools en otros idiomas</span><span class="sxs-lookup"><span data-stu-id="b082e-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="b082e-119">Muchos programadores usan otras herramientas de desarrollo, como StackOverflow y VS Code, en su idioma nativo, no solo en inglés.</span><span class="sxs-lookup"><span data-stu-id="b082e-119">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="b082e-120">Nos complace anunciar la localización de la DevTools, que ahora puedes usar en uno de los 10 idiomas además del inglés:</span><span class="sxs-lookup"><span data-stu-id="b082e-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b082e-121">Chino \ (simplificado \)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="b082e-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b082e-122">Chino (tradicional \)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="b082e-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="b082e-123">Francés: Francisco&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="b082e-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b082e-124">Alemán-Deutsch</span><span class="sxs-lookup"><span data-stu-id="b082e-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="b082e-125">Italiano-Italiano</span><span class="sxs-lookup"><span data-stu-id="b082e-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b082e-126"> &#26085;&#26412;&#35486; japonés</span><span class="sxs-lookup"><span data-stu-id="b082e-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="b082e-127">Coreano:  &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="b082e-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b082e-128">Portugués-Portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="b082e-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="b082e-129">Ruso:  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="b082e-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b082e-130">Español-Espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="b082e-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="b082e-131">El DevTools coincide automáticamente con el idioma que usas para Microsoft Edge en `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="b082e-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="b082e-132">Si desea que Microsoft Edge esté en un idioma y que su DevTools permanezca en inglés, presione `F1` la DevTools para abrir la [configuración][Settings] y deshabilitar el **idioma del explorador**.</span><span class="sxs-lookup"><span data-stu-id="b082e-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, press `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

> ##### <span data-ttu-id="b082e-133">Figura 2</span><span class="sxs-lookup"><span data-stu-id="b082e-133">Figure 2</span></span>  
> <span data-ttu-id="b082e-134">El DevTools en alemán</span><span class="sxs-lookup"><span data-stu-id="b082e-134">The DevTools in German</span></span>  
> ![El DevTools en alemán][ImageLocalizedGerman]  

<span data-ttu-id="b082e-136">Los mensajes de **consola** no se localizan.</span><span class="sxs-lookup"><span data-stu-id="b082e-136">**Console** messages are not localized.</span></span>  <span data-ttu-id="b082e-137">Solo las cadenas usadas en la interfaz de usuario de DevTools se muestran en el idioma que usas para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b082e-137">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="b082e-138">Si desea usar la DevTools en un idioma diferente al de los que están disponibles, [Tweet][PostTweetEdgeDevTools] o haga clic en el icono de [comentarios](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="b082e-138">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Feedback](#feedback) icon.</span></span>  

<span data-ttu-id="b082e-139">[#941561][crbug941561] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b082e-139">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="b082e-140">extensión webhint de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b082e-140">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="b082e-141">La extensión webhint de Microsoft Edge te permite examinar fácilmente tu página web y obtener comentarios sobre la accesibilidad, la compatibilidad de explorador, la seguridad, el rendimiento y mucho más dentro de la DevTools.</span><span class="sxs-lookup"><span data-stu-id="b082e-141">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="b082e-142">Para obtener más información, consulte [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="b082e-142">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="b082e-143">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="b082e-143">Figure 3</span></span>  
> <span data-ttu-id="b082e-144">La pestaña sugerencias de la DevTools cuando está instalada la extensión de explorador webhint</span><span class="sxs-lookup"><span data-stu-id="b082e-144">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![La pestaña sugerencias de la DevTools cuando está instalada la extensión de explorador webhint][ImageHintsTabWebhintExtension]  

<span data-ttu-id="b082e-146">[Prueba la extensión de explorador webhint en Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="b082e-146">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="b082e-147">Una vez que haya instalado la extensión, abra el DevTools y seleccione la pestaña sugerencias.  Desde aquí, ejecute un examen de sitios personalizable.</span><span class="sxs-lookup"><span data-stu-id="b082e-147">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="b082e-148">Visita [webhint.IO][WebhintBrowserExtension] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b082e-148">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <span data-ttu-id="b082e-149">Vista 3D</span><span class="sxs-lookup"><span data-stu-id="b082e-149">3D View</span></span>  

<span data-ttu-id="b082e-150">Use la **vista 3D** para depurar la aplicación web desplazándose por el [modelo de objeto de documento \ (Dom \)][MDNDocumentObjectModel] o el contexto de apilamiento [de índice z][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="b082e-150">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="b082e-151">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="b082e-151">Figure 4</span></span>  
> <span data-ttu-id="b082e-152">Vista 3D en el DevTools</span><span class="sxs-lookup"><span data-stu-id="b082e-152">The 3D View in the DevTools</span></span>  
> ![Vista 3D en el DevTools][Image3DView]  

<span data-ttu-id="b082e-154">Para acceder a la vista 3D, pulse `Ctrl`  +  `Shift`  +  `P` , escriba en la **vista 3D** y seleccione **Mostrar vista en 3D**.</span><span class="sxs-lookup"><span data-stu-id="b082e-154">To access the 3D View, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="b082e-155">Trabajamos en la interfaz de usuario y agregamos más funcionalidad a la vista 3D; por lo tanto, envíanos tus [comentarios](#feedback).</span><span class="sxs-lookup"><span data-stu-id="b082e-155">We're working on the UI and adding more functionality to the 3D View, so please send us your [feedback](#feedback).</span></span>  

<span data-ttu-id="b082e-156">[#987787][crbug987787] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b082e-156">Chromium issue [#987787][crbug987787]</span></span>  

### <span data-ttu-id="b082e-157">Extensiones de código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b082e-157">Visual Studio Code extensions</span></span>  

<span data-ttu-id="b082e-158">El equipo de DevTools también ha publicado algunas extensiones para [Visual Studio Code \ (vs Code \)][VisualStudioCode] que te permiten usar la potencia de DevTools directamente desde tu editor de texto.</span><span class="sxs-lookup"><span data-stu-id="b082e-158">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="b082e-159">Consulta las siguientes extensiones:</span><span class="sxs-lookup"><span data-stu-id="b082e-159">Check out the extensions below:</span></span>  

#### <span data-ttu-id="b082e-160">Elementos de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b082e-160">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="b082e-161">Use la herramienta elementos de VS Code agregando los [elementos de la extensión de código de Microsoft Edge \ (cromo \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] .</span><span class="sxs-lookup"><span data-stu-id="b082e-161">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="b082e-162">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="b082e-162">Figure 5</span></span>  
> <span data-ttu-id="b082e-163">La herramienta elementos en VS Code uso de los elementos de la extensión de Microsoft Edge ![ la herramienta elementos en vs Code usando los elementos de la extensión de Microsoft Edge][ImageElementsVisualStudioCode]</span><span class="sxs-lookup"><span data-stu-id="b082e-163">The Elements tool in VS Code using the Elements for Microsoft Edge extension ![The Elements tool in VS Code using the Elements for Microsoft Edge extension][ImageElementsVisualStudioCode]</span></span>  

<span data-ttu-id="b082e-164">Para obtener más información, consulta [los elementos de la extensión de código de Microsoft Edge vs][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="b082e-164">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="b082e-165">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b082e-165">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="b082e-166">Con el [depurador para la extensión de código de Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] vs, depure JavaScript que se ejecuta en Microsoft Edge directamente desde el código de vs.</span><span class="sxs-lookup"><span data-stu-id="b082e-166">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="b082e-167">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="b082e-167">Figure 6</span></span>  
> <span data-ttu-id="b082e-168">El depurador para la extensión de Microsoft Edge en VS Code</span><span class="sxs-lookup"><span data-stu-id="b082e-168">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![El depurador para la extensión de Microsoft Edge en VS Code][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="b082e-170">Para obtener más información, consulte [Cómo depurar Microsoft Edge desde vs Code][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="b082e-170">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="b082e-171">sugerencia</span><span class="sxs-lookup"><span data-stu-id="b082e-171">webhint</span></span>  

<span data-ttu-id="b082e-172">La extensión de código [webhint][VisualStudioMarketplaceWebhintExtension] de vs usa `webhint` para mejorar la página web mientras la escribes.</span><span class="sxs-lookup"><span data-stu-id="b082e-172">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="b082e-173">Esta extensión ejecuta y notifica diagnósticos en los archivos de área de trabajo según el `webhint` análisis.</span><span class="sxs-lookup"><span data-stu-id="b082e-173">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="b082e-174">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="b082e-174">Figure 7</span></span>  
> <span data-ttu-id="b082e-175">La extensión de código de webhint VS analizando un archivo. TSX en VS Code</span><span class="sxs-lookup"><span data-stu-id="b082e-175">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![La extensión de código de webhint VS analizando un archivo. TSX en VS Code][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="b082e-177">[Más información sobre la extensión webhint de vs Code][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="b082e-177">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="b082e-178">Integración con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b082e-178">Visual Studio integration</span></span>  

<span data-ttu-id="b082e-179">En Visual Studio 2019 versión 16,2 o posterior, usa el depurador de Visual Studio para depurar JavaScript que se ejecuta en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b082e-179">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="b082e-180">[Descarga Visual Studio 2019][MicrosoftVisualStudioDownloads] para probar esta característica.</span><span class="sxs-lookup"><span data-stu-id="b082e-180">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="b082e-181">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="b082e-181">Figure 8</span></span>  
> <span data-ttu-id="b082e-182">Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta</span><span class="sxs-lookup"><span data-stu-id="b082e-182">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="b082e-184">[Obtenga más información sobre la depuración de Microsoft Edge desde Visual Studio][MicrosoftVisualStudio].</span><span class="sxs-lookup"><span data-stu-id="b082e-184">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <span data-ttu-id="b082e-185">Mensajes de la consola de prevención de seguimiento</span><span class="sxs-lookup"><span data-stu-id="b082e-185">Tracking prevention Console messages</span></span>  

<span data-ttu-id="b082e-186">La prevención de seguimiento es una característica exclusiva de Microsoft Edge que le protege de ser rastreada por los sitios web que no ha visitado antes.</span><span class="sxs-lookup"><span data-stu-id="b082e-186">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="b082e-187">La configuración predeterminada de prevención de rastreo es el modo equilibrado, que bloquea los rastreadores de terceros y los rastreadores maliciosos conocidos para obtener una experiencia que equilibre la compatibilidad de la privacidad y la Web.</span><span class="sxs-lookup"><span data-stu-id="b082e-187">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="b082e-188">Para obtener más información sobre la compatibilidad de su página web cuando se bloquean determinados rastreadores, también hemos añadido mensajes de advertencia en la consola cuando se bloquea un rastreador.</span><span class="sxs-lookup"><span data-stu-id="b082e-188">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="b082e-189">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="b082e-189">Figure 9</span></span>  
> <span data-ttu-id="b082e-190">Mensajes en la consola cuando el seguimiento de prevención bloquea el acceso al almacenamiento de un rastreador</span><span class="sxs-lookup"><span data-stu-id="b082e-190">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Mensajes en la consola cuando el seguimiento de prevención bloquea el acceso al almacenamiento de un rastreador][ImageTrackingPrevention]  

<span data-ttu-id="b082e-192">[Obtenga más información acerca de la prevención de seguimiento y el equilibrio entre privacidad y compatibilidad web][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="b082e-192">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>



## <span data-ttu-id="b082e-193">Anuncios del proyecto de cromo</span><span class="sxs-lookup"><span data-stu-id="b082e-193">Announcements from the Chromium project</span></span>  

<span data-ttu-id="b082e-194">En las siguientes secciones se anuncian características adicionales disponibles en Microsoft Edge 81 que se han contribuido al proyecto de código abierto.</span><span class="sxs-lookup"><span data-stu-id="b082e-194">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="b082e-195">Compatibilidad de moto G4 en el modo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b082e-195">Moto G4 support in Device Mode</span></span> 

<span data-ttu-id="b082e-196">Después de [Habilitar la barra de herramientas del dispositivo][DeviceToolbar], simule las dimensiones de una ventanilla de moto G4 en la lista de **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="b082e-196">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

> ##### <span data-ttu-id="b082e-197">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="b082e-197">Figure 10</span></span>  
> <span data-ttu-id="b082e-198">Simulación de una ventanilla de moto G4</span><span class="sxs-lookup"><span data-stu-id="b082e-198">Simulating a Moto G4 viewport</span></span>  
> ![Simulación de una ventanilla de moto G4][ImageMotoG4]  

<span data-ttu-id="b082e-200">Haga clic en [Mostrar marco del dispositivo][DeviceFrame] para mostrar el hardware de moto G4 en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="b082e-200">Click [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

> ##### <span data-ttu-id="b082e-201">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="b082e-201">Figure 11</span></span>  
> <span data-ttu-id="b082e-202">Mostrar el hardware de moto G4</span><span class="sxs-lookup"><span data-stu-id="b082e-202">Showing the Moto G4 hardware</span></span>  
> ![Mostrar el hardware de moto G4][ImageMotoG4Frame]  

<span data-ttu-id="b082e-204">Características relacionadas:</span><span class="sxs-lookup"><span data-stu-id="b082e-204">Related features:</span></span>  

*   <span data-ttu-id="b082e-205">Abra el [menú de comandos][CommandMenu] y ejecute el `Capture screenshot` comando para tomar una captura de pantalla de la ventanilla que incluye el hardware moto G4 (después de habilitar **Mostrar marco de dispositivo**).</span><span class="sxs-lookup"><span data-stu-id="b082e-205">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="b082e-206">[Limite la red y la CPU][ThrottleNetworkAndCpu] para simular de forma más precisa las condiciones de navegación web de un usuario móvil.</span><span class="sxs-lookup"><span data-stu-id="b082e-206">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="b082e-207">[#924693][crbug924693] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b082e-207">Chromium issue [#924693][crbug924693]</span></span>  

### <span data-ttu-id="b082e-208">Actualizaciones relacionadas con cookies</span><span class="sxs-lookup"><span data-stu-id="b082e-208">Cookie-related updates</span></span>   

#### <span data-ttu-id="b082e-209">Cookies bloqueados en el panel cookies</span><span class="sxs-lookup"><span data-stu-id="b082e-209">Blocked cookies in the Cookies pane</span></span>   

<span data-ttu-id="b082e-210">El panel cookies en el panel de la aplicación ahora muestra las cookies bloqueadas con un fondo amarillo.</span><span class="sxs-lookup"><span data-stu-id="b082e-210">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

> ##### <span data-ttu-id="b082e-211">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="b082e-211">Figure 12</span></span>  
> <span data-ttu-id="b082e-212">Cookies bloqueados en el panel de cookies del panel de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b082e-212">Blocked cookies in the Cookies pane of the Application panel</span></span>  
> ![Cookies bloqueados en el panel de cookies del panel de aplicaciones][ImageBlockedCookies]  

<span data-ttu-id="b082e-214">[#1030258][crbug|::ref1::|] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b082e-214">Chromium issue [#1030258][crbug|::ref1::|]</span></span>  

#### <span data-ttu-id="b082e-215">Prioridad de la cookie en el panel de cookies</span><span class="sxs-lookup"><span data-stu-id="b082e-215">Cookie priority in the Cookie pane</span></span>   

<span data-ttu-id="b082e-216">Las tablas de cookies de los paneles red y aplicación ahora incluyen una columna de **prioridad** .</span><span class="sxs-lookup"><span data-stu-id="b082e-216">The Cookies tables in the Network and Application panels now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="b082e-217">Los exploradores basados en cromo, como Microsoft Edge, son los únicos exploradores que admiten la prioridad de las cookies.</span><span class="sxs-lookup"><span data-stu-id="b082e-217">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="b082e-218">[#1026879][crbug1026879] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b082e-218">Chromium issue [#1026879][crbug1026879]</span></span>  

#### <span data-ttu-id="b082e-219">Editar todos los valores de cookies</span><span class="sxs-lookup"><span data-stu-id="b082e-219">Edit all cookie values</span></span>   

<span data-ttu-id="b082e-220">Ahora todas las celdas de las tablas de cookies se pueden editar, excepto las celdas de la columna **tamaño** , porque esa columna representa el tamaño de red de la cookie, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b082e-220">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="b082e-221">Vea [los campos][CookiesFields] para obtener una explicación de cada columna.</span><span class="sxs-lookup"><span data-stu-id="b082e-221">See [Fields][CookiesFields] for an explanation of each column.</span></span>  

> ##### <span data-ttu-id="b082e-222">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="b082e-222">Figure 13</span></span>  
> <span data-ttu-id="b082e-223">Editar un valor de cookie</span><span class="sxs-lookup"><span data-stu-id="b082e-223">Editing a cookie value</span></span>  
> ![Editar un valor de cookie][ImageEditCookie]  

#### <span data-ttu-id="b082e-225">Copiar como la búsqueda de node. js para incluir datos de cookies</span><span class="sxs-lookup"><span data-stu-id="b082e-225">Copy as Node.js fetch to include cookie data</span></span>   

<span data-ttu-id="b082e-226">Haga clic con el botón derecho en una solicitud de red y seleccione **copiar**  >  **copia como nodo. js fetch** para obtener una `fetch` expresión que incluya datos de cookies.</span><span class="sxs-lookup"><span data-stu-id="b082e-226">Right-click a network request and select **Copy** > **Copy as Node.js fetch** to get a `fetch` expression that includes cookie data.</span></span>  

> ##### <span data-ttu-id="b082e-227">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="b082e-227">Figure 14</span></span>  
> <span data-ttu-id="b082e-228">Copiar como fetch de node. js</span><span class="sxs-lookup"><span data-stu-id="b082e-228">Copy as Node.js fetch</span></span>  
> ![Copiar como fetch de node. js][ImageCopyFetch]  

<span data-ttu-id="b082e-230">[#1029826][crbug1029826] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b082e-230">Chromium issue [#1029826][crbug1029826]</span></span>  

### <span data-ttu-id="b082e-231">Iconos más exactos del manifiesto de la aplicación Web</span><span class="sxs-lookup"><span data-stu-id="b082e-231">More accurate web app manifest icons</span></span>   

<span data-ttu-id="b082e-232">Anteriormente, el panel manifiesto del panel de aplicaciones enviaba sus propias solicitudes para mostrar los iconos del manifiesto de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="b082e-232">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="b082e-233">DevTools ahora muestra el mismo icono de manifiesto que usa Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b082e-233">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

> ##### <span data-ttu-id="b082e-234">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="b082e-234">Figure 15</span></span>  
> <span data-ttu-id="b082e-235">Iconos en el panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="b082e-235">Icons in the Manifest pane</span></span>  
> ![Iconos en el panel manifiesto][ImageManifestIcon]   

<span data-ttu-id="b082e-237">[#985402][crbug985402] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b082e-237">Chromium issue [#985402][crbug985402]</span></span>  

### <span data-ttu-id="b082e-238">Mantenga el mouse sobre las propiedades de contenido CSS para ver valores sin escape</span><span class="sxs-lookup"><span data-stu-id="b082e-238">Hover over CSS content properties to see unescaped values</span></span>   

<span data-ttu-id="b082e-239">Desplace el puntero sobre el valor de una `content` propiedad para ver la versión sin escape del valor.</span><span class="sxs-lookup"><span data-stu-id="b082e-239">Hover over the value of a `content` property to see the unescaped version of the value.</span></span>  

<span data-ttu-id="b082e-240">Por ejemplo, en esta [demostración][CSSContentDemo] , cuando Inspeccione el `p::after` seudoelemento, verá una cadena de escape en el panel Estilos:</span><span class="sxs-lookup"><span data-stu-id="b082e-240">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element you see an escaped string in the Styles pane:</span></span>  

> ##### <span data-ttu-id="b082e-241">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="b082e-241">Figure 16</span></span>  
> <span data-ttu-id="b082e-242">La cadena de escape</span><span class="sxs-lookup"><span data-stu-id="b082e-242">The escaped string</span></span>  
> ![La cadena de escape][ImageEscapedString]   

<span data-ttu-id="b082e-244">Cuando pasa el puntero sobre el `content` valor, Ve el valor unescape:</span><span class="sxs-lookup"><span data-stu-id="b082e-244">When you hover over the `content` value you see the unescaped value:</span></span>  

> ##### <span data-ttu-id="b082e-245">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="b082e-245">Figure 17</span></span>  
> <span data-ttu-id="b082e-246">Valor sin escape</span><span class="sxs-lookup"><span data-stu-id="b082e-246">The unescaped value</span></span>  
> ![Valor sin escape][ImageUnescapedString]   

### <span data-ttu-id="b082e-248">Errores de mapas de origen más detallados en la consola</span><span class="sxs-lookup"><span data-stu-id="b082e-248">More detailed source map errors in the Console</span></span>   

<span data-ttu-id="b082e-249">La consola ahora proporciona más información sobre por qué no se pudo cargar o analizar un mapa de origen.</span><span class="sxs-lookup"><span data-stu-id="b082e-249">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="b082e-250">Anteriormente, se ha proporcionado un error sin explicar qué falló.</span><span class="sxs-lookup"><span data-stu-id="b082e-250">Previously it just provided an error without explaining what went wrong.</span></span>  

> ##### <span data-ttu-id="b082e-251">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="b082e-251">Figure 18</span></span>  
> <span data-ttu-id="b082e-252">Un error de carga del mapa de origen en la consola</span><span class="sxs-lookup"><span data-stu-id="b082e-252">A source map loading error in the Console</span></span>  
> ![Un error de carga del mapa de origen en la consola][ImageSourcemapError]  

### <span data-ttu-id="b082e-254">Configuración para deshabilitar el desplazamiento más allá del final de un archivo</span><span class="sxs-lookup"><span data-stu-id="b082e-254">Setting for disabling scrolling past the end of a file</span></span>   

<span data-ttu-id="b082e-255">Abrir [configuración][Settings] y deshabilitar **preferencias**  >  **orígenes**:  >  **permite desplazarse más allá del final del archivo** para deshabilitar el comportamiento predeterminado de la interfaz de usuario que permite desplazarse hasta el final de un archivo en el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="b082e-255">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

> ##### <span data-ttu-id="b082e-256">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="b082e-256">Figure 19</span></span>  
> <span data-ttu-id="b082e-257">Deshabilitar la **opción permitir el desplazamiento más allá del final del archivo** en configuración</span><span class="sxs-lookup"><span data-stu-id="b082e-257">Disabling **Allow scrolling past end of file** in Settings</span></span>  
> ![Deshabilitar la opción permitir el desplazamiento más allá del final del archivo][ImageSettings]  

> ##### <span data-ttu-id="b082e-259">Ilustración 20</span><span class="sxs-lookup"><span data-stu-id="b082e-259">Figure 20</span></span>  
> <span data-ttu-id="b082e-260">El desplazamiento más allá del final de un archivo ya está deshabilitado en el panel orígenes</span><span class="sxs-lookup"><span data-stu-id="b082e-260">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
> ![El desplazamiento más allá del final de un archivo ya está deshabilitado en el panel orígenes][ImageScroll]  

## <span data-ttu-id="b082e-262">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b082e-262">Feedback</span></span>   



<span data-ttu-id="b082e-263">Para comentar las nuevas características y cambios de esta publicación, o cualquier otro tema relacionado con DevTools:</span><span class="sxs-lookup"><span data-stu-id="b082e-263">To discuss the new features and changes in this post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="b082e-264">Envíe sus comentarios con el icono de **comentarios** en el DevTools</span><span class="sxs-lookup"><span data-stu-id="b082e-264">Send your feedback using the **Feedback** icon in the DevTools</span></span>  

> ##### <span data-ttu-id="b082e-265">Ilustración 21</span><span class="sxs-lookup"><span data-stu-id="b082e-265">Figure 21</span></span>  
> <span data-ttu-id="b082e-266">El icono de **comentarios** en el DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b082e-266">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
> ![El icono \* \* comentarios \* \* en Microsoft Edge DevTools][ImageFeedbackIcon]  

*   <span data-ttu-id="b082e-268">Tweet a [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="b082e-268">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="b082e-269">Enviar una sugerencia a [la web][TheWebWeWant] que queremos</span><span class="sxs-lookup"><span data-stu-id="b082e-269">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="b082e-270">Archivar errores en este documento en el repositorio [Edge-desarrollador][GitHubMicrosoftDocsEdgeDeveloperNewIssue]</span><span class="sxs-lookup"><span data-stu-id="b082e-270">File bugs on this document in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

## <span data-ttu-id="b082e-271">Descargar los canales de Microsoft Edge Preview</span><span class="sxs-lookup"><span data-stu-id="b082e-271">Download the Microsoft Edge preview channels</span></span>   

<span data-ttu-id="b082e-272">Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b082e-272">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="b082e-273">Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b082e-273">The preview channels give you access to the latest DevTools features.</span></span>  

<!-- <<../../_shared/devtools-feedback.md>>

<<../../_shared/canary.md>>

<<../../_shared/discover.md>> -->



<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2020/01/a11y-performance-tool.msft.gif "Ilustración 1: la herramienta de rendimiento en DevTools con la navegación con el teclado y las mejoras del lector de pantalla"  
[ImageLocalizedGerman]: ../../images/2020/01/localized-devtools.msft.png "Ilustración 2: el DevTools en alemán"  
[ImageHintsTabWebhintExtension]: ../../images/2020/01/webhint-browser-extension.msft.png "Ilustración 3: la pestaña sugerencias en Microsoft Edge DevTools cuando la extensión de explorador webhint está instalada"  
[Image3DView]: ../../images/2020/01/3dview.msft.png "Ilustración 4: vista 3D en el DevTools de Microsoft Edge"  
[ImageElementsVisualStudioCode]: ../../images/2020/01/elements-for-edge.msft.png "Ilustración 5: la herramienta elementos en VS Code que usa los elementos de la extensión de Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2020/01/vscode-debugger.msft.png "Ilustración 6: el depurador para la extensión de Microsoft Edge en VS Code"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2020/01/webhint-vscode-extension.msft.png "Ilustración 7: la extensión de código webhint de VS analizando un archivo. TSX en VS Code"  
[ImageVisualStudioLaunchWebApp]: ../../images/2020/01/vs.msft.png "Ilustración 8: Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta"  
[ImageTrackingPrevention]: ../../images/2020/01/tracking-prevention.msft.png "Ilustración 9: mensajes en la consola cuando el control de prevención bloquea el acceso al almacenamiento de un rastreador" 
[ImageMotoG4]: ../../images/2020/01/motog4.msft.png "Ilustración 10: simular una ventanilla de moto G4" 
[ImageMotoG4Frame]: ../../images/2020/01/motog4frame.msft.png "Ilustración 11: mostrar el hardware de moto G4" 
[ImageBlockedCookies]: ../../images/2020/01/blockedcookies.msft.png "Ilustración 12: cookies bloqueadas en el panel de cookies del panel de aplicaciones"
[ImageEditCookie]: ../../images/2020/01/editcookie.msft.png "Ilustración 13: edición de un valor de cookie"
[ImageCopyFetch]: ../../images/2020/01/fetchcookies.msft.png "Ilustración 14: copiar como fetch de node. js"
[ImageManifestIcon]: ../../images/2020/01/manifesticons.msft.png "Ilustración 15: iconos en el panel manifiesto"
[ImageEscapedString]: ../../images/2020/01/escapedstring.msft.png "Ilustración 16: la cadena de escape"
[ImageUnescapedString]: ../../images/2020/01/unescapedstring.msft.png "Ilustración 17: el valor sin escape"
[ImageSourcemapError]: ../../images/2020/01/sourcemap.msft.png "Ilustración 18: un error de carga del mapa de origen en la consola"
[ImageSettings]: ../../images/2020/01/settings.msft.png "Ilustración 19: deshabilitar la opción permitir el desplazamiento más allá del final del archivo en configuración"
[ImageScroll]: ../../images/2020/01/scrollingsources.msft.png "Ilustración 20: el desplazamiento más allá del final de un archivo ya está deshabilitado en el panel orígenes"
[ImageFeedbackIcon]: ../../images/2020/01/feedback-icon.msft.png "Ilustración 21: el icono * * comentarios * * en el DevTools de Microsoft Edge."


<!-- links -->  

[DeviceToolbar]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular un área de visualización móvil con el modo de dispositivo en Microsoft Edge DevTools"
[DeviceFrame]: ../../../device-mode/index.md#show-device-frame "Seleccione Mostrar marco del dispositivo para mostrar el marco del dispositivo físico en la ventanilla."
[CommandMenu]: ../../../command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[ThrottleNetworkAndCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Limite la red y la CPU para simular de forma más precisa las condiciones de navegación web de un usuario móvil."
[crbug924693]: https://crbug.com/924693 "924693: solicitud de característica: agregar moto G4 a la lista de modos de dispositivo"
[crbug1030258]: https://crbug.com/1030258 "1030258"
[crbug1026879]: https://crbug.com/1026879 "1026879: la pestaña de cookies ya no muestra la prioridad en la consola de desarrollo"
[CookiesFields]: ../../../storage/cookies.md#fields "Los campos de la tabla cookies"
[crbug1029826]: https://crbug.com/1029826 "1029826: red > clic con el botón secundario para solicitar > copiar-> copia como fetch no copia las cookies"
[crbug985402]: https://crbug.com/985402 "985402: las cadenas de error del icono del manifiesto de la aplicación web son confusas"
[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demostración de contenido CSS sin escape"
[Settings]: ../../../customize/index.md#settings "Personalizar Microsoft Edge DevTools con la configuración"
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publicar un tweet"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nuevo problema: MicrosoftDocs/Edge-Developer"  
[TheWebWeWant]: https://aka.ms/webwewant "La web que queremos"
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canales de Microsoft Edge Preview"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Depurador para la extensión de código de Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elementos de la extensión de código de Microsoft Edge VS"  
[crbug963183]: https://crbug.com/963183 "963183-DevTools no cumplen la norma WCAG"
[crbug941561]: https://crbug.com/941561 "941561: localizabilidad del DevTools"
[crbug987787]: https://crbug.com/987787 "987787-vista 3D Dom"
[AccessibilityInsights]: https://aka.ms/a11yinsights "Información de accesibilidad"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Complementos de Insider de Microsoft Edge"  
[MicrosoftVisualStudio]: ../../../../visual-studio/index.md "Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Descargar Visual Studio 2019 para Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objetos de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "índice z | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools cuenta de Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Código de Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge-Marketplace de Visual Studio"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos de Microsoft Edge \ (cromo \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-catálogo de soluciones de Visual Studio"
[Webhint]: https://aka.ms/webhint "sugerencia"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extensión de explorador webhint | documentación de webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Extensión de código de VS webhint | documentación de webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Mejorar la prevención de seguimiento en la entrada de blog de Microsoft Edge"

> [!NOTE]
> <span data-ttu-id="b082e-331">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b082e-331">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b082e-332">La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/01/devtools/index) y está creada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="b082e-332">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b082e-334">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b082e-334">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
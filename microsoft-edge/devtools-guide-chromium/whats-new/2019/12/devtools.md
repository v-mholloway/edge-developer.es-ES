---
title: Novedades de DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 03fd78eddf54b68d072ba11401a897ad9f109058
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942144"
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

# <span data-ttu-id="4168f-103">Novedades de DevTools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="4168f-103">What's new in DevTools (Microsoft Edge 80)</span></span>  

## <span data-ttu-id="4168f-104">Anuncios del equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4168f-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="4168f-105">Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo de DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4168f-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="4168f-106">Compruébelos para probar las nuevas características de la DevTools, las extensiones de código de VS y mucho más.</span><span class="sxs-lookup"><span data-stu-id="4168f-106">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="4168f-107">Para mantenerte al tanto de las últimas y mejores características de las herramientas para desarrolladores, descarga los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] y mantente [en Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="4168f-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="4168f-108">Mejoras de accesibilidad para el DevTools</span><span class="sxs-lookup"><span data-stu-id="4168f-108">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="4168f-109">El equipo de DevTools ha contribuido a 170 cambios en cromo para solucionar problemas de alto impacto en el contraste de color, el teclado y el lector de pantalla en el DevTools.</span><span class="sxs-lookup"><span data-stu-id="4168f-109">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="4168f-110">Cada desarrollador que crea la web debe poder usar el DevTools.</span><span class="sxs-lookup"><span data-stu-id="4168f-110">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="4168f-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="4168f-111">Figure 1</span></span>  
> <span data-ttu-id="4168f-112">La herramienta de rendimiento en el DevTools con la navegación con el teclado y las mejoras del lector de pantalla</span><span class="sxs-lookup"><span data-stu-id="4168f-112">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![La herramienta de rendimiento en el DevTools con la navegación con el teclado y las mejoras del lector de pantalla][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="4168f-114">¿Desea saber cómo hacer que su página web sea accesible para todos los usuarios?</span><span class="sxs-lookup"><span data-stu-id="4168f-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="4168f-115">Descargue [Insight Insights][AccessibilityInsights] y extensiones [Webhint][WebhintBrowserExtension] para Microsoft Edge para comenzar.</span><span class="sxs-lookup"><span data-stu-id="4168f-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="4168f-116">Si usa lectores de pantalla o el teclado para desplazarse por la DevTools, envíenos sus comentarios con un [Tweet][PostTweetEdgeDevTools] o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="4168f-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="4168f-117">[#963183][crbug963183] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="4168f-117">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="4168f-118">Usar el DevTools en otros idiomas</span><span class="sxs-lookup"><span data-stu-id="4168f-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="4168f-119">Muchos programadores usan otras herramientas de desarrollo, como StackOverflow y VS Code, en su idioma nativo, no solo en inglés.</span><span class="sxs-lookup"><span data-stu-id="4168f-119">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="4168f-120">Nos complace anunciar la localización de la DevTools, que ahora puedes usar en uno de los 10 idiomas además del inglés:</span><span class="sxs-lookup"><span data-stu-id="4168f-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="4168f-121">Chino \ (simplificado \)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="4168f-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4168f-122">Chino (tradicional \)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="4168f-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="4168f-123">Francés: Francisco&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="4168f-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4168f-124">Alemán-Deutsch</span><span class="sxs-lookup"><span data-stu-id="4168f-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="4168f-125">Italiano-Italiano</span><span class="sxs-lookup"><span data-stu-id="4168f-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4168f-126"> &#26085;&#26412;&#35486; japonés</span><span class="sxs-lookup"><span data-stu-id="4168f-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="4168f-127">Coreano:  &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="4168f-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4168f-128">Portugués-Portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="4168f-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="4168f-129">Ruso:  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="4168f-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4168f-130">Español-Espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="4168f-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="4168f-131">Vaya a `edge://flags` y establezca la marca **Habilitar herramientas de desarrollo localizadas** en **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="4168f-131">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="4168f-132">También establezca el marcador de **experimentos de herramientas de desarrollo** en **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="4168f-132">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="4168f-133">Reinicie Microsoft Edge y abra el DevTools.</span><span class="sxs-lookup"><span data-stu-id="4168f-133">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="4168f-134">El DevTools coincide con el idioma que usas para Microsoft Edge en `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="4168f-134">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

> ##### <span data-ttu-id="4168f-135">Figura 2</span><span class="sxs-lookup"><span data-stu-id="4168f-135">Figure 2</span></span>  
> <span data-ttu-id="4168f-136">El DevTools en alemán</span><span class="sxs-lookup"><span data-stu-id="4168f-136">The DevTools in German</span></span>  
> ![El DevTools en alemán][ImageLocalizedGerman]  

<span data-ttu-id="4168f-138">Si desea usar la DevTools en un idioma diferente al de los que están disponibles, [Tweet][PostTweetEdgeDevTools] o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="4168f-138">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="4168f-139">[#941561][crbug941561] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="4168f-139">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="4168f-140">extensión webhint de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4168f-140">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="4168f-141">La extensión webhint de Microsoft Edge te permite examinar fácilmente tu página web y obtener comentarios sobre la accesibilidad, la compatibilidad de explorador, la seguridad, el rendimiento y mucho más dentro de la DevTools.</span><span class="sxs-lookup"><span data-stu-id="4168f-141">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="4168f-142">Para obtener más información, consulte [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="4168f-142">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="4168f-143">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="4168f-143">Figure 3</span></span>  
> <span data-ttu-id="4168f-144">La pestaña sugerencias de la DevTools cuando está instalada la extensión de explorador webhint</span><span class="sxs-lookup"><span data-stu-id="4168f-144">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![La pestaña sugerencias de la DevTools cuando está instalada la extensión de explorador webhint][ImageHintsTabWebhintExtension]  

<span data-ttu-id="4168f-146">[Prueba la extensión de explorador webhint en Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="4168f-146">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="4168f-147">Una vez que haya instalado la extensión, abra el DevTools y seleccione la pestaña sugerencias.  Desde aquí, ejecute un examen de sitios personalizable.</span><span class="sxs-lookup"><span data-stu-id="4168f-147">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="4168f-148">Visita [webhint.IO][WebhintBrowserExtension] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4168f-148">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <span data-ttu-id="4168f-149">Vista 3D</span><span class="sxs-lookup"><span data-stu-id="4168f-149">3D View</span></span>  

<span data-ttu-id="4168f-150">Use la **vista 3D** para depurar la aplicación web desplazándose por el [modelo de objeto de documento \ (Dom \)][MDNDocumentObjectModel] o el contexto de apilamiento [de índice z][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="4168f-150">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="4168f-151">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="4168f-151">Figure 4</span></span>  
> <span data-ttu-id="4168f-152">Vista 3D en el DevTools</span><span class="sxs-lookup"><span data-stu-id="4168f-152">The 3D View in the DevTools</span></span>  
> ![Vista 3D en el DevTools][Image3DView]  

<span data-ttu-id="4168f-154">Para obtener acceso a la vista 3D, vaya a `edge://flags` y asegúrese de que el indicador **experimentos de herramientas para desarrolladores** está **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="4168f-154">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="4168f-155">Reinicie Microsoft Edge y abra el DevTools.</span><span class="sxs-lookup"><span data-stu-id="4168f-155">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="4168f-156">Pulsa `F1` en la DevTools o ve a **configuración**, ve a sección **experimentos** y marca la casilla **Habilitar vista 3D** .</span><span class="sxs-lookup"><span data-stu-id="4168f-156">Press `F1` in the DevTools or go to **Settings**, navigate to **Experiments** section, and check the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="4168f-157">Ahora, pulse `Ctrl`  +  `Shift`  +  `P` , escriba en la **vista 3D** y seleccione **Mostrar vista en 3D**.</span><span class="sxs-lookup"><span data-stu-id="4168f-157">Now, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="4168f-158">Trabajamos en la interfaz de usuario y agregamos más funciones a la vista 3D; por lo tanto, envíanos tus [comentarios](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="4168f-158">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="4168f-159">[#987787][crbug987787] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="4168f-159">Chromium issue [#987787][crbug987787]</span></span>

### <span data-ttu-id="4168f-160">Extensiones de código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4168f-160">Visual Studio Code extensions</span></span>  

<span data-ttu-id="4168f-161">El equipo de DevTools también ha publicado algunas extensiones para [Visual Studio Code \ (vs Code \)][VisualStudioCode] que te permiten usar la potencia de DevTools directamente desde tu editor de texto.</span><span class="sxs-lookup"><span data-stu-id="4168f-161">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="4168f-162">Consulta las siguientes extensiones:</span><span class="sxs-lookup"><span data-stu-id="4168f-162">Check out the extensions below:</span></span>  

#### <span data-ttu-id="4168f-163">Elementos de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4168f-163">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="4168f-164">Use la herramienta elementos de VS Code agregando los [elementos de la extensión de código de Microsoft Edge \ (cromo \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] .</span><span class="sxs-lookup"><span data-stu-id="4168f-164">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="4168f-165">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="4168f-165">Figure 5</span></span>  
> <span data-ttu-id="4168f-166">La herramienta elementos en VS Code que usa los elementos de la extensión de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4168f-166">The Elements tool in VS Code using the Elements for Microsoft Edge extension</span></span>  
> ![La herramienta elementos en VS Code que usa los elementos de la extensión de Microsoft Edge][ImageElementsVisualStudioCode]  

<span data-ttu-id="4168f-168">Para obtener más información, consulta [los elementos de la extensión de código de Microsoft Edge vs][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="4168f-168">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="4168f-169">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4168f-169">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="4168f-170">Con el [depurador para la extensión de código de Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] vs, depure JavaScript que se ejecuta en Microsoft Edge directamente desde el código de vs.</span><span class="sxs-lookup"><span data-stu-id="4168f-170">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="4168f-171">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="4168f-171">Figure 6</span></span>  
> <span data-ttu-id="4168f-172">El depurador para la extensión de Microsoft Edge en VS Code</span><span class="sxs-lookup"><span data-stu-id="4168f-172">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![El depurador para la extensión de Microsoft Edge en VS Code][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="4168f-174">Para obtener más información, consulte [Cómo depurar Microsoft Edge desde vs Code][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="4168f-174">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="4168f-175">webhint</span><span class="sxs-lookup"><span data-stu-id="4168f-175">webhint</span></span>  

<span data-ttu-id="4168f-176">La extensión de código [webhint][VisualStudioMarketplaceWebhintExtension] de vs usa `webhint` para mejorar la página web mientras la escribes.</span><span class="sxs-lookup"><span data-stu-id="4168f-176">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="4168f-177">Esta extensión ejecuta y notifica diagnósticos en los archivos de área de trabajo según el `webhint` análisis.</span><span class="sxs-lookup"><span data-stu-id="4168f-177">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="4168f-178">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="4168f-178">Figure 7</span></span>  
> <span data-ttu-id="4168f-179">La extensión de código de webhint VS analizando un archivo. TSX en VS Code</span><span class="sxs-lookup"><span data-stu-id="4168f-179">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![La extensión de código de webhint VS analizando un archivo. TSX en VS Code][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="4168f-181">[Más información sobre la extensión webhint de vs Code][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="4168f-181">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="4168f-182">Integración con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4168f-182">Visual Studio integration</span></span>
<span data-ttu-id="4168f-183">En Visual Studio 2019 versión 16,2 o posterior, usa el depurador de Visual Studio para depurar JavaScript que se ejecuta en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4168f-183">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="4168f-184">[Descarga Visual Studio 2019][MicrosoftVisualStudioDownloads] para probar esta característica.</span><span class="sxs-lookup"><span data-stu-id="4168f-184">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="4168f-185">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="4168f-185">Figure 8</span></span>  
> <span data-ttu-id="4168f-186">Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta</span><span class="sxs-lookup"><span data-stu-id="4168f-186">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="4168f-188">[Lea nuestra entrada de blog para obtener información sobre cómo depurar Microsoft Edge desde Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="4168f-188">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <span data-ttu-id="4168f-189">Mensajes de la consola de prevención de seguimiento</span><span class="sxs-lookup"><span data-stu-id="4168f-189">Tracking prevention Console messages</span></span>  

<span data-ttu-id="4168f-190">La prevención de seguimiento es una característica exclusiva de Microsoft Edge que le protege de ser rastreada por los sitios web que no ha visitado antes.</span><span class="sxs-lookup"><span data-stu-id="4168f-190">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="4168f-191">La configuración predeterminada de prevención de rastreo es el modo equilibrado, que bloquea los rastreadores de terceros y los rastreadores maliciosos conocidos para obtener una experiencia que equilibre la compatibilidad de la privacidad y la Web.</span><span class="sxs-lookup"><span data-stu-id="4168f-191">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="4168f-192">Para obtener más información sobre la compatibilidad de su página web cuando se bloquean determinados rastreadores, también hemos añadido mensajes de advertencia en la consola cuando se bloquea un rastreador.</span><span class="sxs-lookup"><span data-stu-id="4168f-192">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="4168f-193">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="4168f-193">Figure 9</span></span>  
> <span data-ttu-id="4168f-194">Mensajes en la consola cuando el seguimiento de prevención bloquea el acceso al almacenamiento de un rastreador</span><span class="sxs-lookup"><span data-stu-id="4168f-194">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Mensajes en la consola cuando el seguimiento de prevención bloquea el acceso al almacenamiento de un rastreador][ImageTrackingPrevention]  

<span data-ttu-id="4168f-196">[Obtenga más información acerca de la prevención de seguimiento y el equilibrio entre privacidad y compatibilidad web][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="4168f-196">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="4168f-197">Anuncios del proyecto de cromo</span><span class="sxs-lookup"><span data-stu-id="4168f-197">Announcements from the Chromium project</span></span>  

<span data-ttu-id="4168f-198">En las siguientes secciones se anuncian características adicionales disponibles en Microsoft Edge 80 que se han contribuido al proyecto de código abierto.</span><span class="sxs-lookup"><span data-stu-id="4168f-198">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="4168f-199">Compatibilidad con las redeclaraciones Let y Class en la consola</span><span class="sxs-lookup"><span data-stu-id="4168f-199">Support for let and class redeclarations in the Console</span></span>  

<span data-ttu-id="4168f-200">La consola ahora es compatible con las declaraciones `let` e `class` instrucciones.</span><span class="sxs-lookup"><span data-stu-id="4168f-200">The Console now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="4168f-201">La incapacidad de redeclarar fue una molestia común para los desarrolladores web que usan la consola para experimentar con el nuevo código de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4168f-201">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="4168f-202">La Redeclaración de `let` una `class` instrucción or en una secuencia de comandos fuera de la consola o dentro de una sola entrada de consola sigue produciendo un `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="4168f-202">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="4168f-203">Por ejemplo, antes, cuando se redeclara una variable local con `let` , la consola producía un error:</span><span class="sxs-lookup"><span data-stu-id="4168f-203">For example, previously, when redeclaring a local variable with `let`, the Console threw an error:</span></span>  

> ##### <span data-ttu-id="4168f-204">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="4168f-204">Figure 10</span></span>  
> <span data-ttu-id="4168f-205">La consola en Microsoft Edge 79 que muestra que no se puede realizar la Redeclaración</span><span class="sxs-lookup"><span data-stu-id="4168f-205">The Console in Microsoft Edge 79 showing that the let redeclaration fails</span></span>  
> ![La consola en Microsoft Edge 79 que muestra que no se puede realizar la Redeclaración][ImageConsoleRedeclarationFails]  

<span data-ttu-id="4168f-207">Ahora, la consola permite la nueva declaración:</span><span class="sxs-lookup"><span data-stu-id="4168f-207">Now, the Console allows the redeclaration:</span></span>  

> ##### <span data-ttu-id="4168f-208">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="4168f-208">Figure 11</span></span>  
> <span data-ttu-id="4168f-209">La consola en Microsoft Edge 80, que muestra que la Redeclaración Let se realiza correctamente</span><span class="sxs-lookup"><span data-stu-id="4168f-209">The Console in Microsoft Edge 80 showing that the let redeclaration succeeds</span></span>  
> ![La consola en Microsoft Edge 80, que muestra que la Redeclaración Let se realiza correctamente][ImageConsoleRedeclarationSucceeds]  

<span data-ttu-id="4168f-211">[#1004193][crbug1004193] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="4168f-211">Chromium issue [#1004193][crbug1004193]</span></span>  

### <span data-ttu-id="4168f-212">Depuración de webassembler mejorada</span><span class="sxs-lookup"><span data-stu-id="4168f-212">Improved WebAssembly debugging</span></span>  

<span data-ttu-id="4168f-213">DevTools ha empezado a admitir el [estándar de depuración Dwarf][DwarfHome], lo que significa que se ha mejorado la compatibilidad para desplazarse por el código, establecer puntos de interrupción y resolver los rastros de pila en los idiomas de origen en DevTools.</span><span class="sxs-lookup"><span data-stu-id="4168f-213">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
> ##### Figure  
> The new DWARF-powered WebAssembly debugging  
> ![The new DWARF-powered WebAssembly debugging][ImageDwarfPoweredWebAssemblyDebugging]  
-->  

### <span data-ttu-id="4168f-214">Actualizaciones del panel de red</span><span class="sxs-lookup"><span data-stu-id="4168f-214">Network panel updates</span></span>  

#### <span data-ttu-id="4168f-215">Solicitar cadenas de iniciador en la ficha Initiator</span><span class="sxs-lookup"><span data-stu-id="4168f-215">Request Initiator Chains in the Initiator tab</span></span>  

<span data-ttu-id="4168f-216">Ahora puede ver los iniciadores y las dependencias de una solicitud de red como una lista anidada.</span><span class="sxs-lookup"><span data-stu-id="4168f-216">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="4168f-217">Esto puede ayudarle a comprender por qué se solicitó un recurso o la actividad de la red que un determinado recurso \ (como un script \) ha causado.</span><span class="sxs-lookup"><span data-stu-id="4168f-217">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

> ##### <span data-ttu-id="4168f-218">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="4168f-218">Figure 12</span></span>  
> <span data-ttu-id="4168f-219">Una cadena de iniciador de solicitudes en la ficha Initiator</span><span class="sxs-lookup"><span data-stu-id="4168f-219">A Request Initiator Chain in the Initiator tab</span></span>  
> ![Una cadena de iniciador de solicitudes en la ficha Initiator][ImageRequestInitiatorChain]  

<span data-ttu-id="4168f-221">Después [de registrar la actividad de la red en el panel red][DevToolsNetworkIndex], haga clic en un recurso y, a continuación, vaya a la pestaña **iniciador** para ver la **cadena de iniciadores de solicitudes**:</span><span class="sxs-lookup"><span data-stu-id="4168f-221">After [logging network activity in the Network panel][DevToolsNetworkIndex], click a resource and then go to the **Initiator** tab to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="4168f-222">El **recurso inspeccionado** está en negrita.</span><span class="sxs-lookup"><span data-stu-id="4168f-222">The **inspected resource** is bold.</span></span>  <span data-ttu-id="4168f-223">En la captura de pantalla anterior, `ai.2.min.js` se encuentra el recurso inspeccionado.</span><span class="sxs-lookup"><span data-stu-id="4168f-223">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="4168f-224">Los recursos situados por encima del recurso inspeccionado son los **iniciadores**.</span><span class="sxs-lookup"><span data-stu-id="4168f-224">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="4168f-225">En la captura de pantalla anterior, `https://www.microsoftedgeinsider.com` se trata del iniciador de `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="4168f-225">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="4168f-226">En otras palabras, `https://www.microsoftedgeinsider.com` causó la solicitud de red `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="4168f-226">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="4168f-227">Los recursos que se encuentran debajo del recurso inspeccionado son las **dependencias**.</span><span class="sxs-lookup"><span data-stu-id="4168f-227">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="4168f-228">En la captura de pantalla anterior, `https://dc.services.visualstudio.com/v2/track` se trata de una dependencia de `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="4168f-228">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="4168f-229">En otras palabras, `ai.2.min.js` causó la solicitud de red `https://dc.services.visualstudio.com/v2/track` .</span><span class="sxs-lookup"><span data-stu-id="4168f-229">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="4168f-230">También se puede tener acceso a la información del iniciador y la dependencia si se mantiene presionado `Shift` y, a continuación, coloca el puntero sobre recursos de red.</span><span class="sxs-lookup"><span data-stu-id="4168f-230">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="4168f-231">Consulte [Ver iniciadores y dependencias][DevToolsNetworkReferenceViewInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="4168f-231">See [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="4168f-232">[#842488][crbug842488] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="4168f-232">Chromium issue [#842488][crbug842488]</span></span>  

#### <span data-ttu-id="4168f-233">Resaltar la solicitud de red seleccionada en la información general</span><span class="sxs-lookup"><span data-stu-id="4168f-233">Highlight the selected network request in the Overview</span></span>  

<span data-ttu-id="4168f-234">Después de hacer clic en un recurso de red para inspeccionarlo, el panel red ahora coloca un borde azul en torno a ese recurso en la **información general**.</span><span class="sxs-lookup"><span data-stu-id="4168f-234">After you click a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="4168f-235">Esto puede ayudarle a detectar si la solicitud de red se está realizando antes o después de lo esperado.</span><span class="sxs-lookup"><span data-stu-id="4168f-235">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

> ##### <span data-ttu-id="4168f-236">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="4168f-236">Figure 13</span></span>  
> <span data-ttu-id="4168f-237">El panel de información general resaltando el recurso inspeccionado</span><span class="sxs-lookup"><span data-stu-id="4168f-237">The Overview pane highlighting the inspected resource</span></span>  
> ![El panel de información general resaltando el recurso inspeccionado][ImageOverviewPaneInspectedResource]  

<span data-ttu-id="4168f-239">[#988253][crbug988253] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="4168f-239">Chromium issue [#988253][crbug988253]</span></span>  

#### <span data-ttu-id="4168f-240">Columnas URL y ruta de acceso en el panel red</span><span class="sxs-lookup"><span data-stu-id="4168f-240">URL and path columns in the Network panel</span></span>  

<span data-ttu-id="4168f-241">Use las nuevas columnas de **dirección URL** y **ruta de acceso** del panel **red** para ver la ruta de acceso absoluta o la dirección URL completa de cada recurso de red.</span><span class="sxs-lookup"><span data-stu-id="4168f-241">Use the new **Path** and **URL** columns in the **Network** panel to see the absolute path or full URL of each network resource.</span></span>  

> ##### <span data-ttu-id="4168f-242">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="4168f-242">Figure 14</span></span>  
> <span data-ttu-id="4168f-243">Las nuevas columnas de dirección URL y ruta de acceso del panel red</span><span class="sxs-lookup"><span data-stu-id="4168f-243">The new Path and URL columns in the Network panel</span></span>  
> ![Las nuevas columnas de dirección URL y ruta de acceso del panel red][ImagePathNetworkPanel]  

<span data-ttu-id="4168f-245">Haga clic con el botón secundario en el encabezado de tabla **cascada** y seleccione **ruta** o **dirección URL** para mostrar las nuevas columnas.</span><span class="sxs-lookup"><span data-stu-id="4168f-245">Right-click the **Waterfall** table header and select **Path** or **URL** to show the new columns.</span></span>  

<span data-ttu-id="4168f-246">[#993366][crbug993366] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="4168f-246">Chromium issue [#993366][crbug993366]</span></span>  

#### <span data-ttu-id="4168f-247">Cadenas de agente de usuario actualizadas</span><span class="sxs-lookup"><span data-stu-id="4168f-247">Updated User-Agent strings</span></span>  

<span data-ttu-id="4168f-248">DevTools admite la configuración de una cadena de agente de usuario personalizada en la pestaña **condiciones de red** .  La cadena de agente de usuario afecta al `User-Agent` encabezado HTTP adjunto a los recursos de red y también al valor de `navigator.userAgent` .</span><span class="sxs-lookup"><span data-stu-id="4168f-248">DevTools supports setting a custom User-Agent string through the **Network Conditions** tab.  The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="4168f-249">Las cadenas de agente de usuario predefinidas se han actualizado para reflejar las versiones modernas del explorador.</span><span class="sxs-lookup"><span data-stu-id="4168f-249">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

> ##### <span data-ttu-id="4168f-250">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="4168f-250">Figure 15</span></span>  
> <span data-ttu-id="4168f-251">El menú agente de usuario en la pestaña condiciones de red</span><span class="sxs-lookup"><span data-stu-id="4168f-251">The User Agent menu in the Network Conditions tab</span></span>  
> ![El menú agente de usuario en la pestaña condiciones de red][ImageUserAgentNetworkConditionsTab]  

<span data-ttu-id="4168f-253">Para obtener acceso a **condiciones**de la red, [Abra el menú de comandos][DevToolsCommandMenuIndex] y ejecute el `Show Network Conditions` comando.</span><span class="sxs-lookup"><span data-stu-id="4168f-253">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="4168f-254">También puede [establecer cadenas de agente de usuario en el modo de dispositivo][DevToolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="4168f-254">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="4168f-255">[#1029031][crbug1029031] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="4168f-255">Chromium issue [#1029031][crbug1029031]</span></span>  

### <span data-ttu-id="4168f-256">Actualizaciones del panel auditorías</span><span class="sxs-lookup"><span data-stu-id="4168f-256">Audits panel updates</span></span>  

#### <span data-ttu-id="4168f-257">Nueva interfaz de usuario de configuración</span><span class="sxs-lookup"><span data-stu-id="4168f-257">New configuration UI</span></span>  

<span data-ttu-id="4168f-258">La interfaz de usuario de configuración tiene un diseño nuevo y con capacidad de respuesta, y las opciones de configuración de límite se han simplificado.</span><span class="sxs-lookup"><span data-stu-id="4168f-258">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="4168f-259">Para obtener más información sobre los cambios de la interfaz de usuario de regulación, consulte [regulación del panel auditorías][GitHubGoogleChromeDevToolsAuditsPanelThrottling] .</span><span class="sxs-lookup"><span data-stu-id="4168f-259">See [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling] for more information on the throttling UI changes.</span></span>  

> ##### <span data-ttu-id="4168f-260">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="4168f-260">Figure 16</span></span>  
> <span data-ttu-id="4168f-261">La nueva interfaz de usuario de configuración</span><span class="sxs-lookup"><span data-stu-id="4168f-261">The new configuration UI</span></span>  
> ![La nueva interfaz de usuario de configuración][ImageConfigurationUI]  

### <span data-ttu-id="4168f-263">Actualizaciones de la ficha cobertura</span><span class="sxs-lookup"><span data-stu-id="4168f-263">Coverage tab updates</span></span>  

#### <span data-ttu-id="4168f-264">Modos de cobertura por función o por bloque</span><span class="sxs-lookup"><span data-stu-id="4168f-264">Per-function or per-block coverage modes</span></span>  

<span data-ttu-id="4168f-265">La [pestaña cobertura][DevToolsCoverageIndex] tiene un nuevo menú desplegable que le permite especificar si se deben recopilar datos de cobertura de código **por función** o **por bloque**.</span><span class="sxs-lookup"><span data-stu-id="4168f-265">The [Coverage tab][DevToolsCoverageIndex] has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="4168f-266">La cobertura **por bloque** es más detallada, pero es mucho más costosa de recopilar.</span><span class="sxs-lookup"><span data-stu-id="4168f-266">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="4168f-267">De forma predeterminada, DevTools usa la cobertura de **por función** .</span><span class="sxs-lookup"><span data-stu-id="4168f-267">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="4168f-268">Es posible que vea diferencias de cobertura de código de gran tamaño en archivos HTML dependiendo de si usa **por función** o **por bloque** .</span><span class="sxs-lookup"><span data-stu-id="4168f-268">You may see large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="4168f-269">Al usar el modo **por función** , las secuencias de comandos en línea de archivos HTML se tratan como funciones.</span><span class="sxs-lookup"><span data-stu-id="4168f-269">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="4168f-270">Si se ejecuta la secuencia de comandos, DevTools marca la secuencia de comandos completa como código usado.</span><span class="sxs-lookup"><span data-stu-id="4168f-270">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="4168f-271">Solo si el script no se ejecuta, DevTools marca el script como código no usado.</span><span class="sxs-lookup"><span data-stu-id="4168f-271">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

> ##### <span data-ttu-id="4168f-272">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="4168f-272">Figure 17</span></span>  
> <span data-ttu-id="4168f-273">El menú desplegable modo de cobertura</span><span class="sxs-lookup"><span data-stu-id="4168f-273">The coverage mode dropdown menu</span></span>  
> ![El menú desplegable modo de cobertura][ImageCoverageMode]  

#### <span data-ttu-id="4168f-275">La cobertura debe iniciarse ahora al volver a cargar una página</span><span class="sxs-lookup"><span data-stu-id="4168f-275">Coverage must now be initiated by a page reload</span></span>  

<span data-ttu-id="4168f-276">Se ha quitado la cobertura de código sin que se recargue la página porque los datos de cobertura eran inconfiables.</span><span class="sxs-lookup"><span data-stu-id="4168f-276">Toggling code coverage without a page reload has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="4168f-277">Por ejemplo, se puede notificar que una función no se usa si el tiempo de ejecución fue de larga duración y el recolector de elementos no utilizados de la V8 ha limpiado.</span><span class="sxs-lookup"><span data-stu-id="4168f-277">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="4168f-278">[#1004203][crbug1004203] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="4168f-278">Chromium issue [#1004203][crbug1004203]</span></span>  

## <span data-ttu-id="4168f-279">Descargar los canales de Microsoft Edge Preview</span><span class="sxs-lookup"><span data-stu-id="4168f-279">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="4168f-280">Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4168f-280">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="4168f-281">Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4168f-281">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="4168f-282">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4168f-282">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!--<<../../_shared/devtools-feedback.md>> -->

<!--<<../../_shared/canary.md>> -->

<!--<<../../_shared/discover.md>> -->

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2019/12/a11y-performance-tool.msft.gif "Ilustración 1: la herramienta de rendimiento en DevTools con la navegación con el teclado y las mejoras del lector de pantalla"  
[ImageLocalizedGerman]: ../../images/2019/12/localized-devtools.msft.png "Ilustración 2: el DevTools en alemán"  
[ImageHintsTabWebhintExtension]: ../../images/2019/12/webhint-browser-extension.msft.png "Ilustración 3: la pestaña sugerencias en Microsoft Edge DevTools cuando la extensión de explorador webhint está instalada"  
[Image3DView]: ../../images/2019/12/3dview.msft.png "Ilustración 4: vista 3D en el DevTools de Microsoft Edge"  
[ImageElementsVisualStudioCode]: ../../images/2019/12/elements-for-edge.msft.png "Ilustración 5: la herramienta elementos en VS Code que usa los elementos de la extensión de Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2019/12/vscode-debugger.msft.png "Ilustración 6: el depurador para la extensión de Microsoft Edge en VS Code"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2019/12/webhint-vscode-extension.msft.png "Ilustración 7: la extensión de código webhint de VS analizando un archivo. TSX en VS Code"  
[ImageVisualStudioLaunchWebApp]: ../../images/2019/12/vs.msft.png "Ilustración 8: Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta"  
[ImageTrackingPrevention]: ../../images/2019/12/tracking-prevention.msft.png "Ilustración 9: mensajes en la consola cuando el control de prevención bloquea el acceso al almacenamiento de un rastreador"  
[ImageConsoleRedeclarationFails]: ../../images/2019/12/letbefore.msft.png "Ilustración 10: la consola en Microsoft Edge 79 que muestra que no se puede realizar la Redeclaración"  
[ImageConsoleRedeclarationSucceeds]: ../../images/2019/12/letafter.msft.png "Ilustración 11: la consola en Microsoft Edge 80, que muestra que la Redeclaración Let se realiza correctamente"  
[ImageRequestInitiatorChain]: ../../images/2019/12/initiators.msft.png "Figura 12: una cadena de iniciador de solicitudes en la ficha Initiator"  
[ImageOverviewPaneInspectedResource]: ../../images/2019/12/overview.msft.png "Ilustración 13: el panel de información general resaltando el recurso inspeccionado"  
[ImagePathNetworkPanel]: ../../images/2019/12/columns.msft.png "Ilustración 14: nuevas columnas de dirección URL y ruta de acceso en el panel red"  
[ImageUserAgentNetworkConditionsTab]: ../../images/2019/12/useragent.msft.png "Ilustración 15: el menú agente de usuario en la pestaña condiciones de red"  
[ImageConfigurationUI]: ../../images/2019/12/start.msft.png "Ilustración 16: la nueva interfaz de usuario de configuración"  
[ImageCoverageMode]: ../../images/2019/12/modes.msft.png "Ilustración 17: menú desplegable de modo de cobertura"  

<!--[ImageDwarfPoweredWebAssemblyDebugging]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: ../../../command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[DevToolsCoverageIndex]: ../../../coverage/index.md "Buscar código JavaScript y CSS sin usar con la pestaña cobertura en Microsoft Edge DevTools"  
[DevToolsDeviceModeIndex]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular un área de visualización móvil: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools"  
[DevToolsNetworkIndex]: ../../../network/index.md "Inspeccionar la actividad de la red en Microsoft Edge DevTools"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: ../../../network/reference.md#view-initiators-and-dependencies "Ver iniciadores y dependencias-referencia de análisis de red"  
[DevGuideEdgeHtmlWhatsNew]: ../../../../dev-guide/whats-new.md "Novedades de EdgeHTML"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Depurador para la extensión de código de Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elementos de la extensión de código de Microsoft Edge VS"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[crbug842488]: https://crbug.com/842488 "842488: agregue el campo Initiator a la pestaña encabezados: monorail"  
[crbug988253]: https://crbug.com/988253 "988253-error DevTools: sin asociación entre la solicitud de red y el gráfico de escala de tiempo: monorail"  
[crbug993366]: https://crbug.com/993366 "993366: mostrar parte de la ruta en la dirección URL en la lista de solicitudes del panel de red-monorail"  
[crbug1004193]: https://crbug.com/1004193 "1004193: modo de perdedor para V8-monorail"  
[crbug1004203]: https://crbug.com/1004203 "1004203-monorail"  
[crbug1029031]: https://crbug.com/1029031 "1029031-las cadenas de UA se están desactualizadas-monorail" 
[crbug963183]: https://crbug.com/963183 "963183-DevTools no cumplen la norma WCAG"
[crbug941561]: https://crbug.com/941561 "941561: localizabilidad del DevTools"
[crbug987787]: https://crbug.com/987787 "987787-vista 3D Dom"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Información de accesibilidad"  

[DwarfHome]: https://dwarfstd.org "Dwarf hogar"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "DevTools de la pantalla de auditorías de GoogleChrome/Lighthouse | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nuevo problema: MicrosoftDocs/Edge-Developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canales de Microsoft Edge Preview"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Complementos de Insider de Microsoft Edge"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Depurar JavaScript en Microsoft Edge desde Visual Studio | Blog de Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Descargar Visual Studio 2019 para Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objetos de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "índice z | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools cuenta de Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Código de Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge-Marketplace de Visual Studio"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos de Microsoft Edge \ (cromo \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-catálogo de soluciones de Visual Studio"
[Webhint]: https://aka.ms/webhint "sugerencia"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extensión de explorador webhint | documentación de webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Extensión de código de VS webhint | documentación de webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Mejorar la prevención de seguimiento en la entrada de blog de Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "La web que queremos"

> [!NOTE]
> <span data-ttu-id="4168f-339">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4168f-339">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4168f-340">La página original se encuentra [aquí](https://developers.google.com/web/updates/2019/12/devtools/index) y está creada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="4168f-340">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4168f-342">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4168f-342">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

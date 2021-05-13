---
description: Vista 3D, Visual Studio integración con Microsoft Edge y mucho más.
title: Novedades de DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 03b17f524e9be55e1ed37147ce46b7a15fc3a17d
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564962"
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
# <a name="whats-new-in-devtools-microsoft-edge-81"></a><span data-ttu-id="ab847-104">Novedades de DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="ab847-104">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ab847-105">Anuncios del equipo Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ab847-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="ab847-106">Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="ab847-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="ab847-107">Echa un vistazo a los anuncios para probar nuevas características en DevTools, Microsoft Visual Studio code extensions y mucho más.</span><span class="sxs-lookup"><span data-stu-id="ab847-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="ab847-108">Para mantenerse al día de todas las características más recientes [][MicrosoftEdgePreviewChannels] y más importantes de las herramientas para desarrolladores, descargue los canales de vista previa Microsoft Edge y [síganos en Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="ab847-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="accessibility-improvements-to-the-devtools"></a><span data-ttu-id="ab847-109">Mejoras de accesibilidad a DevTools</span><span class="sxs-lookup"><span data-stu-id="ab847-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="ab847-110">El equipo de DevTools ha contribuido con 170 cambios en Chromium para solucionar problemas de contraste de color, teclado y lector de pantalla de alto impacto en DevTools.</span><span class="sxs-lookup"><span data-stu-id="ab847-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="ab847-111">Cada desarrollador que esté creando la web debe poder usar DevTools.</span><span class="sxs-lookup"><span data-stu-id="ab847-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="La herramienta Rendimiento de DevTools con las mejoras de navegación del teclado y lector de pantalla" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="ab847-113">La **herramienta Rendimiento** de DevTools con las mejoras de navegación del teclado y lector de pantalla</span><span class="sxs-lookup"><span data-stu-id="ab847-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-114">¿Desea obtener información sobre cómo hacer que la página web sea accesible para todos los usuarios?</span><span class="sxs-lookup"><span data-stu-id="ab847-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="ab847-115">Descargue las [extensiones accessibility Insights][AccessibilityInsights] y [webhint][WebhintBrowserExtension] Microsoft Edge para empezar.</span><span class="sxs-lookup"><span data-stu-id="ab847-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="ab847-116">Si usas lectores de pantalla o el teclado para navegar [][PostTweetEdgeDevTools] por DevTools, envíanos tus comentarios tuiteando o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.</span><span class="sxs-lookup"><span data-stu-id="ab847-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="ab847-117">Chromium problema [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="ab847-117">Chromium issue [#963183][CR963183]</span></span>  

### <a name="using-the-devtools-in-other-languages"></a><span data-ttu-id="ab847-118">Uso de DevTools en otros idiomas</span><span class="sxs-lookup"><span data-stu-id="ab847-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="ab847-119">Muchos desarrolladores usan otras herramientas de desarrollador, como StackOverflow y Visual Studio Code, en su idioma nativo, no solo en inglés.</span><span class="sxs-lookup"><span data-stu-id="ab847-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="ab847-120">Estamos encantados de anunciar la localización de DevTools, que ahora puedes usar en uno de los 10 idiomas además del inglés:</span><span class="sxs-lookup"><span data-stu-id="ab847-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ab847-121">Chino \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="ab847-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ab847-122">Chino \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="ab847-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="ab847-123">Francés : fran&#231;ais</span><span class="sxs-lookup"><span data-stu-id="ab847-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ab847-124">Alemán - deutsch</span><span class="sxs-lookup"><span data-stu-id="ab847-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="ab847-125">Italiano - italiano</span><span class="sxs-lookup"><span data-stu-id="ab847-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ab847-126">Japonés - &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="ab847-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="ab847-127">Coreano - &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="ab847-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ab847-128">Portugués : portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="ab847-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="ab847-129">Ruso – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="ab847-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ab847-130">Español - espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="ab847-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="ab847-131">Las DevTools coinciden automáticamente con el idioma que usa para Microsoft Edge en `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="ab847-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="ab847-132">Si desea que Microsoft Edge en un idioma y devTools permanezca en inglés, seleccione en DevTools para abrir Configuración y deshabilitar Match `F1` **browser language**. [][DevtoolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="ab847-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, select `F1` in the DevTools to open [Settings][DevtoolsCustomizeIndexSettings] and disable **Match browser language**.</span></span>  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="DevTools en alemán" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   <span data-ttu-id="ab847-134">DevTools en alemán</span><span class="sxs-lookup"><span data-stu-id="ab847-134">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-135">**Los mensajes** de consola no están localizados.</span><span class="sxs-lookup"><span data-stu-id="ab847-135">**Console** messages are not localized.</span></span>  <span data-ttu-id="ab847-136">Solo las cadenas usadas en la interfaz de usuario de DevTools se muestran en el idioma que usa para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab847-136">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="ab847-137">Si quieres usar DevTools en un idioma diferente al que está [disponible,][PostTweetEdgeDevTools] envíanos un tweet o elige el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.</span><span class="sxs-lookup"><span data-stu-id="ab847-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or choose the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="ab847-138">Chromium problema [#941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="ab847-138">Chromium issue [#941561][CR941561]</span></span>  

### <a name="webhint-microsoft-edge-extension"></a><span data-ttu-id="ab847-139">extensión webhint Microsoft Edge webhint</span><span class="sxs-lookup"><span data-stu-id="ab847-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="ab847-140">La extensión webhint Microsoft Edge le permite examinar fácilmente la página web y obtener comentarios sobre accesibilidad, compatibilidad del explorador, seguridad, rendimiento y mucho más dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="ab847-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="ab847-141">Leer más en [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="ab847-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="La herramienta Sugerencias en DevTools cuando se instala la extensión del explorador webhint" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   <span data-ttu-id="ab847-143">La **herramienta Sugerencias** en DevTools cuando se instala la extensión del explorador webhint</span><span class="sxs-lookup"><span data-stu-id="ab847-143">The **Hints** tool in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-144">[Pruebe la extensión del explorador webhint en Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="ab847-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="ab847-145">Una vez instalada la extensión, abra DevTools y elija la **herramienta Sugerencias.**</span><span class="sxs-lookup"><span data-stu-id="ab847-145">Once you install the extension, open the DevTools and choose the **Hints** tool.</span></span>  <span data-ttu-id="ab847-146">Desde aquí, ejecute un examen de sitio personalizable.</span><span class="sxs-lookup"><span data-stu-id="ab847-146">From here, run a customizable site scan.</span></span>  <span data-ttu-id="ab847-147">Dirígete a [webhint.io][WebhintBrowserExtension] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ab847-147">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <a name="3d-view"></a><span data-ttu-id="ab847-148">Vista 3D</span><span class="sxs-lookup"><span data-stu-id="ab847-148">3D View</span></span>  

<span data-ttu-id="ab847-149">Use la **vista 3D** para depurar la aplicación web navegando por el modelo de objetos de documento [\(DOM\)][MDNDocumentObjectModel] o el contexto de apilamiento [de índice z.][MDNZIndex]</span><span class="sxs-lookup"><span data-stu-id="ab847-149">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="La vista 3D en DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   <span data-ttu-id="ab847-151">La vista 3D en DevTools</span><span class="sxs-lookup"><span data-stu-id="ab847-151">The 3D View in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-152">Para obtener acceso a la vista 3D, seleccione `Ctrl`  +  `Shift`  +  `P` , escriba en **Vista 3D** y **seleccione Mostrar vista 3D**.</span><span class="sxs-lookup"><span data-stu-id="ab847-152">To access the 3D View, select `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="ab847-153">El Microsoft Edge está trabajando con el equipo de Chromium en la interfaz de usuario y agregando más funcionalidad a la vista 3D, por lo que envíe sus [comentarios](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="ab847-153">The Microsoft Edge team is working with the Chromium team on the UI and adding more functionality to the 3D View, so please send your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="ab847-154">Chromium problema [#987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="ab847-154">Chromium issue [#987787][CR987787]</span></span>  

### <a name="visual-studio-code-extensions"></a><span data-ttu-id="ab847-155">Visual Studio Code de datos</span><span class="sxs-lookup"><span data-stu-id="ab847-155">Visual Studio Code extensions</span></span>  

<span data-ttu-id="ab847-156">El equipo de DevTools también ha publicado algunas extensiones para [Visual Studio Code][VisualStudioCode] que le permiten usar la potencia de DevTools directamente desde el editor de texto.</span><span class="sxs-lookup"><span data-stu-id="ab847-156">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="ab847-157">Consulte las extensiones siguientes:</span><span class="sxs-lookup"><span data-stu-id="ab847-157">Check out the extensions below:</span></span>  

#### <a name="elements-for-microsoft-edge"></a><span data-ttu-id="ab847-158">Elementos para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ab847-158">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="ab847-159">Use la herramienta Elementos desde dentro de Visual Studio Code agregando la [extensión Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="ab847-159">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="La herramienta Elementos de Visual Studio Code la extensión Elements for Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   <span data-ttu-id="ab847-161">La **herramienta Elementos** de Visual Studio Code la extensión Elements for Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ab847-161">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-162">Para obtener más información, consulte [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="ab847-162">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <a name="debugger-for-microsoft-edge"></a><span data-ttu-id="ab847-163">Depurador de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ab847-163">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="ab847-164">Con la [extensión Depurador para Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code, depura JavaScript que se ejecuta en Microsoft Edge directamente desde Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="ab847-164">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="El depurador de Microsoft Edge de Visual Studio Code" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   <span data-ttu-id="ab847-166">El depurador de Microsoft Edge de Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ab847-166">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-167">Para obtener más información, [consulte cómo depurar][VisualStudioCodeDebuggerEdgeExtension]Microsoft Edge desde Visual Studio Code .</span><span class="sxs-lookup"><span data-stu-id="ab847-167">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <a name="webhint"></a><span data-ttu-id="ab847-168">webhint</span><span class="sxs-lookup"><span data-stu-id="ab847-168">webhint</span></span>  

<span data-ttu-id="ab847-169">La [extensión webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code para `webhint` mejorar la página web mientras la escribe.</span><span class="sxs-lookup"><span data-stu-id="ab847-169">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you are writing it.</span></span>  <span data-ttu-id="ab847-170">Esta extensión ejecuta e informa de diagnósticos en los archivos del área de trabajo en función del `webhint` análisis.</span><span class="sxs-lookup"><span data-stu-id="ab847-170">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="La extensión webhint Visual Studio Code analizar un archivo .tsx en Visual Studio Code" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="ab847-172">La extensión webhint Visual Studio Code análisis de un `.tsx` archivo en Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ab847-172">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-173">[Obtenga más información sobre la Visual Studio Code webhint][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="ab847-173">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <a name="visual-studio-integration"></a><span data-ttu-id="ab847-174">Visual Studio integración</span><span class="sxs-lookup"><span data-stu-id="ab847-174">Visual Studio integration</span></span>  

<span data-ttu-id="ab847-175">En Visual Studio versión 16.2 o posterior de 2019, use el depurador de Visual Studio para depurar JavaScript que se ejecuta en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab847-175">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="ab847-176">[Descarga Visual Studio 2019 para][MicrosoftVisualStudioDownloads] probar esta característica.</span><span class="sxs-lookup"><span data-stu-id="ab847-176">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canary, Dev o Beta" lightbox="../../images/2020/01/vs.msft.png":::
   <span data-ttu-id="ab847-178">Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canary, Dev o Beta</span><span class="sxs-lookup"><span data-stu-id="ab847-178">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-179">[Obtenga más información sobre la depuración Microsoft Edge desde Visual Studio][VisualStudioIndex].</span><span class="sxs-lookup"><span data-stu-id="ab847-179">[Learn more about debugging Microsoft Edge from Visual Studio][VisualStudioIndex].</span></span>  

### <a name="tracking-prevention-console-messages"></a><span data-ttu-id="ab847-180">Seguimiento de mensajes de consola de prevención</span><span class="sxs-lookup"><span data-stu-id="ab847-180">Tracking prevention Console messages</span></span>  

<span data-ttu-id="ab847-181">La prevención de seguimiento es una característica única en Microsoft Edge que le protege de que los sitios web que no ha visitado antes le realicen un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="ab847-181">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you have not visited before.</span></span>  <span data-ttu-id="ab847-182">La configuración predeterminada de prevención de seguimiento es el modo equilibrado, que bloquea los rastreadores de terceros y los rastreadores malintencionados conocidos para una experiencia que equilibra la privacidad y la compatibilidad web.</span><span class="sxs-lookup"><span data-stu-id="ab847-182">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="ab847-183">Para obtener más información sobre la compatibilidad de la página web cuando se \*\*\*\* bloquean determinados rastreadores, se agregaron mensajes de advertencia en la consola cuando se bloquea un rastreador.</span><span class="sxs-lookup"><span data-stu-id="ab847-183">To give you more insight into the compatibility of your web page when certain trackers are blocked, warning messages were added in the **Console** when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Mensajes en la consola cuando la prevención de seguimiento bloquea el acceso al almacenamiento de un rastreador" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   <span data-ttu-id="ab847-185">Mensajes en la **consola cuando** la prevención de seguimiento bloquea el acceso al almacenamiento de un rastreador</span><span class="sxs-lookup"><span data-stu-id="ab847-185">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-186">[Obtenga más información sobre la prevención de seguimiento y el equilibrio entre privacidad y compatibilidad web.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="ab847-186">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="ab847-187">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="ab847-187">Announcements from the Chromium project</span></span>  

<span data-ttu-id="ab847-188">Las secciones siguientes anuncian características adicionales disponibles en Microsoft Edge 81 que se contribuyeron al proyecto de código Chromium abierto.</span><span class="sxs-lookup"><span data-stu-id="ab847-188">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <a name="moto-g4-support-in-device-mode"></a><span data-ttu-id="ab847-189">Compatibilidad con Moto G4 en modo dispositivo</span><span class="sxs-lookup"><span data-stu-id="ab847-189">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="ab847-190">Después [de habilitar la barra de herramientas de][DevtoolsDeviceModeIndexSimulateMobileViewport]dispositivos, simula las dimensiones de una ventanilla de Moto G4 desde la lista **Dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ab847-190">After [enabling the Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulación de una ventanilla de Moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   <span data-ttu-id="ab847-192">Simulación de una ventanilla de Moto G4</span><span class="sxs-lookup"><span data-stu-id="ab847-192">Simulating a Moto G4 viewport</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-193">Elija [Mostrar marco de dispositivo][DevtoolsDeviceModeIndexShowDeviceFrame] para mostrar el hardware de Moto G4 alrededor de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="ab847-193">Choose [Show Device Frame][DevtoolsDeviceModeIndexShowDeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Mostrar el hardware de Moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   <span data-ttu-id="ab847-195">Mostrar el hardware de Moto G4</span><span class="sxs-lookup"><span data-stu-id="ab847-195">Showing the Moto G4 hardware</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-196">Características relacionadas:</span><span class="sxs-lookup"><span data-stu-id="ab847-196">Related features:</span></span>  

*   <span data-ttu-id="ab847-197">Abra el [menú comando y][DevtoolsCommandMenuIndex] ejecute el comando para realizar una captura de pantalla de la ventanilla que incluye el hardware de Moto `Capture screenshot` G4 (después de habilitar Mostrar marco de **dispositivo**).</span><span class="sxs-lookup"><span data-stu-id="ab847-197">Open the [Command Menu][DevtoolsCommandMenuIndex] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="ab847-198">[Limita la red y la CPU para][DevtoolsDeviceModeIndexThrottleNetworkCpu] simular con mayor precisión las condiciones de navegación web de un usuario móvil.</span><span class="sxs-lookup"><span data-stu-id="ab847-198">[Throttle the network and CPU][DevtoolsDeviceModeIndexThrottleNetworkCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="ab847-199">Chromium problema [#924693][CR924693]</span><span class="sxs-lookup"><span data-stu-id="ab847-199">Chromium issue [#924693][CR924693]</span></span>  

### <a name="cookie-related-updates"></a><span data-ttu-id="ab847-200">Actualizaciones relacionadas con cookies</span><span class="sxs-lookup"><span data-stu-id="ab847-200">Cookie-related updates</span></span>  

#### <a name="blocked-cookies-in-the-cookies-pane"></a><span data-ttu-id="ab847-201">Cookies bloqueadas en el panel Cookies</span><span class="sxs-lookup"><span data-stu-id="ab847-201">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="ab847-202">El panel Cookies del panel Aplicación ahora muestra las cookies bloqueadas con un fondo amarillo.</span><span class="sxs-lookup"><span data-stu-id="ab847-202">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqueadas en el panel Cookies del panel Aplicación" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   <span data-ttu-id="ab847-204">Cookies bloqueadas en el panel Cookies del panel Aplicación</span><span class="sxs-lookup"><span data-stu-id="ab847-204">Blocked cookies in the Cookies pane of the Application panel</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-205">Chromium problema [#1030258][CR1030258]</span><span class="sxs-lookup"><span data-stu-id="ab847-205">Chromium issue [#1030258][CR1030258]</span></span>  <!-- inaccessible  -->  

#### <a name="cookie-priority-in-the-cookie-pane"></a><span data-ttu-id="ab847-206">Prioridad de cookies en el panel Cookie</span><span class="sxs-lookup"><span data-stu-id="ab847-206">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="ab847-207">Las tablas cookies de las **herramientas de red** **y** aplicación ahora incluyen una **columna Prioridad.**</span><span class="sxs-lookup"><span data-stu-id="ab847-207">The Cookies tables in the **Network** and **Application** tools now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="ab847-208">Chromium exploradores basados en cookies, como Microsoft Edge, son los únicos exploradores que admiten la prioridad de cookies.</span><span class="sxs-lookup"><span data-stu-id="ab847-208">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="ab847-209">Chromium problema [#1026879][CR1026879]</span><span class="sxs-lookup"><span data-stu-id="ab847-209">Chromium issue [#1026879][CR1026879]</span></span>  

#### <a name="edit-all-cookie-values"></a><span data-ttu-id="ab847-210">Editar todos los valores de cookie</span><span class="sxs-lookup"><span data-stu-id="ab847-210">Edit all cookie values</span></span>  

<span data-ttu-id="ab847-211">Todas las celdas de las tablas Cookie son editables ahora, excepto las celdas de la columna **Tamaño** porque esa columna representa el tamaño de red de la cookie, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ab847-211">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="ab847-212">Para obtener una explicación de cada columna, vaya a [Campos][DevtoolsStorageCookiesFields].</span><span class="sxs-lookup"><span data-stu-id="ab847-212">For an explanation of each column, navigate to [Fields][DevtoolsStorageCookiesFields].</span></span>  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Edición de un valor de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   <span data-ttu-id="ab847-214">Edición de un valor de cookie</span><span class="sxs-lookup"><span data-stu-id="ab847-214">Editing a cookie value</span></span>  
:::image-end:::  

#### <a name="copy-as-nodejs-fetch-to-include-cookie-data"></a><span data-ttu-id="ab847-215">Copiar como Node.js para incluir datos de cookies</span><span class="sxs-lookup"><span data-stu-id="ab847-215">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="ab847-216">Para obtener una expresión que incluya datos de cookies, mantenga el mouse en una solicitud de red, abra el menú contextual \(hacer clic con el botón secundario\) y elija `fetch` **Copiar**copia como  >  **Node.js capturar**.</span><span class="sxs-lookup"><span data-stu-id="ab847-216">To get a `fetch` expression that includes cookie data, hover on a network request, open the contextual menu \(right-click\), and choose **Copy** > **Copy as Node.js fetch**.</span></span>  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copiar como Node.js captura" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   <span data-ttu-id="ab847-218">Copiar como Node.js captura</span><span class="sxs-lookup"><span data-stu-id="ab847-218">Copy as Node.js fetch</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-219">Chromium problema [#1029826][CR1029826]</span><span class="sxs-lookup"><span data-stu-id="ab847-219">Chromium issue [#1029826][CR1029826]</span></span>  

### <a name="more-accurate-web-app-manifest-icons"></a><span data-ttu-id="ab847-220">Iconos de manifiesto de aplicación web más precisos</span><span class="sxs-lookup"><span data-stu-id="ab847-220">More accurate web app manifest icons</span></span>  

<span data-ttu-id="ab847-221">Anteriormente, el panel Manifiesto del panel Aplicación enviaba sus propias solicitudes para mostrar iconos de manifiesto de aplicación web.</span><span class="sxs-lookup"><span data-stu-id="ab847-221">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="ab847-222">DevTools ahora muestra exactamente el mismo icono de manifiesto que Microsoft Edge usa.</span><span class="sxs-lookup"><span data-stu-id="ab847-222">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Iconos en el panel Manifiesto" lightbox="../../images/2020/01/manifesticons.msft.png":::
   <span data-ttu-id="ab847-224">Iconos en el panel Manifiesto</span><span class="sxs-lookup"><span data-stu-id="ab847-224">Icons in the Manifest pane</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-225">Chromium problema [#985402][CR985402]</span><span class="sxs-lookup"><span data-stu-id="ab847-225">Chromium issue [#985402][CR985402]</span></span>  

### <a name="hover-on-css-content-properties-to-display-unescaped-values"></a><span data-ttu-id="ab847-226">Mantenga el mouse en las propiedades de contenido CSS para mostrar valores sin obtener.</span><span class="sxs-lookup"><span data-stu-id="ab847-226">Hover on CSS content properties to display unescaped values</span></span>  

<span data-ttu-id="ab847-227">Mantenga el mouse sobre el valor de una propiedad para mostrar la versión sin obtener `content` del valor.</span><span class="sxs-lookup"><span data-stu-id="ab847-227">Hover on the value of a `content` property to display the unescaped version of the value.</span></span>  

<span data-ttu-id="ab847-228">Por ejemplo, en esta [demostración][CSSContentDemo] al inspeccionar el pseudo elemento se muestra una cadena de escape `p::after` en el panel **Estilos:**</span><span class="sxs-lookup"><span data-stu-id="ab847-228">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element an escaped string is displayed in the **Styles** pane:</span></span>  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="La cadena de escape" lightbox="../../images/2020/01/escapedstring.msft.png":::
   <span data-ttu-id="ab847-230">La cadena de escape</span><span class="sxs-lookup"><span data-stu-id="ab847-230">The escaped string</span></span>  
:::image-end:::  

<span data-ttu-id="ab847-231">Cuando se mantiene el mouse en el valor, se muestra el valor sin `content` descapote.</span><span class="sxs-lookup"><span data-stu-id="ab847-231">When you hover on the `content` value, the unescaped value is displayed.</span></span>  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="El valor unescaped" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   <span data-ttu-id="ab847-233">El valor unescaped</span><span class="sxs-lookup"><span data-stu-id="ab847-233">The unescaped value</span></span>  
:::image-end:::  

### <a name="more-detailed-source-map-errors-in-the-console"></a><span data-ttu-id="ab847-234">Errores de mapa de origen más detallados en la consola</span><span class="sxs-lookup"><span data-stu-id="ab847-234">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="ab847-235">La consola ahora proporciona más detalles sobre por qué no se pudo cargar o analizar un mapa de origen.</span><span class="sxs-lookup"><span data-stu-id="ab847-235">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="ab847-236">Anteriormente, solo proporcionaba un error sin explicar lo que salió mal.</span><span class="sxs-lookup"><span data-stu-id="ab847-236">Previously it just provided an error without explaining what went wrong.</span></span>  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Error de carga de mapa de origen en la consola" lightbox="../../images/2020/01/sourcemap.msft.png":::
   <span data-ttu-id="ab847-238">Error de carga de mapa de origen en la consola</span><span class="sxs-lookup"><span data-stu-id="ab847-238">A source map loading error in the Console</span></span>  
:::image-end:::  

### <a name="setting-for-disabling-scrolling-past-the-end-of-a-file"></a><span data-ttu-id="ab847-239">Configuración para deshabilitar el desplazamiento más allá del final de un archivo</span><span class="sxs-lookup"><span data-stu-id="ab847-239">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="ab847-240">Abra [Configuración y,][DevtoolsCustomizeIndexSettings] a \*\*\*\* continuación, deshabilite Orígenes de preferencias Permitir el desplazamiento más allá del final del archivo para deshabilitar el comportamiento predeterminado de la interfaz de usuario que le permite desplazarse mucho más allá del final de un archivo en el  >  \*\*\*\*  >  \*\*\*\* panel Orígenes. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ab847-240">Open [Settings][DevtoolsCustomizeIndexSettings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Deshabilitar Permitir el desplazamiento más allá del final del archivo" lightbox="../../images/2020/01/settings.msft.png":::
   <span data-ttu-id="ab847-242">Deshabilitar Permitir **el desplazamiento al final del archivo en** Configuración</span><span class="sxs-lookup"><span data-stu-id="ab847-242">Disabling **Allow scrolling past end of file** in Settings</span></span>  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="El desplazamiento más allá del final de un archivo ahora está deshabilitado en el panel Orígenes" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   <span data-ttu-id="ab847-244">El desplazamiento más allá del final de un archivo ahora está deshabilitado en el panel Orígenes</span><span class="sxs-lookup"><span data-stu-id="ab847-244">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="ab847-245">Descargar los canales de vista previa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ab847-245">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="ab847-246">Si está en Windows o macOS, considere la posibilidad de usar los canales [Microsoft Edge vista previa][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ab847-246">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="ab847-247">Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="ab847-247">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="ab847-248">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ab847-248">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular una ventanilla móvil: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsDeviceModeIndexShowDeviceFrame]: ../../../device-mode/index.md#show-device-frame "Mostrar marco de dispositivo: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCommandMenuIndex]: ../../../command-menu/index.md "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsDeviceModeIndexThrottleNetworkCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Limitar la red y la CPU: simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsStorageCookiesFields]: ../../../storage/cookies.md#fields "Campos: ver, editar y eliminar cookies con Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioIndex]: ../../../../visual-studio/index.md "Visual Studio | Microsoft Docs"  

[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Depurador de Microsoft Edge Visual Studio Code extensión | Microsoft Docs"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elementos para Microsoft Edge Visual Studio Code extensión | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elementos para Microsoft Edge \(Chromium\) | Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"

[TrackingPrevention]: https://blogs.windows.com/msedgedev/2019/12/03/improving-tracking-prevention-microsoft-edge-79 "Mejorar la prevención de seguimiento en Microsoft Edge de blog"

[MicrosoftEdgeInsiderAddons]: https://microsoftedge.microsoft.com/addons/detail/webhint/mlgfbihcfnkaenjpdcngdnhcpkdmcdee "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Descargar Visual Studio 2019 para Windows & Mac"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un Tweet"  

[CR924693]: https://crbug.com/924693 "Solicitud de característica: Agregar Moto G4 a la lista de modo de dispositivo | Chromium Errores"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Chromium Errores"  
[CR1026879]: https://crbug.com/1026879 "La pestaña Cookie de la consola de desarrollo ya no muestra prioridad | Chromium Errores"  
[CR1029826]: https://crbug.com/1029826 "pestaña de red -> derecho elegir solicitar -> copia -> copia ya que la captura no copia las cookies | Chromium Errores"  
[CR985402]: https://crbug.com/985402 "Las cadenas de error de icono de manifiesto de la aplicación web son confusas | Chromium Errores"  
[CR963183]: https://crbug.com/963183 "DevTools no son compatibles con WCAG | Chromium Errores"  
[CR941561]: https://crbug.com/941561 "Localizabilidad del | Chromium Errores"  
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium Errores"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demostración de contenido CSS sin descapote"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nuevo problema: MicrosoftDocs/edge-developer"  

[TheWebWeWant]: https://webwewant.fyi "La web que queremos"  
[AccessibilityInsights]: https://accessibilityinsights.io "Accessibility Insights"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objetos de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "Z-index | MDN"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  

[Webhint]: https://webhint.io "webhint"  

[WebhintBrowserExtension]: https://webhint.io/docs/user-guide/extensions/extension-browser "Extensión de explorador Webhint | documentación de webhint"  
[WebhintVisualStudioCodeExtension]: https://webhint.io/docs/user-guide/extensions/vscode-webhint "Webhint Visual Studio Code extensión | documentación de webhint"  

> [!NOTE]
> <span data-ttu-id="ab847-285">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ab847-285">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ab847-286">La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-81) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="ab847-286">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-81) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ab847-288">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ab847-288">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
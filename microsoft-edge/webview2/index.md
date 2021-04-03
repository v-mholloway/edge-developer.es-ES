---
description: Hospedar contenido web en las aplicaciones de Win32, .NET y UWP con el control WebView2 de Microsoft Edge
title: Microsoft Edge WebView2 Control
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, control de explorador, html perimetral, Windows Forms, WinForms, WPF, .NET, WinUI, Reunión del proyecto
ms.openlocfilehash: 501b6ed3694c66e4c0882550003e636d3b390108
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470817"
---
# <a name="introduction-to-microsoft-edge-webview2"></a><span data-ttu-id="f38b7-104">Introducción a Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="f38b7-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="f38b7-105">El control WebView2 de Microsoft Edge permite insertar tecnologías web \(HTML, CSS y JavaScript\) en las aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="f38b7-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native apps.</span></span>  <span data-ttu-id="f38b7-106">El control WebView2 usa [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] como motor de representación para mostrar el contenido web en aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="f38b7-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native apps.</span></span>  <span data-ttu-id="f38b7-107">Con WebView2, puedes insertar código web en diferentes partes de la aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="f38b7-107">With WebView2, you may embed web code in different parts of your native app.</span></span>  <span data-ttu-id="f38b7-108">Crea toda la aplicación nativa en una sola instancia de WebView.</span><span class="sxs-lookup"><span data-stu-id="f38b7-108">Build all of the native app within a single WebView instance.</span></span>  <span data-ttu-id="f38b7-109">Para obtener información sobre cómo empezar a crear una aplicación WebView2, vaya a [Introducción.](#getting-started)</span><span class="sxs-lookup"><span data-stu-id="f38b7-109">For information on how to start building a WebView2 app, navigate to [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="¿Qué es WebView?" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="f38b7-111">¿Qué es WebView?</span><span class="sxs-lookup"><span data-stu-id="f38b7-111">What is WebView?</span></span>  
:::image-end:::  

## <a name="hybrid-app-approach"></a><span data-ttu-id="f38b7-112">Enfoque de aplicación híbrida</span><span class="sxs-lookup"><span data-stu-id="f38b7-112">Hybrid app approach</span></span>  

<span data-ttu-id="f38b7-113">A menudo, los desarrolladores deben decidir entre crear una aplicación web o una aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="f38b7-113">Developers must often decide between building a web app or a native app.</span></span>  <span data-ttu-id="f38b7-114">La decisión depende del equilibrio entre el alcance y la potencia.</span><span class="sxs-lookup"><span data-stu-id="f38b7-114">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="f38b7-115">Las aplicaciones web permiten un amplio alcance.</span><span class="sxs-lookup"><span data-stu-id="f38b7-115">Web apps allow for a broad reach.</span></span>  <span data-ttu-id="f38b7-116">Como desarrollador web, puede reutilizar la mayor parte del código en diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="f38b7-116">As a Web developer, you may reuse most of your code across different platforms.</span></span>  <span data-ttu-id="f38b7-117">Para acceder a todas las funcionalidades de una plataforma nativa, usa una aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="f38b7-117">To access the all capabilities of a native platform, use a native app.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Nativo web" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="f38b7-119">Nativo web</span><span class="sxs-lookup"><span data-stu-id="f38b7-119">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="f38b7-120">Las aplicaciones híbridas permiten a los desarrolladores disfrutar de lo mejor de ambos mundos.</span><span class="sxs-lookup"><span data-stu-id="f38b7-120">Hybrid apps allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="f38b7-121">Los desarrolladores de aplicaciones híbridas se benefician de las siguientes ventajas.</span><span class="sxs-lookup"><span data-stu-id="f38b7-121">Hybrid app developers benefit from the following advantages.</span></span>  

*   <span data-ttu-id="f38b7-122">La ubicuidad y la fuerza de la plataforma web.</span><span class="sxs-lookup"><span data-stu-id="f38b7-122">The ubiquity and strength of the web platform.</span></span>  
*   <span data-ttu-id="f38b7-123">La potencia y las capacidades completas de la plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="f38b7-123">The power and full capabilities of the native platform.</span></span>  
    
## <a name="webview2-benefits"></a><span data-ttu-id="f38b7-124">Ventajas de WebView2</span><span class="sxs-lookup"><span data-stu-id="f38b7-124">WebView2 benefits</span></span>   

<!--  
:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="WebView reasons" lightbox="./media/WebView2/webviewreasons.png":::
   WebView reasons  
:::image-end:::  
-->  

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset.msft.png":::  
      **<span data-ttu-id="f38b7-125">Ecosistema web \& skillset</span><span class="sxs-lookup"><span data-stu-id="f38b7-125">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="f38b7-126">Use toda la plataforma web, bibliotecas, herramientas y talento que existe en el ecosistema web.</span><span class="sxs-lookup"><span data-stu-id="f38b7-126">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation.msft.png":::  
      **<span data-ttu-id="f38b7-127">Innovación rápida</span><span class="sxs-lookup"><span data-stu-id="f38b7-127">Rapid innovation</span></span>**  
      <span data-ttu-id="f38b7-128">El desarrollo web permite una implementación e iteración más rápidas.</span><span class="sxs-lookup"><span data-stu-id="f38b7-128">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support.msft.png":::  
      **<span data-ttu-id="f38b7-129">Compatibilidad con Windows 7, 8 y 10</span><span class="sxs-lookup"><span data-stu-id="f38b7-129">Windows 7, 8, and 10 support</span></span>**  
      <span data-ttu-id="f38b7-130">Compatibilidad con una experiencia de usuario coherente en Windows 7, Windows 8 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f38b7-130">Support for a consistent user experience across Windows 7, Windows 8, and Windows 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities.msft.png":::  
      **<span data-ttu-id="f38b7-131">Funcionalidades nativas</span><span class="sxs-lookup"><span data-stu-id="f38b7-131">Native capabilities</span></span>**  
      <span data-ttu-id="f38b7-132">Obtenga acceso al conjunto completo de API nativas.</span><span class="sxs-lookup"><span data-stu-id="f38b7-132">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing.msft.png":::  
      **<span data-ttu-id="f38b7-133">Uso compartido de código</span><span class="sxs-lookup"><span data-stu-id="f38b7-133">Code-sharing</span></span>**  
      <span data-ttu-id="f38b7-134">Agregar código web a la base de código permite una mayor reutilización en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="f38b7-134">Add web code to your codebase allows for increased reuse across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support.msft.png":::  
      **<span data-ttu-id="f38b7-135">Soporte técnico de Microsoft</span><span class="sxs-lookup"><span data-stu-id="f38b7-135">Microsoft support</span></span>**  
      <span data-ttu-id="f38b7-136">Microsoft proporciona soporte técnico y agrega nuevas solicitudes de características cuando WebView2 se publica en Disponibilidad general \(GA\).</span><span class="sxs-lookup"><span data-stu-id="f38b7-136">Microsoft provides support and adds new feature requests when WebView2 releases at Generally Availability \(GA\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen.msft.png":::  
      **<span data-ttu-id="f38b7-137">Distribución de Evergreen</span><span class="sxs-lookup"><span data-stu-id="f38b7-137">Evergreen distribution</span></span>**  
      <span data-ttu-id="f38b7-138">Confíe en una versión actualizada de Chromium con actualizaciones de plataforma regulares y revisiones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f38b7-138">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed.msft.png":::  
      **<span data-ttu-id="f38b7-139">Corregido</span><span class="sxs-lookup"><span data-stu-id="f38b7-139">Fixed</span></span>**  
      <span data-ttu-id="f38b7-140">\(próximamente\) Elige empaquetar los bits de Chromium en tu aplicación.</span><span class="sxs-lookup"><span data-stu-id="f38b7-140">\(coming soon\)  Choose to package the Chromium bits in your app.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption.msft.png":::  
      **<span data-ttu-id="f38b7-141">Adopción incremental</span><span class="sxs-lookup"><span data-stu-id="f38b7-141">Incremental adoption</span></span>**  
      <span data-ttu-id="f38b7-142">Agrega componentes web pieza a pieza a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f38b7-142">Add web components piece by piece to your app.</span></span>  
   :::column-end:::
:::row-end:::  

## <a name="getting-started"></a><span data-ttu-id="f38b7-143">Introducción</span><span class="sxs-lookup"><span data-stu-id="f38b7-143">Getting started</span></span>  

<span data-ttu-id="f38b7-144">Para crear y probar la aplicación con el control WebView2, debes tener</span><span class="sxs-lookup"><span data-stu-id="f38b7-144">To build and test your app using the WebView2 control, you need to have</span></span> <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  --><span data-ttu-id="f38b7-145">el [SDK de WebView2][NugetPackagesMicrosoftWebWebView2] instalado.</span><span class="sxs-lookup"><span data-stu-id="f38b7-145">the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="f38b7-146">Seleccione una de las siguientes opciones para empezar.</span><span class="sxs-lookup"><span data-stu-id="f38b7-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="f38b7-147">Introducción a Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="f38b7-147">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="f38b7-148">Introducción a WPF</span><span class="sxs-lookup"><span data-stu-id="f38b7-148">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="f38b7-149">Introducción a WinForms</span><span class="sxs-lookup"><span data-stu-id="f38b7-149">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="f38b7-150">Introducción a WinUI3</span><span class="sxs-lookup"><span data-stu-id="f38b7-150">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="f38b7-151">El repositorio de ejemplos de [WebView2][GithubMicrosoftedgeWebview2samples] contiene ejemplos que muestran todas las características del SDK de WebView2 y los patrones de uso de la API.</span><span class="sxs-lookup"><span data-stu-id="f38b7-151">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="f38b7-152">A medida que se agregan más características al SDK de WebView2, las aplicaciones de ejemplo se actualizarán.</span><span class="sxs-lookup"><span data-stu-id="f38b7-152">As more features are added to the WebView2 SDK, the sample apps will be updated.</span></span>  

## <a name="supported-platforms"></a><span data-ttu-id="f38b7-153">Plataformas compatibles</span><span class="sxs-lookup"><span data-stu-id="f38b7-153">Supported platforms</span></span>  

<span data-ttu-id="f38b7-154">Una versión de disponibilidad general \(GA\) o vista previa está disponible en los siguientes entornos de programación.</span><span class="sxs-lookup"><span data-stu-id="f38b7-154">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="f38b7-155">Win32 C/C++ \(GA\)</span><span class="sxs-lookup"><span data-stu-id="f38b7-155">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="f38b7-156">.NET Framework 4.6.2 o posterior</span><span class="sxs-lookup"><span data-stu-id="f38b7-156">.NET Framework 4.6.2 or later</span></span>  
*   <span data-ttu-id="f38b7-157">.NET Core 3.1 o posterior</span><span class="sxs-lookup"><span data-stu-id="f38b7-157">.NET Core 3.1 or later</span></span>  
*   <span data-ttu-id="f38b7-158">.NET 5</span><span class="sxs-lookup"><span data-stu-id="f38b7-158">.NET 5</span></span>  
*   <span data-ttu-id="f38b7-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span><span class="sxs-lookup"><span data-stu-id="f38b7-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  

<span data-ttu-id="f38b7-160">Puedes ejecutar aplicaciones webView2 en las siguientes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="f38b7-160">You may run WebView2 apps on the following versions of Windows.</span></span>  

*   <span data-ttu-id="f38b7-161">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f38b7-161">Windows 10</span></span>  
*   <span data-ttu-id="f38b7-162">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f38b7-162">Windows 8.1</span></span>  
*   <span data-ttu-id="f38b7-163">Windows 7 \*\*</span><span class="sxs-lookup"><span data-stu-id="f38b7-163">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="f38b7-164">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="f38b7-164">Windows Server 2019</span></span>  
*   <span data-ttu-id="f38b7-165">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f38b7-165">Windows Server 2016</span></span>  
*   <span data-ttu-id="f38b7-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f38b7-166">Windows Server 2012</span></span>  
*   <span data-ttu-id="f38b7-167">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f38b7-167">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="f38b7-168">Windows Server 2008 R2 \*\*</span><span class="sxs-lookup"><span data-stu-id="f38b7-168">Windows Server 2008 R2 \*\*</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="f38b7-169">\*\* La compatibilidad con WebView2 para Windows 7 y Windows Server 2008 R2 tiene el mismo ciclo de compatibilidad que Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f38b7-169">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="f38b7-170">Para obtener más información, vaya a [Sistemas operativos compatibles con Microsoft Edge.][DeployedgeMicrosoftEdgeSupportedOS]</span><span class="sxs-lookup"><span data-stu-id="f38b7-170">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <a name="next-steps"></a><span data-ttu-id="f38b7-171">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="f38b7-171">Next steps</span></span>  

<span data-ttu-id="f38b7-172">Para obtener más información sobre cómo crear e implementar aplicaciones webView2, revise la documentación conceptual y las guías de cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="f38b7-172">For more information on how to build and deploy WebView2 apps, review the conceptual documentation and how-to guides.</span></span>  

#### <a name="concepts"></a><span data-ttu-id="f38b7-173">Conceptos</span><span class="sxs-lookup"><span data-stu-id="f38b7-173">Concepts</span></span>  

*   [<span data-ttu-id="f38b7-174">Comprender las versiones del SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="f38b7-174">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]  
*   [<span data-ttu-id="f38b7-175">Distribución de aplicaciones con WebView2</span><span class="sxs-lookup"><span data-stu-id="f38b7-175">Distribution of apps using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="f38b7-176">Procedimientos recomendados para desarrollar aplicaciones webview2 seguras</span><span class="sxs-lookup"><span data-stu-id="f38b7-176">Best practices for developing secure WebView2 apps</span></span>][Webview2ConceptsSecurity]  
*   [<span data-ttu-id="f38b7-177">Administrar carpeta de datos de usuario en aplicaciones webView2</span><span class="sxs-lookup"><span data-stu-id="f38b7-177">Manage User Data Folder in WebView2 apps</span></span>][Webview2ConceptsUserdatafolder]  
 
#### <a name="how-to-guides"></a><span data-ttu-id="f38b7-178">How-To guías</span><span class="sxs-lookup"><span data-stu-id="f38b7-178">How-To guides</span></span>  

*   [<span data-ttu-id="f38b7-179">Cómo depurar con WebView2</span><span class="sxs-lookup"><span data-stu-id="f38b7-179">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="f38b7-180">Automatizar y probar WebView2 con controlador de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f38b7-180">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="f38b7-181">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="f38b7-181">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribución de aplicaciones con WebView2 | Microsoft Docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Procedimientos recomendados para desarrollar aplicaciones webview2 seguras | Microsoft Docs"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Administración de la carpeta de datos de usuario | Microsoft Docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprender las versiones del SDK de WebView2 | Microsoft Docs"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Introducción a WebView2 | Microsoft Docs"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Introducción a WebView2 en aplicaciones de Windows Forms (versión preliminar) | Microsoft Docs"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Introducción a WebView2 en WinUI3 (versión preliminar) | Microsoft Docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Introducción a WebView2 en WPF (versión preliminar) | Microsoft Docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Cómo depurar con WebView2 | Microsoft Docs"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatizar y probar WebView2 con controladores de Microsoft Edge | Microsoft Docs"  
[Webview2Releasenotes]: ./releasenotes.md "Notas de la versión de WebView2 SDK | Microsoft Docs"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows UI Library 3 Preview 2 (julio de 2020) | Microsoft Docs"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Sistemas operativos compatibles con Microsoft Edge | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | Galería nuGet"  

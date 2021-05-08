---
description: Hospedar contenido web en las aplicaciones de Win32, .NET y UWP con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 Control
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, control de explorador, edge html, Windows Forms, WinForms, WPF, .NET, WinUI, Project Reunion
ms.openlocfilehash: 154c18a3cc9236a8abd286918d72e1a1968fea38
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535735"
---
# <a name="introduction-to-microsoft-edge-webview2"></a><span data-ttu-id="5495b-104">Introducción a Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="5495b-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="5495b-105">El Microsoft Edge WebView2 permite insertar tecnologías web \(HTML, CSS y JavaScript\) en las aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="5495b-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native apps.</span></span>  <span data-ttu-id="5495b-106">El control WebView2 [usa Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] como motor de representación para mostrar el contenido web en aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="5495b-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native apps.</span></span>  <span data-ttu-id="5495b-107">Con WebView2, puedes insertar código web en diferentes partes de la aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="5495b-107">With WebView2, you may embed web code in different parts of your native app.</span></span>  <span data-ttu-id="5495b-108">Crea toda la aplicación nativa en una sola instancia de WebView.</span><span class="sxs-lookup"><span data-stu-id="5495b-108">Build all of the native app within a single WebView instance.</span></span>  <span data-ttu-id="5495b-109">Para obtener información sobre cómo empezar a crear una aplicación WebView2, vaya a [Introducción](#get-started).</span><span class="sxs-lookup"><span data-stu-id="5495b-109">For information on how to start building a WebView2 app, navigate to [Get Started](#get-started).</span></span>  

:::image type="complex" source="./media/WebView2/what-webview.png" alt-text="¿Qué es WebView?" lightbox="./media/WebView2/what-webview.png":::
   <span data-ttu-id="5495b-111">¿Qué es WebView?</span><span class="sxs-lookup"><span data-stu-id="5495b-111">What is WebView?</span></span>  
:::image-end:::    

## <a name="hybrid-app-approach"></a><span data-ttu-id="5495b-112">Enfoque de aplicación híbrida</span><span class="sxs-lookup"><span data-stu-id="5495b-112">Hybrid app approach</span></span>  

<span data-ttu-id="5495b-113">A menudo, los desarrolladores deben decidir entre crear una aplicación web o una aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="5495b-113">Developers must often decide between building a web app or a native app.</span></span>  <span data-ttu-id="5495b-114">La decisión depende del equilibrio entre el alcance y la potencia.</span><span class="sxs-lookup"><span data-stu-id="5495b-114">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="5495b-115">Las aplicaciones web permiten un amplio alcance.</span><span class="sxs-lookup"><span data-stu-id="5495b-115">Web apps allow for a broad reach.</span></span>  <span data-ttu-id="5495b-116">Como desarrollador web, puede reutilizar la mayor parte del código en diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="5495b-116">As a Web developer, you may reuse most of your code across different platforms.</span></span>  <span data-ttu-id="5495b-117">Para acceder a todas las funcionalidades de una plataforma nativa, usa una aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="5495b-117">To access the all capabilities of a native platform, use a native app.</span></span>  

:::image type="complex" source="./media/WebView2/web-native.png" alt-text="Nativo web" lightbox="./media/WebView2/web-native.png":::
   <span data-ttu-id="5495b-119">Nativo web</span><span class="sxs-lookup"><span data-stu-id="5495b-119">Web native</span></span>  
:::image-end:::    

<span data-ttu-id="5495b-120">Las aplicaciones híbridas permiten a los desarrolladores disfrutar de lo mejor de ambos mundos.</span><span class="sxs-lookup"><span data-stu-id="5495b-120">Hybrid apps allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="5495b-121">Los desarrolladores de aplicaciones híbridas se benefician de las siguientes ventajas.</span><span class="sxs-lookup"><span data-stu-id="5495b-121">Hybrid app developers benefit from the following advantages.</span></span>  

*   <span data-ttu-id="5495b-122">La ubicuidad y la fuerza de la plataforma web.</span><span class="sxs-lookup"><span data-stu-id="5495b-122">The ubiquity and strength of the web platform.</span></span>  
*   <span data-ttu-id="5495b-123">La potencia y las capacidades completas de la plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="5495b-123">The power and full capabilities of the native platform.</span></span>  
    
## <a name="webview2-benefits"></a><span data-ttu-id="5495b-124">Ventajas de WebView2</span><span class="sxs-lookup"><span data-stu-id="5495b-124">WebView2 benefits</span></span>   

<!--  
:::image type="complex" source="./media/WebView2/webview-reasons.png" alt-text="WebView reasons" lightbox="./media/WebView2/webview-reasons.png":::
   WebView reasons  
:::image-end:::    
-->  

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset.msft.png":::  
      **<span data-ttu-id="5495b-125">Ecosistema web \& skillset</span><span class="sxs-lookup"><span data-stu-id="5495b-125">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="5495b-126">Use toda la plataforma web, bibliotecas, herramientas y talento que existe en el ecosistema web.</span><span class="sxs-lookup"><span data-stu-id="5495b-126">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation.msft.png":::  
      **<span data-ttu-id="5495b-127">Innovación rápida</span><span class="sxs-lookup"><span data-stu-id="5495b-127">Rapid innovation</span></span>**  
      <span data-ttu-id="5495b-128">El desarrollo web permite una implementación e iteración más rápidas.</span><span class="sxs-lookup"><span data-stu-id="5495b-128">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support.msft.png":::  
      **<span data-ttu-id="5495b-129">Windows compatibilidad con 7, 8 y 10</span><span class="sxs-lookup"><span data-stu-id="5495b-129">Windows 7, 8, and 10 support</span></span>**  
      <span data-ttu-id="5495b-130">Compatibilidad con una experiencia de usuario coherente en Windows 7, Windows 8 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5495b-130">Support for a consistent user experience across Windows 7, Windows 8, and Windows 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities.msft.png":::  
      **<span data-ttu-id="5495b-131">Funcionalidades nativas</span><span class="sxs-lookup"><span data-stu-id="5495b-131">Native capabilities</span></span>**  
      <span data-ttu-id="5495b-132">Obtenga acceso al conjunto completo de API nativas.</span><span class="sxs-lookup"><span data-stu-id="5495b-132">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing.msft.png":::  
      **<span data-ttu-id="5495b-133">Uso compartido de código</span><span class="sxs-lookup"><span data-stu-id="5495b-133">Code-sharing</span></span>**  
      <span data-ttu-id="5495b-134">Agregar código web a la base de código permite una mayor reutilización en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="5495b-134">Add web code to your codebase allows for increased reuse across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support.msft.png":::  
      **<span data-ttu-id="5495b-135">Soporte técnico de Microsoft</span><span class="sxs-lookup"><span data-stu-id="5495b-135">Microsoft support</span></span>**  
      <span data-ttu-id="5495b-136">Microsoft proporciona soporte técnico y agrega nuevas solicitudes de características cuando WebView2 se publica en Disponibilidad general \(GA\).</span><span class="sxs-lookup"><span data-stu-id="5495b-136">Microsoft provides support and adds new feature requests when WebView2 releases at Generally Availability \(GA\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen.msft.png":::  
      **<span data-ttu-id="5495b-137">Distribución de Evergreen</span><span class="sxs-lookup"><span data-stu-id="5495b-137">Evergreen distribution</span></span>**  
      <span data-ttu-id="5495b-138">Confíe en una versión actualizada de Chromium actualizaciones de plataforma y revisiones de seguridad normales.</span><span class="sxs-lookup"><span data-stu-id="5495b-138">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed.msft.png":::  
      **<span data-ttu-id="5495b-139">Corregido</span><span class="sxs-lookup"><span data-stu-id="5495b-139">Fixed</span></span>**  
      <span data-ttu-id="5495b-140">\(coming soon\) Elige empaquetar los Chromium bits de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5495b-140">\(coming soon\)  Choose to package the Chromium bits in your app.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption.msft.png":::  
      **<span data-ttu-id="5495b-141">Adopción incremental</span><span class="sxs-lookup"><span data-stu-id="5495b-141">Incremental adoption</span></span>**  
      <span data-ttu-id="5495b-142">Agrega componentes web pieza a pieza a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5495b-142">Add web components piece by piece to your app.</span></span>  
   :::column-end:::
:::row-end:::  

## <a name="get-started"></a><span data-ttu-id="5495b-143">Comenzar</span><span class="sxs-lookup"><span data-stu-id="5495b-143">Get started</span></span>  

<span data-ttu-id="5495b-144">Para crear y probar la aplicación con el control WebView2, debes tener</span><span class="sxs-lookup"><span data-stu-id="5495b-144">To build and test your app using the WebView2 control, you need to have</span></span> <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  --><span data-ttu-id="5495b-145">el [SDK de WebView2][NugetPackagesMicrosoftWebWebView2] instalado.</span><span class="sxs-lookup"><span data-stu-id="5495b-145">the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="5495b-146">Seleccione una de las siguientes opciones para empezar.</span><span class="sxs-lookup"><span data-stu-id="5495b-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="5495b-147">Introducción con Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="5495b-147">Get Started with Win32 C/C++</span></span>][Webview2GetStartedWin32]  
*   [<span data-ttu-id="5495b-148">Introducción wpf</span><span class="sxs-lookup"><span data-stu-id="5495b-148">Get Started with WPF</span></span>][Webview2GetStartedWpf]  
*   [<span data-ttu-id="5495b-149">Introducción con WinForms</span><span class="sxs-lookup"><span data-stu-id="5495b-149">Get Started with WinForms</span></span>][Webview2GetStartedWinforms]  
*   [<span data-ttu-id="5495b-150">Introducción con WinUI3</span><span class="sxs-lookup"><span data-stu-id="5495b-150">Get Started with WinUI3</span></span>][Webview2GetStartedWinui]  
    
<span data-ttu-id="5495b-151">El repositorio de ejemplos de [WebView2][GithubMicrosoftedgeWebview2samples] contiene ejemplos que muestran todas las características del SDK de WebView2 y los patrones de uso de la API.</span><span class="sxs-lookup"><span data-stu-id="5495b-151">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="5495b-152">A medida que se agregan más características al SDK de WebView2, las aplicaciones de ejemplo se actualizarán.</span><span class="sxs-lookup"><span data-stu-id="5495b-152">As more features are added to the WebView2 SDK, the sample apps will be updated.</span></span>  

## <a name="supported-platforms"></a><span data-ttu-id="5495b-153">Plataformas compatibles</span><span class="sxs-lookup"><span data-stu-id="5495b-153">Supported platforms</span></span>  

<span data-ttu-id="5495b-154">Una versión de disponibilidad general \(GA\) o vista previa está disponible en los siguientes entornos de programación.</span><span class="sxs-lookup"><span data-stu-id="5495b-154">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="5495b-155">Win32 C/C++ \(GA\)</span><span class="sxs-lookup"><span data-stu-id="5495b-155">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="5495b-156">.NET Framework 4.5 o posterior</span><span class="sxs-lookup"><span data-stu-id="5495b-156">.NET Framework 4.5 or later</span></span>  
*   <span data-ttu-id="5495b-157">.NET Core 3.1 o posterior</span><span class="sxs-lookup"><span data-stu-id="5495b-157">.NET Core 3.1 or later</span></span>  
*   <span data-ttu-id="5495b-158">.NET 5</span><span class="sxs-lookup"><span data-stu-id="5495b-158">.NET 5</span></span>  
*   <span data-ttu-id="5495b-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span><span class="sxs-lookup"><span data-stu-id="5495b-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  
    
<span data-ttu-id="5495b-160">Puede ejecutar aplicaciones webView2 en las siguientes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="5495b-160">You may run WebView2 apps on the following versions of Windows.</span></span>  

*   <span data-ttu-id="5495b-161">Windows 10</span><span class="sxs-lookup"><span data-stu-id="5495b-161">Windows 10</span></span>  
*   <span data-ttu-id="5495b-162">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5495b-162">Windows 8.1</span></span>  
*   <span data-ttu-id="5495b-163">Windows 7 \*\*</span><span class="sxs-lookup"><span data-stu-id="5495b-163">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="5495b-164">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="5495b-164">Windows Server 2019</span></span>  
*   <span data-ttu-id="5495b-165">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5495b-165">Windows Server 2016</span></span>  
*   <span data-ttu-id="5495b-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5495b-166">Windows Server 2012</span></span>  
*   <span data-ttu-id="5495b-167">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5495b-167">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="5495b-168">Windows Server 2008 R2 \*\*</span><span class="sxs-lookup"><span data-stu-id="5495b-168">Windows Server 2008 R2 \*\*</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="5495b-169">\*\* La compatibilidad con WebView2 para Windows 7 y Windows Server 2008 R2 tiene el mismo ciclo de compatibilidad que Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5495b-169">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="5495b-170">Para obtener más información, vaya [a Microsoft Edge sistemas operativos compatibles.][DeployedgeMicrosoftEdgeSupportedOS]</span><span class="sxs-lookup"><span data-stu-id="5495b-170">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <a name="next-steps"></a><span data-ttu-id="5495b-171">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="5495b-171">Next steps</span></span>  

<span data-ttu-id="5495b-172">Para obtener más información sobre cómo crear e implementar aplicaciones webView2, revise la documentación conceptual y las guías de cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="5495b-172">For more information on how to build and deploy WebView2 apps, review the conceptual documentation and how-to guides.</span></span>  

### <a name="concepts"></a><span data-ttu-id="5495b-173">Conceptos</span><span class="sxs-lookup"><span data-stu-id="5495b-173">Concepts</span></span>  

*   [<span data-ttu-id="5495b-174">Comprender las versiones del SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="5495b-174">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]  
*   [<span data-ttu-id="5495b-175">Distribución de aplicaciones con WebView2</span><span class="sxs-lookup"><span data-stu-id="5495b-175">Distribution of apps using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="5495b-176">Procedimientos recomendados para desarrollar aplicaciones webview2 seguras</span><span class="sxs-lookup"><span data-stu-id="5495b-176">Best practices for developing secure WebView2 apps</span></span>][Webview2ConceptsSecurity]  
*   [<span data-ttu-id="5495b-177">Administrar carpeta de datos de usuario en aplicaciones webView2</span><span class="sxs-lookup"><span data-stu-id="5495b-177">Manage User Data Folder in WebView2 apps</span></span>][Webview2ConceptsUserDataFolder]  
 
### <a name="how-to-guides"></a><span data-ttu-id="5495b-178">How-To guías</span><span class="sxs-lookup"><span data-stu-id="5495b-178">How-To guides</span></span>  

*   [<span data-ttu-id="5495b-179">Cómo depurar con WebView2</span><span class="sxs-lookup"><span data-stu-id="5495b-179">How to Debug with WebView2</span></span>][Webview2HowToDebug]  
*   [<span data-ttu-id="5495b-180">Automatizar y probar WebView2 con Microsoft Edge controlador</span><span class="sxs-lookup"><span data-stu-id="5495b-180">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowToWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="5495b-181">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="5495b-181">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribución de aplicaciones con WebView2 | Microsoft Docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Procedimientos recomendados para desarrollar aplicaciones webview2 seguras | Microsoft Docs"  
[Webview2ConceptsUserDataFolder]: ./concepts/user-data-folder.md "Administrar la carpeta de datos de usuario | Microsoft Docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprender las versiones del SDK de WebView2 | Microsoft Docs"  
[Webview2GetStartedWin32]: ./get-started/win32.md "Introducción a WebView2 | Microsoft Docs"  
[Webview2GetStartedWinforms]: ./get-started/winforms.md "Introducción a WebView2 en Windows forms (versión preliminar) | Microsoft Docs"  
[Webview2GetStartedWinui]: ./get-started/winui.md "Introducción a WebView2 en WinUI3 (versión preliminar) | Microsoft Docs"  
[Webview2GetStartedWpf]: ./get-started/wpf.md "Introducción a WebView2 en WPF (versión preliminar) | Microsoft Docs"  
[Webview2HowToDebug]: ./how-to/debug.md "Cómo depurar con WebView2 | Microsoft Docs"  
[Webview2HowToWebdriver]: ./how-to/webdriver.md "Automatizar y probar WebView2 con Microsoft Edge driver | Microsoft Docs"  
[Webview2ReleaseNotes]: ./release-notes.md "Notas de la versión de WebView2 SDK | Microsoft Docs"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows Biblioteca de interfaz de usuario 3 Versión preliminar 2 (julio de 2020) | Microsoft Docs"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Microsoft Edge sistemas operativos compatibles | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | NuGet Galería"  

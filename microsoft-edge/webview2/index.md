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
ms.openlocfilehash: 9c1aa073294fc649223da19c44850dc4335f6c00
ms.sourcegitcommit: 7f7922dbb6af87ecac1378d18359125770c5b8e5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536873"
---
# <a name="introduction-to-microsoft-edge-webview2"></a><span data-ttu-id="e9ca1-104">Introducción a Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="e9ca1-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="e9ca1-105">El Microsoft Edge WebView2 permite insertar tecnologías web \(HTML, CSS y JavaScript\) en las aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-105">The Microsoft Edge WebView2 control allows you to embed web technologies \(HTML, CSS, and JavaScript\) in your native apps.</span></span>  <span data-ttu-id="e9ca1-106">El control WebView2 [usa Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] como motor de representación para mostrar el contenido web en aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native apps.</span></span>  <span data-ttu-id="e9ca1-107">Con WebView2, puedes insertar código web en diferentes partes de la aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-107">With WebView2, you may embed web code in different parts of your native app.</span></span>  <span data-ttu-id="e9ca1-108">Crea toda la aplicación nativa en una sola instancia de WebView.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-108">Build all of the native app within a single WebView instance.</span></span>  <span data-ttu-id="e9ca1-109">Para obtener información sobre cómo empezar a crear una aplicación WebView2, vaya a [Introducción](#get-started).</span><span class="sxs-lookup"><span data-stu-id="e9ca1-109">For information on how to start building a WebView2 app, navigate to [Get Started](#get-started).</span></span>  

:::image type="complex" source="./media/WebView2/what-webview.png" alt-text="¿Qué es WebView?" lightbox="./media/WebView2/what-webview.png":::
   <span data-ttu-id="e9ca1-111">¿Qué es WebView?</span><span class="sxs-lookup"><span data-stu-id="e9ca1-111">What is WebView?</span></span>  
:::image-end:::    

## <a name="hybrid-app-approach"></a><span data-ttu-id="e9ca1-112">Enfoque de aplicación híbrida</span><span class="sxs-lookup"><span data-stu-id="e9ca1-112">Hybrid app approach</span></span>  

<span data-ttu-id="e9ca1-113">A menudo, los desarrolladores deben decidir entre crear una aplicación web o una aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-113">Developers must often decide between building a web app or a native app.</span></span>  <span data-ttu-id="e9ca1-114">La decisión depende del equilibrio entre el alcance y la potencia.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-114">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="e9ca1-115">Las aplicaciones web permiten un amplio alcance.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-115">Web apps allow for a broad reach.</span></span>  <span data-ttu-id="e9ca1-116">Como desarrollador web, puede reutilizar la mayor parte del código en diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-116">As a Web developer, you may reuse most of your code across different platforms.</span></span>  <span data-ttu-id="e9ca1-117">Para acceder a todas las funcionalidades de una plataforma nativa, usa una aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-117">To access the all capabilities of a native platform, use a native app.</span></span>  

:::image type="complex" source="./media/WebView2/web-native.png" alt-text="Nativo web" lightbox="./media/WebView2/web-native.png":::
   <span data-ttu-id="e9ca1-119">Nativo web</span><span class="sxs-lookup"><span data-stu-id="e9ca1-119">Web native</span></span>  
:::image-end:::    

<span data-ttu-id="e9ca1-120">Las aplicaciones híbridas permiten a los desarrolladores disfrutar de lo mejor de ambos mundos.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-120">Hybrid apps allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="e9ca1-121">Los desarrolladores de aplicaciones híbridas se benefician de las siguientes ventajas.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-121">Hybrid app developers benefit from the following advantages.</span></span>  

*   <span data-ttu-id="e9ca1-122">La ubicuidad y la fuerza de la plataforma web.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-122">The ubiquity and strength of the web platform.</span></span>  
*   <span data-ttu-id="e9ca1-123">La potencia y las capacidades completas de la plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-123">The power and full capabilities of the native platform.</span></span>  
    
## <a name="webview2-benefits"></a><span data-ttu-id="e9ca1-124">Ventajas de WebView2</span><span class="sxs-lookup"><span data-stu-id="e9ca1-124">WebView2 benefits</span></span>   

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="web-ecosystem--skillset"></a><span data-ttu-id="e9ca1-125">Conjunto de aptitudes & web</span><span class="sxs-lookup"><span data-stu-id="e9ca1-125">Web ecosystem & skillset</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="rapid-innovation"></a><span data-ttu-id="e9ca1-126">Innovación rápida</span><span class="sxs-lookup"><span data-stu-id="e9ca1-126">Rapid innovation</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="windows-7-8-and-10-support"></a><span data-ttu-id="e9ca1-127">Windows compatibilidad con 7, 8 y 10</span><span class="sxs-lookup"><span data-stu-id="e9ca1-127">Windows 7, 8, and 10 support</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="e9ca1-128">Use toda la plataforma web, bibliotecas, herramientas y talento que existe en el ecosistema web.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-128">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="e9ca1-129">El desarrollo web permite una implementación e iteración más rápidas.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-129">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="e9ca1-130">Compatibilidad con una experiencia de usuario coherente en Windows 7, Windows 8 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-130">Support for a consistent user experience across Windows 7, Windows 8, and Windows 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="native-capabilities"></a><span data-ttu-id="e9ca1-131">Funcionalidades nativas</span><span class="sxs-lookup"><span data-stu-id="e9ca1-131">Native capabilities</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="code-sharing"></a><span data-ttu-id="e9ca1-132">Uso compartido de código</span><span class="sxs-lookup"><span data-stu-id="e9ca1-132">Code-sharing</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="microsoft-support"></a><span data-ttu-id="e9ca1-133">Soporte técnico de Microsoft</span><span class="sxs-lookup"><span data-stu-id="e9ca1-133">Microsoft support</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="e9ca1-134">Obtenga acceso al conjunto completo de API nativas.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-134">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="e9ca1-135">Agregar código web a la base de código permite una mayor reutilización en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-135">Add web code to your codebase allows for increased reuse across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="e9ca1-136">Microsoft proporciona soporte técnico y agrega nuevas solicitudes de características cuando WebView2 se publica en Disponibilidad general \(GA\).</span><span class="sxs-lookup"><span data-stu-id="e9ca1-136">Microsoft provides support and adds new feature requests when WebView2 releases at Generally Availability \(GA\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="evergreen-distribution"></a><span data-ttu-id="e9ca1-137">Distribución de Evergreen</span><span class="sxs-lookup"><span data-stu-id="e9ca1-137">Evergreen distribution</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="fixed"></a><span data-ttu-id="e9ca1-138">Corregido</span><span class="sxs-lookup"><span data-stu-id="e9ca1-138">Fixed</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="incremental-adoption"></a><span data-ttu-id="e9ca1-139">Adopción incremental</span><span class="sxs-lookup"><span data-stu-id="e9ca1-139">Incremental adoption</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="e9ca1-140">Confíe en una versión actualizada de Chromium actualizaciones de plataforma y revisiones de seguridad normales.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-140">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="e9ca1-141">\(coming soon\) Elige empaquetar los Chromium bits de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-141">\(coming soon\)  Choose to package the Chromium bits in your app.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="e9ca1-142">Agrega componentes web pieza a pieza a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-142">Add web components piece by piece to your app.</span></span>  
   :::column-end:::
:::row-end:::  

## <a name="get-started"></a><span data-ttu-id="e9ca1-143">Comenzar</span><span class="sxs-lookup"><span data-stu-id="e9ca1-143">Get started</span></span>  

<span data-ttu-id="e9ca1-144">Para crear y probar la aplicación con el control WebView2, debes tener</span><span class="sxs-lookup"><span data-stu-id="e9ca1-144">To build and test your app using the WebView2 control, you need to have</span></span> <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  --><span data-ttu-id="e9ca1-145">el [SDK de WebView2][NugetPackagesMicrosoftWebWebView2] instalado.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-145">the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="e9ca1-146">Seleccione una de las siguientes opciones para empezar.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="e9ca1-147">Introducción con Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="e9ca1-147">Get Started with Win32 C/C++</span></span>][Webview2GetStartedWin32]  
*   [<span data-ttu-id="e9ca1-148">Introducción wpf</span><span class="sxs-lookup"><span data-stu-id="e9ca1-148">Get Started with WPF</span></span>][Webview2GetStartedWpf]  
*   [<span data-ttu-id="e9ca1-149">Introducción con WinForms</span><span class="sxs-lookup"><span data-stu-id="e9ca1-149">Get Started with WinForms</span></span>][Webview2GetStartedWinforms]  
*   [<span data-ttu-id="e9ca1-150">Introducción con WinUI3</span><span class="sxs-lookup"><span data-stu-id="e9ca1-150">Get Started with WinUI3</span></span>][Webview2GetStartedWinui]  
    
<span data-ttu-id="e9ca1-151">El repositorio de ejemplos de [WebView2][GithubMicrosoftedgeWebview2samples] contiene ejemplos que muestran todas las características del SDK de WebView2 y los patrones de uso de la API.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-151">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="e9ca1-152">A medida que se agregan más características al SDK de WebView2, las aplicaciones de ejemplo se actualizarán.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-152">As more features are added to the WebView2 SDK, the sample apps will be updated.</span></span>  

## <a name="supported-platforms"></a><span data-ttu-id="e9ca1-153">Plataformas compatibles</span><span class="sxs-lookup"><span data-stu-id="e9ca1-153">Supported platforms</span></span>  

<span data-ttu-id="e9ca1-154">Una versión de disponibilidad general \(GA\) o vista previa está disponible en los siguientes entornos de programación.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-154">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="e9ca1-155">Win32 C/C++ \(GA\)</span><span class="sxs-lookup"><span data-stu-id="e9ca1-155">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="e9ca1-156">.NET Framework 4.5 o posterior</span><span class="sxs-lookup"><span data-stu-id="e9ca1-156">.NET Framework 4.5 or later</span></span>  
*   <span data-ttu-id="e9ca1-157">.NET Core 3.1 o posterior</span><span class="sxs-lookup"><span data-stu-id="e9ca1-157">.NET Core 3.1 or later</span></span>  
*   <span data-ttu-id="e9ca1-158">.NET 5</span><span class="sxs-lookup"><span data-stu-id="e9ca1-158">.NET 5</span></span>  
*   <span data-ttu-id="e9ca1-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span><span class="sxs-lookup"><span data-stu-id="e9ca1-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  
    
<span data-ttu-id="e9ca1-160">Puede ejecutar aplicaciones webView2 en las siguientes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-160">You may run WebView2 apps on the following versions of Windows.</span></span>  

*   <span data-ttu-id="e9ca1-161">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e9ca1-161">Windows 10</span></span>  
*   <span data-ttu-id="e9ca1-162">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e9ca1-162">Windows 8.1</span></span>  
*   <span data-ttu-id="e9ca1-163">Windows 7 \*\*</span><span class="sxs-lookup"><span data-stu-id="e9ca1-163">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="e9ca1-164">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="e9ca1-164">Windows Server 2019</span></span>  
*   <span data-ttu-id="e9ca1-165">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e9ca1-165">Windows Server 2016</span></span>  
*   <span data-ttu-id="e9ca1-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9ca1-166">Windows Server 2012</span></span>  
*   <span data-ttu-id="e9ca1-167">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e9ca1-167">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="e9ca1-168">Windows Server 2008 R2 \*\*</span><span class="sxs-lookup"><span data-stu-id="e9ca1-168">Windows Server 2008 R2 \*\*</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="e9ca1-169">\*\* La compatibilidad con WebView2 para Windows 7 y Windows Server 2008 R2 tiene el mismo ciclo de compatibilidad que Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-169">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="e9ca1-170">Para obtener más información, vaya [a Microsoft Edge sistemas operativos compatibles.][DeployedgeMicrosoftEdgeSupportedOS]</span><span class="sxs-lookup"><span data-stu-id="e9ca1-170">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <a name="next-steps"></a><span data-ttu-id="e9ca1-171">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="e9ca1-171">Next steps</span></span>  

<span data-ttu-id="e9ca1-172">Para obtener más información sobre cómo crear e implementar aplicaciones webView2, revise la documentación conceptual y las guías de cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-172">For more information on how to build and deploy WebView2 apps, review the conceptual documentation and how-to guides.</span></span>  

### <a name="concepts"></a><span data-ttu-id="e9ca1-173">Conceptos</span><span class="sxs-lookup"><span data-stu-id="e9ca1-173">Concepts</span></span>  

*   [<span data-ttu-id="e9ca1-174">Comprender las versiones del SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="e9ca1-174">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]  
*   [<span data-ttu-id="e9ca1-175">Distribución de aplicaciones con WebView2</span><span class="sxs-lookup"><span data-stu-id="e9ca1-175">Distribution of apps using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="e9ca1-176">Procedimientos recomendados para desarrollar aplicaciones webview2 seguras</span><span class="sxs-lookup"><span data-stu-id="e9ca1-176">Best practices for developing secure WebView2 apps</span></span>][Webview2ConceptsSecurity]  
*   [<span data-ttu-id="e9ca1-177">Administrar carpeta de datos de usuario en aplicaciones webView2</span><span class="sxs-lookup"><span data-stu-id="e9ca1-177">Manage User Data Folder in WebView2 apps</span></span>][Webview2ConceptsUserDataFolder]  
 
### <a name="how-to-guides"></a><span data-ttu-id="e9ca1-178">How-To guías</span><span class="sxs-lookup"><span data-stu-id="e9ca1-178">How-To guides</span></span>  

*   [<span data-ttu-id="e9ca1-179">Cómo depurar con WebView2</span><span class="sxs-lookup"><span data-stu-id="e9ca1-179">How to Debug with WebView2</span></span>][Webview2HowToDebug]  
*   [<span data-ttu-id="e9ca1-180">Automatizar y probar WebView2 con Microsoft Edge controlador</span><span class="sxs-lookup"><span data-stu-id="e9ca1-180">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowToWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="e9ca1-181">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="e9ca1-181">Getting in touch with the Microsoft Edge WebView team</span></span>  

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

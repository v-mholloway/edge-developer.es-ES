---
description: Hospedar contenido web en la aplicación Win32 con el control de WebView 2 de Microsoft Edge
title: Control WebView2 de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, control del explorador, HTML Edge, Windows Forms, WinForms, WPF, .NET
ms.openlocfilehash: ea3d25d16aa9e8c182d564c68615b9643c9993b4
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888601"
---
# <span data-ttu-id="e9c23-104">Introducción a Microsoft Edge WebView2 (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="e9c23-104">Introduction to Microsoft Edge WebView2 (Preview)</span></span>  

<span data-ttu-id="e9c23-105">El control Microsoft Edge WebView2 permite incrustar tecnologías web \ (HTML, CSS y JavaScript \) en las aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="e9c23-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="e9c23-106">El control WebView2 usa [Microsoft Edge (cromo)][MicrosoftedgeinsiderMain] como motor de representación para mostrar el contenido web en aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="e9c23-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="e9c23-107">Con WebView2, puedes incrustar código web en diferentes partes de tu aplicación nativa o compilar toda la aplicación nativa dentro de una sola vista Web.</span><span class="sxs-lookup"><span data-stu-id="e9c23-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="e9c23-108">Para obtener información sobre cómo empezar a crear una aplicación de WebView2, consulte [Introducción](#getting-started).</span><span class="sxs-lookup"><span data-stu-id="e9c23-108">For information on how to start building a WebView2 application, see [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="¿Qué es la vista previa?" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="e9c23-110">¿Qué es la vista previa?</span><span class="sxs-lookup"><span data-stu-id="e9c23-110">What is WebView</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e9c23-111">La vista previa de WebView2 está pensada para el prototipo anticipado y para recopilar comentarios con el fin de ayudar a dar forma a la API.</span><span class="sxs-lookup"><span data-stu-id="e9c23-111">The WebView2 Preview is intended for early prototyping and to gather feedback to help shape the API.</span></span>  <span data-ttu-id="e9c23-112">No debe usar la vista previa en las aplicaciones de producción porque es posible que haya cambios importantes.</span><span class="sxs-lookup"><span data-stu-id="e9c23-112">You should not use the preview in your production apps because there may be breaking changes.</span></span>  <span data-ttu-id="e9c23-113">Para obtener más información, consulte [Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="e9c23-113">For more information, see [Webview2Releasenotes].</span></span>  

## <span data-ttu-id="e9c23-114">Enfoque de aplicaciones híbridas</span><span class="sxs-lookup"><span data-stu-id="e9c23-114">Hybrid application approach</span></span>  

<span data-ttu-id="e9c23-115">Los programadores suelen decidir entre crear una aplicación web o una aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="e9c23-115">Developers often have to decide between building a web application or a native application.</span></span>  <span data-ttu-id="e9c23-116">La decisión depende del equilibrio entre el alcance y el potencial de energía.</span><span class="sxs-lookup"><span data-stu-id="e9c23-116">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="e9c23-117">Las aplicaciones web permiten un amplio alcance.</span><span class="sxs-lookup"><span data-stu-id="e9c23-117">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="e9c23-118">Como desarrollador web, puede volver a usar la mayoría, si no todo el código, en todas las plataformas.</span><span class="sxs-lookup"><span data-stu-id="e9c23-118">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="e9c23-119">Las aplicaciones nativas, sin embargo, usan las capacidades de toda la plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="e9c23-119">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="e9c23-121">Web Native</span><span class="sxs-lookup"><span data-stu-id="e9c23-121">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="e9c23-122">Las aplicaciones híbridas permiten a los desarrolladores disfrutar de lo mejor de ambos mundos.</span><span class="sxs-lookup"><span data-stu-id="e9c23-122">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="e9c23-123">Los programadores de aplicaciones híbridas se benefician de la Ubiquity y fortaleza de la plataforma web, así como de la potencia y capacidades completas de la plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="e9c23-123">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="e9c23-124">Beneficios de WebView2</span><span class="sxs-lookup"><span data-stu-id="e9c23-124">WebView2 benefits</span></span>   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Motivos de la vista en vista previa" lightbox="./media/WebView2/webviewreasons.png":::
   <span data-ttu-id="e9c23-126">Motivos de la vista en vista previa</span><span class="sxs-lookup"><span data-stu-id="e9c23-126">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="e9c23-127">Ecosistema web \ & Aptitudes</span><span class="sxs-lookup"><span data-stu-id="e9c23-127">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="e9c23-128">Use toda la plataforma web, bibliotecas, herramientas y talento que existen en el ecosistema Web.</span><span class="sxs-lookup"><span data-stu-id="e9c23-128">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e9c23-129">Innovación rápida</span><span class="sxs-lookup"><span data-stu-id="e9c23-129">Rapid innovation</span></span>**  
      <span data-ttu-id="e9c23-130">El desarrollo web permite una implementación e iteración más rápidas.</span><span class="sxs-lookup"><span data-stu-id="e9c23-130">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e9c23-131">Compatibilidad con Windows 7, 8, 10</span><span class="sxs-lookup"><span data-stu-id="e9c23-131">Windows 7, 8, 10 support</span></span>**  
      <span data-ttu-id="e9c23-132">Compatibilidad con una experiencia de usuario coherente en Windows 7, 8 y 10.</span><span class="sxs-lookup"><span data-stu-id="e9c23-132">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e9c23-133">Capacidades nativas</span><span class="sxs-lookup"><span data-stu-id="e9c23-133">Native capabilities</span></span>**  
      <span data-ttu-id="e9c23-134">Acceder al conjunto completo de API nativas.</span><span class="sxs-lookup"><span data-stu-id="e9c23-134">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e9c23-135">Uso compartido de código</span><span class="sxs-lookup"><span data-stu-id="e9c23-135">Code-sharing</span></span>**  
      <span data-ttu-id="e9c23-136">Agregar código web a su código base permite un aumento de la reutilización en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="e9c23-136">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e9c23-137">Soporte técnico de Microsoft</span><span class="sxs-lookup"><span data-stu-id="e9c23-137">Microsoft support</span></span>**  
      <span data-ttu-id="e9c23-138">Microsoft proporciona soporte técnico y agrega nuevas solicitudes de características cuando WebView2 se publica como GA.</span><span class="sxs-lookup"><span data-stu-id="e9c23-138">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e9c23-139">Distribución de hoja perenne</span><span class="sxs-lookup"><span data-stu-id="e9c23-139">Evergreen distribution</span></span>**  
      <span data-ttu-id="e9c23-140">Use una versión actualizada de cromo con actualizaciones de plataforma y revisiones de seguridad regulares.</span><span class="sxs-lookup"><span data-stu-id="e9c23-140">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="e9c23-141">**Fijo** \ (próximamente \)</span><span class="sxs-lookup"><span data-stu-id="e9c23-141">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="e9c23-142">Elija empaquetar los bits de cromo en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9c23-142">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="e9c23-143">Adopción incremental</span><span class="sxs-lookup"><span data-stu-id="e9c23-143">Incremental adoption</span></span>**  
      <span data-ttu-id="e9c23-144">Agregue componentes Web por partes a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9c23-144">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="e9c23-145">Introducción</span><span class="sxs-lookup"><span data-stu-id="e9c23-145">Getting started</span></span>  

<span data-ttu-id="e9c23-146">Para compilar y probar la aplicación con el control WebView2, debe tener instalado tanto [Microsoft Edge (cromo)][MicrosoftedgeinsiderDownload] como el [SDK de WebView2][NugetPackagesMicrosoftWebWebView2] .</span><span class="sxs-lookup"><span data-stu-id="e9c23-146">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="e9c23-147">Seleccione una de las siguientes opciones para comenzar.</span><span class="sxs-lookup"><span data-stu-id="e9c23-147">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="e9c23-148">Introducción a Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="e9c23-148">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="e9c23-149">Introducción a WPF</span><span class="sxs-lookup"><span data-stu-id="e9c23-149">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="e9c23-150">Introducción a WinForms</span><span class="sxs-lookup"><span data-stu-id="e9c23-150">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="e9c23-151">Introducción a WinUI3</span><span class="sxs-lookup"><span data-stu-id="e9c23-151">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="e9c23-152">El repositorio de [muestras de WebView2][GithubMicrosoftedgeWebview2samples] contiene ejemplos que muestran todas las características del SDK de WebView2 y los patrones de uso de API.</span><span class="sxs-lookup"><span data-stu-id="e9c23-152">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="e9c23-153">A medida que se agregan más características al SDK de WebView2, se actualizarán las aplicaciones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e9c23-153">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>  

## <span data-ttu-id="e9c23-154">Plataformas compatibles</span><span class="sxs-lookup"><span data-stu-id="e9c23-154">Supported platforms</span></span>  

<span data-ttu-id="e9c23-155">Una vista previa para desarrolladores está disponible en los siguientes entornos de programación.</span><span class="sxs-lookup"><span data-stu-id="e9c23-155">A developer preview is available on the following programming environments.</span></span>  

*   <span data-ttu-id="e9c23-156">C/C++ Win32</span><span class="sxs-lookup"><span data-stu-id="e9c23-156">Win32 C/C++</span></span>  
*   <span data-ttu-id="e9c23-157">.NET Framework 4.6.2 o posterior</span><span class="sxs-lookup"><span data-stu-id="e9c23-157">.NET Framework 4.6.2 or later</span></span>  
*   <span data-ttu-id="e9c23-158">.NET Core 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e9c23-158">.NET Core 3.0 or later</span></span>  
*   [<span data-ttu-id="e9c23-159">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="e9c23-159">WinUI 3.0</span></span>][UwpToolkitsWinui3]  

<span data-ttu-id="e9c23-160">Puede ejecutar aplicaciones de WebView2 en las siguientes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="e9c23-160">You are able to run WebView2 applications on the following versions of Windows.</span></span>  

*   <span data-ttu-id="e9c23-161">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e9c23-161">Windows 10</span></span>  
*   <span data-ttu-id="e9c23-162">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e9c23-162">Windows 8.1</span></span>  
*   <span data-ttu-id="e9c23-163">Windows8</span><span class="sxs-lookup"><span data-stu-id="e9c23-163">Windows 8</span></span>  
*   <span data-ttu-id="e9c23-164">Windows7</span><span class="sxs-lookup"><span data-stu-id="e9c23-164">Windows 7</span></span>  
*   <span data-ttu-id="e9c23-165">WindowsServer2016</span><span class="sxs-lookup"><span data-stu-id="e9c23-165">Windows Server 2016</span></span>  
*   <span data-ttu-id="e9c23-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9c23-166">Windows Server 2012</span></span>  
*   <span data-ttu-id="e9c23-167">Windows Server 2012R2</span><span class="sxs-lookup"><span data-stu-id="e9c23-167">Windows Server 2012R2</span></span>  
*   <span data-ttu-id="e9c23-168">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9c23-168">Windows Server 2008 R2</span></span>  

## <span data-ttu-id="e9c23-169">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="e9c23-169">Next steps</span></span>  

<span data-ttu-id="e9c23-170">Para obtener más información sobre cómo crear e implementar aplicaciones de WebView2, consulte la documentación conceptual y las guías de procedimientos.</span><span class="sxs-lookup"><span data-stu-id="e9c23-170">For more information on how to build and deploy WebView2 applications, review the conceptual documentation and how-to guides.</span></span>  

#### <span data-ttu-id="e9c23-171">Conceptos</span><span class="sxs-lookup"><span data-stu-id="e9c23-171">Concepts</span></span>  

*   [<span data-ttu-id="e9c23-172">Comprender las versiones de SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="e9c23-172">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]
*   [<span data-ttu-id="e9c23-173">Distribución de aplicaciones con WebView2</span><span class="sxs-lookup"><span data-stu-id="e9c23-173">Distribution of applications using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="e9c23-174">Procedimientos recomendados para desarrollar aplicaciones de WebView2 seguras</span><span class="sxs-lookup"><span data-stu-id="e9c23-174">Best practices for developing secure WebView2 applications</span></span>][Webview2ConceptsSecurity]
*   [<span data-ttu-id="e9c23-175">Carpeta administrar datos de usuario en aplicaciones de WebView2</span><span class="sxs-lookup"><span data-stu-id="e9c23-175">Manage User Data Folder in WebView2 Applications</span></span>][Webview2ConceptsUserdatafolder]
 
#### <span data-ttu-id="e9c23-176">Guías de procedimientos</span><span class="sxs-lookup"><span data-stu-id="e9c23-176">How-To guides</span></span>  

*   [<span data-ttu-id="e9c23-177">Cómo depurar con WebView2</span><span class="sxs-lookup"><span data-stu-id="e9c23-177">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="e9c23-178">Automatizar y probar WebView2 con el controlador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e9c23-178">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <span data-ttu-id="e9c23-179">Ponerse en contacto con el equipo de WebView2</span><span class="sxs-lookup"><span data-stu-id="e9c23-179">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="e9c23-180">Ayuda a crear una experiencia WebView2 más rica compartiendo tus comentarios.</span><span class="sxs-lookup"><span data-stu-id="e9c23-180">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="e9c23-181">Para enviar solicitudes de características o informes de errores, vea [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeddback] .</span><span class="sxs-lookup"><span data-stu-id="e9c23-181">To submit feature requests or bug reports, see [WebView feedback repo][GithubMicrosoftedgeWebviewfeddback] .</span></span>  <span data-ttu-id="e9c23-182">También es un buen lugar para buscar problemas conocidos.</span><span class="sxs-lookup"><span data-stu-id="e9c23-182">It's also a good place to search for known issues.</span></span>  

> [!NOTE]
> <span data-ttu-id="e9c23-183">Durante la vista previa, recopilamos datos para ayudar a crear un producto mejor.</span><span class="sxs-lookup"><span data-stu-id="e9c23-183">During the preview, we collect data to help build a better product.</span></span>  <span data-ttu-id="e9c23-184">Para desactivar la recopilación de datos de WebView2, vaya a la `edge://settings/privacy` recopilación de datos del explorador y desactívela.</span><span class="sxs-lookup"><span data-stu-id="e9c23-184">To turn off WebView2 data collection, go to `edge://settings/privacy` and turn off browser data collection.</span></span>  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Procedimientos recomendados para desarrollar aplicaciones de WebView2 seguras | Microsoft docs"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Administración de la carpeta datos de usuario | Microsoft docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprender las versiones de SDK de WebView2 | Microsoft docs"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Introducción a WebView2 (Developer Preview) | Microsoft docs"   
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Introducción a WebView2 en las aplicaciones de Windows Forms (versión preliminar) | Microsoft docs"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Introducción a WebView2 en WinUI3 (vista previa) | Microsoft docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Introducción a WebView2 en WPF (vista previa) | Microsoft docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Cómo depurar con WebView2 | Microsoft docs"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatizar y probar WebView2 con el controlador Microsoft Edge | Microsoft docs"  
[Webview2Releasenotes]: ./releasenotes.md "Notas de la versión de WEBVIEW2RELEASENOTES para WebView2 SDK | Microsoft docs"  

[UwpToolkitsWinui3]: ./gettingstarted/winui.md "Biblioteca de interfaces de usuario de Windows 3 Preview 2 (2020 de julio) | Microsoft docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Insider de Microsoft Edge"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | Galería de NuGet"  

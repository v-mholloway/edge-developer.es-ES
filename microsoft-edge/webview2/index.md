---
description: Hospedar contenido web en tus aplicaciones Win32, .NET y UWP con el control Microsoft Edge WebView2
title: Control WebView2 de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge, Windows Forms, WinForms, WPF, .NET, WinUI, Project reunion
ms.openlocfilehash: 9e5cc3a26f07a11c9fd5c21d62ecafc3ed5103f4
ms.sourcegitcommit: c619168deea44cdec8ebc80ef9ddf1d91d5f726d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/19/2020
ms.locfileid: "11182186"
---
# <span data-ttu-id="b2635-104">Introducción a Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="b2635-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="b2635-105">El control Microsoft Edge WebView2 permite incrustar tecnologías web \ (HTML, CSS y JavaScript \) en las aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="b2635-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="b2635-106">El control WebView2 usa [Microsoft Edge (cromo)][MicrosoftedgeinsiderMain] como motor de representación para mostrar el contenido web en aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="b2635-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="b2635-107">Con WebView2, puedes incrustar código web en diferentes partes de tu aplicación nativa o compilar toda la aplicación nativa dentro de una sola vista Web.</span><span class="sxs-lookup"><span data-stu-id="b2635-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="b2635-108">Para obtener información sobre cómo empezar a crear una aplicación de WebView2, vaya a [Introducción](#getting-started).</span><span class="sxs-lookup"><span data-stu-id="b2635-108">For information on how to start building a WebView2 application, navigate to [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="¿Qué es la vista previa?" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="b2635-110">¿Qué es la vista previa?</span><span class="sxs-lookup"><span data-stu-id="b2635-110">What is WebView</span></span>  
:::image-end:::  

## <span data-ttu-id="b2635-111">Enfoque de aplicaciones híbridas</span><span class="sxs-lookup"><span data-stu-id="b2635-111">Hybrid application approach</span></span>  

<span data-ttu-id="b2635-112">Los programadores suelen decidir entre crear una aplicación web o una aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="b2635-112">Developers often have to decide between building a web application or a native application.</span></span>  <span data-ttu-id="b2635-113">La decisión depende del equilibrio entre el alcance y el potencial de energía.</span><span class="sxs-lookup"><span data-stu-id="b2635-113">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="b2635-114">Las aplicaciones web permiten un amplio alcance.</span><span class="sxs-lookup"><span data-stu-id="b2635-114">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="b2635-115">Como desarrollador web, puede volver a usar la mayoría, si no todo el código, en todas las plataformas.</span><span class="sxs-lookup"><span data-stu-id="b2635-115">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="b2635-116">Las aplicaciones nativas, sin embargo, usan las capacidades de toda la plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="b2635-116">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="b2635-118">Web Native</span><span class="sxs-lookup"><span data-stu-id="b2635-118">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="b2635-119">Las aplicaciones híbridas permiten a los desarrolladores disfrutar de lo mejor de ambos mundos.</span><span class="sxs-lookup"><span data-stu-id="b2635-119">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="b2635-120">Los programadores de aplicaciones híbridas se benefician de la Ubiquity y fortaleza de la plataforma web, así como de la potencia y capacidades completas de la plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="b2635-120">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="b2635-121">Beneficios de WebView2</span><span class="sxs-lookup"><span data-stu-id="b2635-121">WebView2 benefits</span></span>  

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Motivos de la vista en vista previa" lightbox="./media/WebView2/webviewreasons.png":::
   <span data-ttu-id="b2635-123">Motivos de la vista en vista previa</span><span class="sxs-lookup"><span data-stu-id="b2635-123">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="b2635-124">Ecosistema web \ & Aptitudes</span><span class="sxs-lookup"><span data-stu-id="b2635-124">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="b2635-125">Use toda la plataforma web, bibliotecas, herramientas y talento que existen en el ecosistema Web.</span><span class="sxs-lookup"><span data-stu-id="b2635-125">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="b2635-126">Innovación rápida</span><span class="sxs-lookup"><span data-stu-id="b2635-126">Rapid innovation</span></span>**  
      <span data-ttu-id="b2635-127">El desarrollo web permite una implementación e iteración más rápidas.</span><span class="sxs-lookup"><span data-stu-id="b2635-127">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="b2635-128">Compatibilidad con Windows 7, 8, 10</span><span class="sxs-lookup"><span data-stu-id="b2635-128">Windows 7, 8, 10 support</span></span>**  
      <span data-ttu-id="b2635-129">Compatibilidad con una experiencia de usuario coherente en Windows 7, 8 y 10.</span><span class="sxs-lookup"><span data-stu-id="b2635-129">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="b2635-130">Capacidades nativas</span><span class="sxs-lookup"><span data-stu-id="b2635-130">Native capabilities</span></span>**  
      <span data-ttu-id="b2635-131">Acceder al conjunto completo de API nativas.</span><span class="sxs-lookup"><span data-stu-id="b2635-131">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="b2635-132">Uso compartido de código</span><span class="sxs-lookup"><span data-stu-id="b2635-132">Code-sharing</span></span>**  
      <span data-ttu-id="b2635-133">Agregar código web a su código base permite un aumento de la reutilización en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="b2635-133">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="b2635-134">Soporte técnico de Microsoft</span><span class="sxs-lookup"><span data-stu-id="b2635-134">Microsoft support</span></span>**  
      <span data-ttu-id="b2635-135">Microsoft proporciona soporte técnico y agrega nuevas solicitudes de características cuando WebView2 se publica como GA.</span><span class="sxs-lookup"><span data-stu-id="b2635-135">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="b2635-136">Distribución de hoja perenne</span><span class="sxs-lookup"><span data-stu-id="b2635-136">Evergreen distribution</span></span>**  
      <span data-ttu-id="b2635-137">Use una versión actualizada de cromo con actualizaciones de plataforma y revisiones de seguridad regulares.</span><span class="sxs-lookup"><span data-stu-id="b2635-137">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="b2635-138">**Fijo** \ (próximamente \)</span><span class="sxs-lookup"><span data-stu-id="b2635-138">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="b2635-139">Elija empaquetar los bits de cromo en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2635-139">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="b2635-140">Adopción incremental</span><span class="sxs-lookup"><span data-stu-id="b2635-140">Incremental adoption</span></span>**  
      <span data-ttu-id="b2635-141">Agregue componentes Web por partes a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2635-141">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="b2635-142">Introducción</span><span class="sxs-lookup"><span data-stu-id="b2635-142">Getting started</span></span>  

<span data-ttu-id="b2635-143">Para compilar y probar la aplicación con el control WebView2, debe tener instalado tanto [Microsoft Edge (cromo)][MicrosoftedgeinsiderDownload] como el [SDK de WebView2][NugetPackagesMicrosoftWebWebView2] .</span><span class="sxs-lookup"><span data-stu-id="b2635-143">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="b2635-144">Seleccione una de las siguientes opciones para comenzar.</span><span class="sxs-lookup"><span data-stu-id="b2635-144">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="b2635-145">Introducción a Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="b2635-145">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="b2635-146">Introducción a WPF</span><span class="sxs-lookup"><span data-stu-id="b2635-146">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="b2635-147">Introducción a WinForms</span><span class="sxs-lookup"><span data-stu-id="b2635-147">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="b2635-148">Introducción a WinUI3</span><span class="sxs-lookup"><span data-stu-id="b2635-148">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="b2635-149">El repositorio de [muestras de WebView2][GithubMicrosoftedgeWebview2samples] contiene ejemplos que muestran todas las características del SDK de WebView2 y los patrones de uso de API.</span><span class="sxs-lookup"><span data-stu-id="b2635-149">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="b2635-150">A medida que se agregan más características al SDK de WebView2, se actualizarán las aplicaciones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b2635-150">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>  

## <span data-ttu-id="b2635-151">Plataformas compatibles</span><span class="sxs-lookup"><span data-stu-id="b2635-151">Supported platforms</span></span>  

<span data-ttu-id="b2635-152">Una disponibilidad general \ (GA \) o versión preliminar está disponible en los siguientes entornos de programación.</span><span class="sxs-lookup"><span data-stu-id="b2635-152">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="b2635-153">C/C++ \ (GA \) Win32</span><span class="sxs-lookup"><span data-stu-id="b2635-153">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="b2635-154">.NET Framework 4.6.2 o versiones posteriores \ (versión preliminar \)</span><span class="sxs-lookup"><span data-stu-id="b2635-154">.NET Framework 4.6.2 or later \(Preview\)</span></span>  
*   <span data-ttu-id="b2635-155">.NET Core 3,0 o posterior \ (versión preliminar \)</span><span class="sxs-lookup"><span data-stu-id="b2635-155">.NET Core 3.0 or later \(Preview\)</span></span>  
*   <span data-ttu-id="b2635-156">[WinUI 3,0][UwpToolkitsWinui3] \ (versión preliminar \)</span><span class="sxs-lookup"><span data-stu-id="b2635-156">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  

<span data-ttu-id="b2635-157">Puede ejecutar aplicaciones de WebView2 en las siguientes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="b2635-157">You are able to run WebView2 applications on the following versions of Windows.</span></span>  

*   <span data-ttu-id="b2635-158">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b2635-158">Windows 10</span></span>  
*   <span data-ttu-id="b2635-159">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b2635-159">Windows 8.1</span></span>  
*   <span data-ttu-id="b2635-160">Windows 7 \ \* \ \*</span><span class="sxs-lookup"><span data-stu-id="b2635-160">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="b2635-161">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="b2635-161">Windows Server 2019</span></span>  
*   <span data-ttu-id="b2635-162">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b2635-162">Windows Server 2016</span></span>  
*   <span data-ttu-id="b2635-163">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b2635-163">Windows Server 2012</span></span>  
*   <span data-ttu-id="b2635-164">Windows Server2012R2</span><span class="sxs-lookup"><span data-stu-id="b2635-164">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="b2635-165">Windows Server 2008 R2 \ \* \ \*</span><span class="sxs-lookup"><span data-stu-id="b2635-165">Windows Server 2008 R2 \*\*</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b2635-166">\ \* \ \* WebView2 soporte técnico para Windows 7 y Windows Server 2008 R2 tiene el mismo ciclo de soporte que Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b2635-166">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="b2635-167">Para obtener más información, vaya a [sistemas operativos compatibles con Microsoft Edge][DeployedgeMicrosoftEdgeSupportedOS].</span><span class="sxs-lookup"><span data-stu-id="b2635-167">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <span data-ttu-id="b2635-168">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="b2635-168">Next steps</span></span>  

<span data-ttu-id="b2635-169">Para obtener más información sobre cómo crear e implementar aplicaciones de WebView2, consulte la documentación conceptual y las guías de procedimientos.</span><span class="sxs-lookup"><span data-stu-id="b2635-169">For more information on how to build and deploy WebView2 applications, review the conceptual documentation and how-to guides.</span></span>  

#### <span data-ttu-id="b2635-170">Conceptos</span><span class="sxs-lookup"><span data-stu-id="b2635-170">Concepts</span></span>  

*   [<span data-ttu-id="b2635-171">Comprender las versiones de SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="b2635-171">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]
*   [<span data-ttu-id="b2635-172">Distribución de aplicaciones con WebView2</span><span class="sxs-lookup"><span data-stu-id="b2635-172">Distribution of applications using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="b2635-173">Procedimientos recomendados para desarrollar aplicaciones de WebView2 seguras</span><span class="sxs-lookup"><span data-stu-id="b2635-173">Best practices for developing secure WebView2 applications</span></span>][Webview2ConceptsSecurity]
*   [<span data-ttu-id="b2635-174">Carpeta administrar datos de usuario en aplicaciones de WebView2</span><span class="sxs-lookup"><span data-stu-id="b2635-174">Manage User Data Folder in WebView2 Applications</span></span>][Webview2ConceptsUserdatafolder]
 
#### <span data-ttu-id="b2635-175">Guías de How-To</span><span class="sxs-lookup"><span data-stu-id="b2635-175">How-To guides</span></span>  

*   [<span data-ttu-id="b2635-176">Cómo depurar con WebView2</span><span class="sxs-lookup"><span data-stu-id="b2635-176">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="b2635-177">Automatizar y probar WebView2 con el controlador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b2635-177">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <span data-ttu-id="b2635-178">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b2635-178">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Procedimientos recomendados para desarrollar aplicaciones de WebView2 seguras | Microsoft docs"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Administración de la carpeta datos de usuario | Microsoft docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprender las versiones de SDK de WebView2 | Microsoft docs"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Introducción a WebView2 | Microsoft docs"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Introducción a WebView2 en las aplicaciones de Windows Forms (versión preliminar) | Microsoft docs"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Introducción a WebView2 en WinUI3 (vista previa) | Microsoft docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Introducción a WebView2 en WPF (vista previa) | Microsoft docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Cómo depurar con WebView2 | Microsoft docs"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatizar y probar WebView2 con el controlador Microsoft Edge | Microsoft docs"  
[Webview2Releasenotes]: ./releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Biblioteca de interfaces de usuario de Windows 3 Preview 2 (2020 de julio) | Microsoft docs"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Sistemas operativos compatibles con Microsoft Edge | Microsoft docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Insider de Microsoft Edge"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | Galería de NuGet"  

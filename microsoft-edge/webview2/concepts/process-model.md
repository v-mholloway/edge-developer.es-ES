---
description: Modelo de proceso
title: Proceso de | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, controlador de explorador, edge html
ms.openlocfilehash: 95d0c53219114c47a781317ab4b2ee2028fc586f
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535618"
---
# <a name="process-model"></a><span data-ttu-id="932a3-104">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="932a3-104">Process model</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="932a3-105">Plataformas compatibles:</span><span class="sxs-lookup"><span data-stu-id="932a3-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="932a3-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="932a3-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="932a3-107">WebView2 usa el mismo modelo de proceso que el explorador de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="932a3-107">WebView2 uses the same process model as the Microsoft Edge browser.</span></span>  <span data-ttu-id="932a3-108">Para obtener más información sobre el modelo de proceso del explorador, vaya a [Arquitectura del explorador: vea][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]el explorador web moderno.</span><span class="sxs-lookup"><span data-stu-id="932a3-108">For more information about the browser process model, navigate to [Browser Architecture - Inside look at modern web browser][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span></span>  

<span data-ttu-id="932a3-109">Un proceso de explorador está asociado con los procesos del representador y otros procesos de utilidad, como se describe en ese artículo.</span><span class="sxs-lookup"><span data-stu-id="932a3-109">One browser process is associated with the renderer processes and other utility processes as described in that article.</span></span>  <span data-ttu-id="932a3-110">Además, si se especifica WebView2, los procesos de solicitud de aplicaciones host usan WebView2.</span><span class="sxs-lookup"><span data-stu-id="932a3-110">Additionally, if WebView2 is specified, the host app requesting processes use WebView2.</span></span>  

:::image type="complex" source="../media/process-model-1.png" alt-text="Proceso 1" lightbox="../media/process-model-1.png":::
   <span data-ttu-id="932a3-112">Proceso 1</span><span class="sxs-lookup"><span data-stu-id="932a3-112">Process 1</span></span>  
:::image-end:::    

<span data-ttu-id="932a3-113">Un proceso de explorador está asociado a una sola carpeta de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="932a3-113">A browser process is associated with only one user data folder.</span></span>  <span data-ttu-id="932a3-114">Un proceso de solicitud puede especificar más de una carpeta de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="932a3-114">A request process may specify more than one user data folder.</span></span>  <span data-ttu-id="932a3-115">Un proceso de solicitud que especifica más de una carpeta de datos de usuario está asociado con el mismo número de procesos de explorador.</span><span class="sxs-lookup"><span data-stu-id="932a3-115">A request process that specifies more than one user data folder is associated with the same number of browser processes.</span></span>  
<span data-ttu-id="932a3-116">Por ejemplo, un proceso de solicitud que solicita acceso a dos carpetas de datos de usuario usa dos procesos de explorador.</span><span class="sxs-lookup"><span data-stu-id="932a3-116">For example, a request process that requests access to two user data folders uses two browser processes.</span></span>  

:::image type="complex" source="../media/process-model-2.png" alt-text="Proceso 2" lightbox="../media/process-model-2.png":::
   <span data-ttu-id="932a3-118">Proceso 2</span><span class="sxs-lookup"><span data-stu-id="932a3-118">Process 2</span></span>  
:::image-end:::    

<span data-ttu-id="932a3-119">Un proceso de explorador está asociado a varios procesos de representador.</span><span class="sxs-lookup"><span data-stu-id="932a3-119">A browser process is associated with several renderer processes.</span></span>  <span data-ttu-id="932a3-120">Una instancia de WebView 2 crea un proceso de explorador para los marcos de servicio.</span><span class="sxs-lookup"><span data-stu-id="932a3-120">A WebView 2 instance creates a browser process to service frames.</span></span>  <span data-ttu-id="932a3-121">Un proceso de explorador puede estar asociado a varios fotogramas.</span><span class="sxs-lookup"><span data-stu-id="932a3-121">A browser process may be associated with multiple frames.</span></span>  <span data-ttu-id="932a3-122">Un proceso de explorador puede asociarse con diferentes instancias de WebView2.</span><span class="sxs-lookup"><span data-stu-id="932a3-122">A browser process may be associated with different instances of WebView2.</span></span>  <span data-ttu-id="932a3-123">El número de procesos de representación varía en función de las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="932a3-123">The number of render processes varies based on the following conditions.</span></span>  

*   <span data-ttu-id="932a3-124">Uso de la característica de aislamiento del sitio web en el explorador.</span><span class="sxs-lookup"><span data-stu-id="932a3-124">Use of the website isolation feature in your browser.</span></span>  
*   <span data-ttu-id="932a3-125">Número de orígenes desconectados distintos representados en instancias asociadas de WebView2.</span><span class="sxs-lookup"><span data-stu-id="932a3-125">The number of distinct disconnected origins rendered in associated instances of WebView2.</span></span>  
    
<span data-ttu-id="932a3-126">La característica del explorador de aislamiento del sitio web se describe en el contenido anterior.</span><span class="sxs-lookup"><span data-stu-id="932a3-126">The website isolation browser feature is described in the previous content.</span></span> 
<!--todo:  which previous content?  -->  

<span data-ttu-id="932a3-127">Representa `CoreWebView2Environment` una carpeta de datos de usuario y un proceso de explorador.</span><span class="sxs-lookup"><span data-stu-id="932a3-127">The `CoreWebView2Environment` represents a user data folder and browser process.</span></span>  <span data-ttu-id="932a3-128">El no corresponde directamente a ningún conjunto de procesos, ya que un WebView2 usa varios procesos de representador según el aislamiento del sitio web como se describió `CoreWebView2` anteriormente.</span><span class="sxs-lookup"><span data-stu-id="932a3-128">The `CoreWebView2` does not directly correspond to any one set of processes since various renderer processes are used by a WebView2 depending on website isolation as previously described.</span></span>  

<span data-ttu-id="932a3-129">Para reaccionar ante bloqueos y bloqueos en los procesos del explorador y del representador, use el `ProcessFailed` evento `CoreWebView2` de .</span><span class="sxs-lookup"><span data-stu-id="932a3-129">To react to crashes and hangs in the browser and renderer processes, use the `ProcessFailed` event of `CoreWebView2`.</span></span>  

<span data-ttu-id="932a3-130">Para cerrar de forma segura los procesos asociados de explorador y representador, use el `Close` método `CoreWebView2Controller` de .</span><span class="sxs-lookup"><span data-stu-id="932a3-130">To safely shut down associated browser and renderer processes, use the `Close` method of `CoreWebView2Controller`.</span></span>  

<span data-ttu-id="932a3-131">Para abrir la ventana Administrador de tareas del explorador desde la **ventana DevTools** de una instancia WebView2, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="932a3-131">To open the Browser Task Manager window from the **DevTools** window of a WebView2 instance, complete on of the following actions.</span></span>  

*   <span data-ttu-id="932a3-132">Seleccione `Shift` + `Escape` .</span><span class="sxs-lookup"><span data-stu-id="932a3-132">Select `Shift`+`Escape`.</span></span>  
*   <span data-ttu-id="932a3-133">Mantenga el mouse en la barra de título de la ventana DevTools, abra el menú contextual \(haga clic con el botón secundario\) y elija `Browser task manager` .</span><span class="sxs-lookup"><span data-stu-id="932a3-133">Hover on the DevTools window title bar, open the contextual menu \(right-click\), and choose `Browser task manager`.</span></span>  
    
<span data-ttu-id="932a3-134">Se muestran todos los procesos asociados con el proceso de explorador de webView2, incluidos los propósitos asociados.</span><span class="sxs-lookup"><span data-stu-id="932a3-134">All processes associated with the browser process of your WebView2 are displayed including associated purposes.</span></span>  

## <a name="see-also"></a><span data-ttu-id="932a3-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="932a3-135">See also</span></span>  

*   <span data-ttu-id="932a3-136">Para empezar a usar WebView2, vaya a Guías de introducción a [WebView2.][Webview2IndexGetStarted]</span><span class="sxs-lookup"><span data-stu-id="932a3-136">To Get Started using WebView2, navigate to [WebView2 Get Started Guides][Webview2IndexGetStarted] guides.</span></span>  
*   <span data-ttu-id="932a3-137">Para obtener un ejemplo completo de las capacidades de WebView2, vaya al repositorio [WebView2Samples][GithubMicrosoftedgeWebview2samples] en GitHub.</span><span class="sxs-lookup"><span data-stu-id="932a3-137">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="932a3-138">Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="932a3-138">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="932a3-139">Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="932a3-139">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="932a3-140">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="932a3-140">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Introducción a Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Clase WebView2 | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Arquitectura del explorador: aspecto interno del explorador web moderno (parte 1)"  

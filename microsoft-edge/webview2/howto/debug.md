---
description: Más información sobre cómo depurar controles WebView2.
title: Introducción a la depuración de aplicaciones de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/13/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: dcdeeadc2c25bcf50834176706b8d181f06f994a
ms.sourcegitcommit: 6c7ededf8677fd7add5e4060e92f9ec4cfdb6952
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2020
ms.locfileid: "10927933"
---
# <span data-ttu-id="00237-104">Introducción a la depuración de aplicaciones de WebView2</span><span class="sxs-lookup"><span data-stu-id="00237-104">Get started debugging WebView2 applications</span></span>  

<span data-ttu-id="00237-105">El objetivo del control Microsoft Edge WebView2 es combinar lo mejor de las características y herramientas de desarrollo de aplicaciones nativas y Web.</span><span class="sxs-lookup"><span data-stu-id="00237-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native application development features and tools.</span></span>  <span data-ttu-id="00237-106">Al desarrollar su aplicación de WebView2, debe depurar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00237-106">When you develop your WebView2 application, you should debug your application.</span></span>  <span data-ttu-id="00237-107">En este artículo se describen las distintas herramientas que se usan para depurar el código web y nativo de la aplicación WebView2.</span><span class="sxs-lookup"><span data-stu-id="00237-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 application.</span></span>  

## [<span data-ttu-id="00237-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="00237-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="00237-109">Use [las herramientas de desarrollador de Microsoft Edge (cromo)][DevtoolsGuideChromiumMain] para depurar contenido web que se muestra en controles WebView2, de la misma manera que puede depurar para otra página web que se muestra en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="00237-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="00237-110">Para abrir la DevTools, establezca el foco en el control WebView y, a continuación, use una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="00237-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="00237-111">Seleccione `F12` .</span><span class="sxs-lookup"><span data-stu-id="00237-111">Select `F12`.</span></span>  
*   <span data-ttu-id="00237-112">Seleccione `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="00237-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="00237-113">Abra el menú contextual \ (haga clic con el botón derecho \) y elija `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="00237-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  

<span data-ttu-id="00237-114">Para obtener más información, consulte [información general de DevTools][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="00237-114">For more information, see [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="Depuración DevTools" lightbox="./media/f12.png":::
   <span data-ttu-id="00237-116">Depuración DevTools</span><span class="sxs-lookup"><span data-stu-id="00237-116">DevTools debugging</span></span>  
:::image-end:::  

## [<span data-ttu-id="00237-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="00237-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="00237-118">Visual Studio proporciona varias herramientas de depuración para el código nativo y Web en aplicaciones de WebView2.</span><span class="sxs-lookup"><span data-stu-id="00237-118">Visual Studio provides various debugging tools for web and native code in WebView2 applications.</span></span>  <span data-ttu-id="00237-119">En la sección de Visual Studio, el foco principalmente es la depuración de controles de WebView, pero los otros métodos de depuración en Visual Studio están disponibles de la forma habitual.</span><span class="sxs-lookup"><span data-stu-id="00237-119">In the Visual Studio section, the primarily focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="00237-120">Use el siguiente proceso para depurar código nativo y web solo en aplicaciones Win32 o complementos de Office.</span><span class="sxs-lookup"><span data-stu-id="00237-120">Use the following process to debug web and native code in Win32 applications or Office add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="00237-121">Cuando depure la aplicación en Visual Studio con el depurador nativo adjunto, seleccionar `F12` puede desencadenar el depurador nativo en lugar de las herramientas de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="00237-121">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="00237-122">Seleccione `Ctrl` + `Shift` + `I` o use el menú contextual \ (haga clic con el botón derecho \) para evitar la situación.</span><span class="sxs-lookup"><span data-stu-id="00237-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="00237-123">Antes de empezar, asegúrese de que se cumplan los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="00237-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="00237-124">Para depurar scripts, la aplicación debe iniciarse desde Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="00237-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="00237-125">No puede adjuntar un depurador a un proceso de WebView2 en ejecución.</span><span class="sxs-lookup"><span data-stu-id="00237-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="00237-126">Instale Visual Studio 2019 versión 16,4 Preview 2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="00237-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  

<span data-ttu-id="00237-127">Instale y configure las herramientas de depurador de scripts en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="00237-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="00237-128">Complete las acciones siguientes para instalar el componente de **diagnóstico de JavaScript** en el **desarrollo de escritorio con C++**.</span><span class="sxs-lookup"><span data-stu-id="00237-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  

    1. <span data-ttu-id="00237-129">En la barra del explorador de Windows, escriba `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="00237-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1. <span data-ttu-id="00237-130">Elija **instalador de Visual Studio** para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="00237-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1. <span data-ttu-id="00237-131">En el instalador de Visual Studio, en la versión instalada, haga clic en el botón **más** y, a continuación, elija **modificar**.</span><span class="sxs-lookup"><span data-stu-id="00237-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1. <span data-ttu-id="00237-132">En Visual Studio, en **cargas de trabajo**, elija la opción **desarrollo de escritorio en C++** .</span><span class="sxs-lookup"><span data-stu-id="00237-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Pantalla modificando cargas de trabajo de Visual Studio" lightbox="./media/workloads.png":::
            <span data-ttu-id="00237-134">Pantalla modificando cargas de trabajo de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="00237-134">Visual Studio Modifying Workloads Screen</span></span> :::image-end:::  
        
    1.  <span data-ttu-id="00237-135">Elija **componentes individuales**.</span><span class="sxs-lookup"><span data-stu-id="00237-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="00237-136">En el cuadro de búsqueda, escriba `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="00237-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="00237-137">Elija la configuración de **diagnóstico de JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="00237-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="00237-138">Elija **modificar**.</span><span class="sxs-lookup"><span data-stu-id="00237-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Ficha modificar componentes individuales de Visual Studio" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="00237-140">Ficha modificar componentes individuales de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="00237-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="00237-141">Habilite la depuración de scripts para aplicaciones de WebView2.</span><span class="sxs-lookup"><span data-stu-id="00237-141">Enable script debugging for WebView2 applications.</span></span>  
    1.  <span data-ttu-id="00237-142">En el proyecto WebView2, abra el menú contextual \ (haga clic con el botón derecho \) y elija **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="00237-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="00237-143">En las **propiedades de configuración**, elija **depuración**.</span><span class="sxs-lookup"><span data-stu-id="00237-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="00237-144">En el **tipo de depuración**, elija **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="00237-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Propiedad de configuración de depuración de Visual Studio" lightbox="./media/enbjs.png":::
           <span data-ttu-id="00237-146">Propiedad de configuración de **depuración** de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="00237-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="00237-147">Complete las acciones siguientes para depurar su aplicación de WebView2.</span><span class="sxs-lookup"><span data-stu-id="00237-147">Complete the following actions to debug your WebView2 application.</span></span>  

1.  <span data-ttu-id="00237-148">Para establecer un punto de interrupción en el código fuente, coloque el puntero a la izquierda del número de línea y elija establecer un punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="00237-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="00237-149">El adaptador de depuración JS/TS no realiza asignaciones de ruta de origen.</span><span class="sxs-lookup"><span data-stu-id="00237-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="00237-150">Debe abrir exactamente la misma ruta asociada con su WebView2.</span><span class="sxs-lookup"><span data-stu-id="00237-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Agregar punto de interrupción en Visual Studio" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="00237-152">Agregar punto de interrupción en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="00237-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="00237-153">Para ejecutar el depurador, elija el tamaño de bit de la plataforma y, a continuación, elija el botón verde reproducir junto al **depurador local de Windows**.</span><span class="sxs-lookup"><span data-stu-id="00237-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="00237-154">La aplicación se ejecuta y el depurador se conecta al primer proceso WebView2 que se crea.</span><span class="sxs-lookup"><span data-stu-id="00237-154">The application runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Depurador local de Windows de Visual Studio" lightbox="./media/run.png"::: 
       <span data-ttu-id="00237-156">**Depurador local de Windows** de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="00237-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="00237-157">En la **consola de depuración**, busque la salida del depurador.</span><span class="sxs-lookup"><span data-stu-id="00237-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Consola de depuración de Visual Studio" lightbox="./media/console.png"::: 
       <span data-ttu-id="00237-159">Consola de **depuración** de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="00237-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
* * *  

## <span data-ttu-id="00237-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="00237-160">See also</span></span>  

*   <span data-ttu-id="00237-161">Para comenzar a usar WebView2, consulte [WebView2 guías de introducción][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="00237-161">To get started using WebView2, see [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="00237-162">Para obtener un ejemplo completo de las capacidades de WebView2, consulta el repositorio de [WebView2Samples][GithubMicrosoftedgeWebview2samples] en github.</span><span class="sxs-lookup"><span data-stu-id="00237-162">For a comprehensive example of WebView2 capabilities, see the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="00237-163">Para obtener información más detallada sobre las API de WebView2, consulta referencia de la [API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="00237-163">For more detailed information about WebView2 APIs, see [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="00237-164">Para obtener más información sobre WebView2, consulte [recursos WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="00237-164">For more information about WebView2, see [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="00237-165">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="00237-165">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

[Webview2ReferenceDotnet09515MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-515/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions clase | Microsoft docs"  
[Webview2ReferenceWin3209538Webview2IdlParameters]: ../reference/win32/0-9-538/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-Globals | Microsoft docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Referencia de la API de Microsoft Edge WebView2 | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "¿Qué novedades hay? -Depurador de JavaScript para Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicaciones de WebView de Microsoft Edge (cromo): depurador de código de Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  

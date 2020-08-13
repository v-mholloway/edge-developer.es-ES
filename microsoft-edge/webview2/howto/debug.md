---
description: Más información sobre cómo depurar controles WebView2.
title: Depurar WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 6b2cc65e5cb368c29efec2eb3638f0c1772000d9
ms.sourcegitcommit: 4bc904c5d54347185f275bd76441975be471c320
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/12/2020
ms.locfileid: "10926480"
---
# <span data-ttu-id="1b6ed-104">Cómo depurar con WebView2</span><span class="sxs-lookup"><span data-stu-id="1b6ed-104">How to Debug with WebView2</span></span>  

<span data-ttu-id="1b6ed-105">El objetivo del control Microsoft Edge WebView2 es combinar lo mejor de las características de desarrollo de aplicaciones nativas y Web y las herramientas de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="1b6ed-106">En la siguiente página se describen las distintas herramientas que se deben usar al desarrollar con controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-106">The following page outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="1b6ed-107">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1b6ed-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="1b6ed-108">Use [las herramientas de desarrollador de Microsoft Edge (cromo)][DevtoolsGuideChromiumMain] para depurar contenido web que se muestra en los controles de WebView2, de la misma manera que usa Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-108">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you use Microsoft Edge.</span></span>  <span data-ttu-id="1b6ed-109">Para abrir la DevTools, establezca el foco en la ventana WebView y, a continuación, use cualquiera de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-109">To open the DevTools, set focus on the WebView window and then use any of the following actions.</span></span>  
*   <span data-ttu-id="1b6ed-110">Seleccione `F12` .</span><span class="sxs-lookup"><span data-stu-id="1b6ed-110">Select `F12`.</span></span>  
*   <span data-ttu-id="1b6ed-111">Seleccione `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="1b6ed-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="1b6ed-112">Abra el menú contextual \ (haga clic con el botón derecho \) > seleccione `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="1b6ed-112">Open the context menu \(right-click\) > select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   <span data-ttu-id="1b6ed-114">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1b6ed-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="1b6ed-115">Cuando depure la aplicación en Visual Studio con el depurador nativo adjunto, presionar `F12` podría desencadenar el depurador nativo en lugar de las herramientas de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-115">When you debug your application in Visual Studio with the native debugger attached, pressing `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="1b6ed-116">Presione `Ctrl` + `Shift` + `I` o use el menú contextual \ (haga clic con el botón derecho \) para evitar la situación.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-116">Press `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

> [!NOTE]
> <span data-ttu-id="1b6ed-117">Puede usar el `--auto-open-devtools-for-tabs` argumento de la línea de comandos para abrir una nueva ventana de DevTools al crear por primera vez una vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-117">You may use the `--auto-open-devtools-for-tabs` command-line argument to open a new DevTools window when you first create a WebView.</span></span>  <!--See `CreateCoreWebView2Controller` documentation for how to provide additional command-line arguments to the browser process.  See `LoaderOverride` registry key to examine different builds of WebView2 without modifying your application in the `CreateCoreWebView2Controller` documentation.  -->  

## <span data-ttu-id="1b6ed-118">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1b6ed-118">Visual Studio</span></span>  

<span data-ttu-id="1b6ed-119">Use el depurador de scripts en Visual Studio 2019 versión 16,4 Preview 2 o una versión posterior para depurar el script en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-119">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  <span data-ttu-id="1b6ed-120">Compruebe que el componente **diagnóstico de JavaScript** en **desarrollo de escritorio con** la carga de trabajo de C++ está instalado.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-120">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Diagnósticos de JavaScript de Visual Studio":::
   <span data-ttu-id="1b6ed-122">Diagnósticos de JavaScript de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1b6ed-122">Visual Studio JavaScript diagnostics</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="1b6ed-123">Para habilitar la depuración de scripts WebView2, abra el menú contextual \ (haga clic con el botón derecho \) en el proyecto > seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-123">To enable WebView2 script debugging, open the context menu \(right-click\) on your project > select **Properties**.</span></span>  

*   <span data-ttu-id="1b6ed-124">En **propiedades de configuración**, seleccione **depuración**.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-124">On **Configuration Properties**, select **Debugging**.</span></span>  
*   <span data-ttu-id="1b6ed-125">En la propiedad **tipo de depurador** , seleccione **JavaScript (WebView2)** en la lista de opciones.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-125">On the **Debugger Type** property, select **JavaScript (WebView2)** from the list of options.</span></span> 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Depurador de JavaScript de Visual Studio":::
   <span data-ttu-id="1b6ed-127">Depurador de JavaScript de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1b6ed-127">Visual Studio JavaScript Debugger</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="1b6ed-128">Ya está todo configurado y listo para depurar.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-128">You are all set up and ready to debug.</span></span>  

<span data-ttu-id="1b6ed-129">Para depurar, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-129">To Debug, complete the following actions.</span></span>  

1.  <span data-ttu-id="1b6ed-130">Establecer puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="1b6ed-130">Set Breakpoints</span></span>  
    *   <span data-ttu-id="1b6ed-131">Abra el archivo de script y establezca el punto de interrupción en el lugar que desee.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-131">Open the script file and set the breakpoint where you want it.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="1b6ed-132">El adaptador de depuración JS/TS no realiza la asignación de ruta de origen.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-132">The JS/TS debug adapter does not do source path mapping.</span></span><span data-ttu-id="1b6ed-133">Debe abrir exactamente la misma ruta asociada con su WebView2.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-133">  You must open the exact same path associated with your WebView2.</span></span>  
        
1.  <span data-ttu-id="1b6ed-134">Ejecutar código</span><span class="sxs-lookup"><span data-stu-id="1b6ed-134">Run Code</span></span>  
    *   <span data-ttu-id="1b6ed-135">Seleccione el tipo de compilación y el entorno de tiempo de ejecución que corresponda y, a continuación, inicie el depurador local de Windows.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-135">Select your appropriate build flavor and runtime environment and then start the local windows debugger.</span></span>  
1.  <span data-ttu-id="1b6ed-136">Ver consola de depuración</span><span class="sxs-lookup"><span data-stu-id="1b6ed-136">View Debug Console</span></span>  
    *   <span data-ttu-id="1b6ed-137">La aplicación se ejecuta y el depurador se conecta después de que se crea el primer webview2.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-137">You application runs and the debugger connects after the first webview2 is created.</span></span><span data-ttu-id="1b6ed-138">Se muestra el resultado pendiente de depuración.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-138">  Any pending debug output is displayed.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="1b6ed-139">Este método de depuración está actualmente restringido a las aplicaciones Win32 y los complementos de Office.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-139">This method of debugging is currently restricted to Win32 applications and Office add-ins.</span></span>  
        
## <span data-ttu-id="1b6ed-140">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="1b6ed-140">Visual Studio Code</span></span>  

<span data-ttu-id="1b6ed-141">Puede usar código de Visual Studio para depurar scripts que se ejecutan en controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="1b6ed-141">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="1b6ed-142">Para obtener más información, consulte [aplicaciones de WebView de Microsoft Edge (cromo)][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].</span><span class="sxs-lookup"><span data-stu-id="1b6ed-142">For more information, see [Microsoft Edge (Chromium) WebView Applications][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="1b6ed-143">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1b6ed-143">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!--## Debugging  

Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`. You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView. See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process. Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.  -->  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicaciones de WebView de Microsoft Edge (cromo)-VS depurador de código para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  

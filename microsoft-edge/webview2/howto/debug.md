---
description: Más información sobre cómo depurar controles WebView2.
title: Depurar WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 232104abc360cfa660d567ffb66535213fcb3ae0
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888589"
---
# <span data-ttu-id="b4d1e-104">Cómo depurar con WebView2</span><span class="sxs-lookup"><span data-stu-id="b4d1e-104">How to Debug with WebView2</span></span>  

<span data-ttu-id="b4d1e-105">El objetivo del control Microsoft Edge WebView2 es combinar lo mejor de las características de desarrollo de aplicaciones nativas y Web y las herramientas de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="b4d1e-106">En la siguiente página se describen las distintas herramientas que se deben usar al desarrollar con controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-106">The following page outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="b4d1e-107">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b4d1e-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="b4d1e-108">Use [las herramientas de desarrollador de Microsoft Edge (cromo)][DevtoolsMain] para depurar contenido web que se muestra en controles WebView2, de la misma manera que si estuviera usando Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-108">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsMain] to debug web content displayed in WebView2 controls, in the same way that you would if you were using Microsoft Edge.</span></span>  <span data-ttu-id="b4d1e-109">Para abrir la DevTools, establezca el foco en la ventana WebView y, a continuación, use cualquiera de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-109">To open the DevTools, set focus on the WebView window and then use any of the following actions.</span></span>  

*   <span data-ttu-id="b4d1e-110">Seleccione `F12` .</span><span class="sxs-lookup"><span data-stu-id="b4d1e-110">Select `F12`.</span></span>  
*   <span data-ttu-id="b4d1e-111">Seleccione `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="b4d1e-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="b4d1e-112">Abra el menú contextual \ (haga clic con el botón derecho \) y seleccione `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="b4d1e-112">Open the context menu \(right-click\) and select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   <span data-ttu-id="b4d1e-114">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b4d1e-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!IMPORTANT]
> <span data-ttu-id="b4d1e-115">Cuando depure la aplicación en Visual Studio con el depurador nativo adjunto, seleccionar `F12` puede desencadenar el depurador nativo en lugar de las herramientas de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-115">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="b4d1e-116">Use `Ctrl` + `Shift` + `I` o use el menú contextual \ (haga clic con el botón derecho \) para evitar la situación.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-116">Use `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

## <span data-ttu-id="b4d1e-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b4d1e-117">Visual Studio</span></span>  

<span data-ttu-id="b4d1e-118">Puede usar Visual Studio para desarrollar el código de la aplicación y las secuencias de comandos de depuración al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-118">You may use Visual Studio to develop application code and debug scripts at the same time.</span></span>  

<span data-ttu-id="b4d1e-119">Ten en cuenta lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-119">Keep the following things in mind.</span></span>  

*   <span data-ttu-id="b4d1e-120">Visual Studio solo admite scripts de depuración cuando la aplicación se inicia desde Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-120">Visual Studio only supports debugging scripts when the app is launched from within Visual Studio.</span></span>  <span data-ttu-id="b4d1e-121">\ (No se admite adjuntar un proceso en ejecución para la depuración. \)</span><span class="sxs-lookup"><span data-stu-id="b4d1e-121">\(Attaching a running process for debugging is not supported.\)</span></span>  
*   <span data-ttu-id="b4d1e-122">El escenario de depuración de WebView objetivo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-122">The targeted WebView debugging scenario is not supported.</span></span>  

<span data-ttu-id="b4d1e-123">Use el depurador de scripts en Visual Studio 2019 versión 16,4 Preview 2 o una versión posterior para depurar el script en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-123">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  

<span data-ttu-id="b4d1e-124">Configurar el depurador.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-124">Set up the debugger.</span></span>  

*   <span data-ttu-id="b4d1e-125">Compruebe que el componente **diagnóstico de JavaScript** en **desarrollo de escritorio con** la carga de trabajo de C++ está instalado.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-125">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  
    
    1.  <span data-ttu-id="b4d1e-126">Vaya a la configuración de **aplicaciones & características** en Windows.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-126">Navigate to **Apps & features** settings in Windows.</span></span>  <span data-ttu-id="b4d1e-127">Búsquelo con la barra de tareas de Windows.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-127">Search for it using the Windows task bar.</span></span>  
    1.  <span data-ttu-id="b4d1e-128">Elija **modificar**.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-128">Choose **Modify**.</span></span>  
    1.  <span data-ttu-id="b4d1e-129">Compruebe que están seleccionadas las casillas de verificación **diagnósticos de JavaScript** y **desarrollo de escritorio de C++** .</span><span class="sxs-lookup"><span data-stu-id="b4d1e-129">Verify the **Javascript diagnostics** and **Desktop Development in C++** checkboxes are selected.</span></span>  
        
        :::image type="complex" source="../media/appsandfeatures.png" alt-text="Aplicaciones y características" lightbox="../media/appsandfeatures.png":::
           <span data-ttu-id="b4d1e-131">Aplicaciones y características</span><span class="sxs-lookup"><span data-stu-id="b4d1e-131">Apps & Features</span></span>  
        :::image-end:::  
        
*   <span data-ttu-id="b4d1e-132">Habilite la depuración de script WebView2.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-132">Enable WebView2 script debugging.</span></span>  
    1.  <span data-ttu-id="b4d1e-133">Mantenga el puntero sobre el proyecto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-133">Hover on your project, open the context menu \(right-click\), and select **Properties**.</span></span>  
    1.  <span data-ttu-id="b4d1e-134">En **propiedades de configuración**, seleccione **depuración**.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-134">On **Configuration Properties**, select **Debugging**.</span></span>  
    1.  <span data-ttu-id="b4d1e-135">En la propiedad **tipo de depurador** , busque en la lista de opciones y seleccione **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-135">On the **Debugger Type** property, search the the list of options, and select **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="../media/enbjs.png" alt-text="Depurador de JavaScript de Visual Studio" lightbox="../media/enbjs.png":::
           <span data-ttu-id="b4d1e-137">Depurador de JavaScript de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b4d1e-137">Visual Studio JavaScript Debugger</span></span>  
        :::image-end:::  
        
<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="b4d1e-138">Ya está todo configurado y listo para depurar.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-138">You are all set up and ready to debug.</span></span>  

<span data-ttu-id="b4d1e-139">Para depurar, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-139">To Debug, complete the following actions.</span></span>  

1.  <span data-ttu-id="b4d1e-140">Establecer puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="b4d1e-140">Set Breakpoints</span></span>  
    *   <span data-ttu-id="b4d1e-141">Abra el archivo de script y establezca el punto de interrupción en el lugar que desee.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-141">Open the script file and set the breakpoint where you want it.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="b4d1e-142">El adaptador de depuración JS/TS no realiza la asignación de ruta de origen.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-142">The JS/TS debug adapter does not do source path mapping.</span></span><span data-ttu-id="b4d1e-143">Debe abrir exactamente la misma ruta asociada con su WebView2.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-143">  You must open the exact same path associated with your WebView2.</span></span>  
        
1.  <span data-ttu-id="b4d1e-144">Ejecutar código</span><span class="sxs-lookup"><span data-stu-id="b4d1e-144">Run Code</span></span>  
    *   <span data-ttu-id="b4d1e-145">Seleccione el tipo de compilación y el entorno de tiempo de ejecución que corresponda y, a continuación, inicie el depurador local de Windows.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-145">Select your appropriate build flavor and runtime environment and then start the local windows debugger.</span></span>  
1.  <span data-ttu-id="b4d1e-146">Ver consola de depuración</span><span class="sxs-lookup"><span data-stu-id="b4d1e-146">View Debug Console</span></span>  
    *   <span data-ttu-id="b4d1e-147">La aplicación se ejecuta y el depurador se conecta después de que se crea el primer webview2.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-147">You application runs and the debugger connects after the first webview2 is created.</span></span><span data-ttu-id="b4d1e-148">Se muestra el resultado pendiente de depuración.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-148">  Any pending debug output is displayed.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="b4d1e-149">Este método de depuración está actualmente restringido a las aplicaciones Win32 y los complementos de Office.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-149">This method of debugging is currently restricted to Win32 applications and Office add-ins.</span></span>  
        
## <span data-ttu-id="b4d1e-150">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b4d1e-150">Visual Studio Code</span></span>  

<span data-ttu-id="b4d1e-151">Puede usar código de Visual Studio para depurar scripts que se ejecutan en controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-151">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="b4d1e-152">Para obtener más información, consulte [aplicaciones de WebView de Microsoft Edge (cromo)][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].</span><span class="sxs-lookup"><span data-stu-id="b4d1e-152">For more information, see [Microsoft Edge (Chromium) WebView Applications][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="b4d1e-153">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b4d1e-153">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="b4d1e-154">Ayuda a crear una experiencia WebView2 más rica compartiendo tus comentarios.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-154">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="b4d1e-155">Visita el [repositorio de comentarios][GithubMicrosoftedgeWebviewfeedback] para enviar solicitudes de características o informes de errores.</span><span class="sxs-lookup"><span data-stu-id="b4d1e-155">Visit the [feedback repo][GithubMicrosoftedgeWebviewfeedback] to submit feature requests or bug reports.</span></span>  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicaciones de WebView de Microsoft Edge (cromo)-VS depurador de código para Microsoft Edge | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

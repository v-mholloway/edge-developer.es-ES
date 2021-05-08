---
description: Obtenga información sobre cómo depurar controles WebView2.
title: Introducción a la depuración de aplicaciones webView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral
ms.openlocfilehash: f895634d5e005bb07579d9a5f41c6a988cd78a33
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536752"
---
# <a name="get-started-debugging-webview2-apps"></a><span data-ttu-id="b94a4-104">Introducción a la depuración de aplicaciones webView2</span><span class="sxs-lookup"><span data-stu-id="b94a4-104">Get started debugging WebView2 apps</span></span>  

<span data-ttu-id="b94a4-105">El objetivo del control Microsoft Edge WebView2 es combinar lo mejor de las características y herramientas de desarrollo de aplicaciones nativas y web.</span><span class="sxs-lookup"><span data-stu-id="b94a4-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native app development features and tools.</span></span>  <span data-ttu-id="b94a4-106">Al desarrollar la aplicación WebView2, debes depurar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b94a4-106">When you develop your WebView2 app, you should debug your app.</span></span>  <span data-ttu-id="b94a4-107">En este artículo se describen las distintas herramientas que se deben usar para depurar el código web y nativo de la aplicación WebView2.</span><span class="sxs-lookup"><span data-stu-id="b94a4-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 app.</span></span>  

## [<a name="microsoft-edge-devtools"></a><span data-ttu-id="b94a4-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b94a4-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="b94a4-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] para depurar el contenido web que se muestra en los controles WebView2, del mismo modo que puede depurar para otra página web mostrada en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b94a4-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="b94a4-110">Para abrir DevTools, establezca el foco en el control WebView y, a continuación, use una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="b94a4-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="b94a4-111">Seleccione `F12` .</span><span class="sxs-lookup"><span data-stu-id="b94a4-111">Select `F12`.</span></span>  
*   <span data-ttu-id="b94a4-112">Seleccione `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="b94a4-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="b94a4-113">Abra el menú contextual \(hacer clic con el botón secundario\) y elija `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="b94a4-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  
    
<span data-ttu-id="b94a4-114">Para obtener más información, vaya [a DevTools overview][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="b94a4-114">For more information, navigate to [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="Depuración de DevTools" lightbox="./media/f12.png":::
   <span data-ttu-id="b94a4-116">Depuración de DevTools</span><span class="sxs-lookup"><span data-stu-id="b94a4-116">DevTools debugging</span></span>  
:::image-end:::  

## [<a name="visual-studio"></a><span data-ttu-id="b94a4-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b94a4-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="b94a4-118">Visual Studio proporciona varias herramientas de depuración para código web y nativo en aplicaciones webView2.</span><span class="sxs-lookup"><span data-stu-id="b94a4-118">Visual Studio provides various debugging tools for web and native code in WebView2 apps.</span></span>  <span data-ttu-id="b94a4-119">En la Visual Studio, el foco principal es la depuración de controles WebView, pero los demás métodos de depuración de Visual Studio están disponibles como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="b94a4-119">In the Visual Studio section, the primary focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="b94a4-120">Use el siguiente proceso para depurar código web y nativo en aplicaciones de Win32 o solo Office complementos.</span><span class="sxs-lookup"><span data-stu-id="b94a4-120">Use the following process to debug web and native code in Win32 apps or Office Add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b94a4-121">Al depurar la aplicación en Visual Studio con el depurador nativo adjunto, la selección puede desencadenar el depurador nativo `F12` en lugar de Herramientas de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="b94a4-121">When you debug your app in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="b94a4-122">Seleccione `Ctrl` + `Shift` + `I` o use el menú contextual \(hacer clic con el botón secundario\) para evitar la situación.</span><span class="sxs-lookup"><span data-stu-id="b94a4-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="b94a4-123">Antes de comenzar, asegúrese de que se cumplen los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="b94a4-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="b94a4-124">Para depurar scripts, la aplicación debe iniciarse desde dentro de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b94a4-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="b94a4-125">No puede adjuntar un depurador a un proceso webView2 en ejecución.</span><span class="sxs-lookup"><span data-stu-id="b94a4-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="b94a4-126">Instale Visual Studio versión 16.4 preview 2 o posterior de 2019.</span><span class="sxs-lookup"><span data-stu-id="b94a4-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  
    
<span data-ttu-id="b94a4-127">Instale y configure las herramientas del depurador de scripts en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b94a4-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="b94a4-128">Complete las siguientes acciones para instalar el componente **de diagnóstico de JavaScript** en **el desarrollo de escritorio con C++**.</span><span class="sxs-lookup"><span data-stu-id="b94a4-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  
    
    1.  <span data-ttu-id="b94a4-129">En la barra Windows Explorer, escriba `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="b94a4-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1.  <span data-ttu-id="b94a4-130">Elija **Instalador de Visual Studio** para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="b94a4-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1.  <span data-ttu-id="b94a4-131">En el Instalador de Visual Studio, en la versión instalada, elija el botón **Más** y, a continuación, **elija Modificar**.</span><span class="sxs-lookup"><span data-stu-id="b94a4-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1.  <span data-ttu-id="b94a4-132">En Visual Studio, en **Cargas de trabajo,** elija la configuración **Desarrollo de escritorio en C++.**</span><span class="sxs-lookup"><span data-stu-id="b94a4-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Visual Studio Modificar la pantalla cargas de trabajo" lightbox="./media/workloads.png":::
            <span data-ttu-id="b94a4-134">Visual Studio Modificar la pantalla cargas de trabajo</span><span class="sxs-lookup"><span data-stu-id="b94a4-134">Visual Studio Modifying Workloads Screen</span></span>
        :::image-end:::  
        
    1.  <span data-ttu-id="b94a4-135">Elija **Componentes individuales**.</span><span class="sxs-lookup"><span data-stu-id="b94a4-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="b94a4-136">En el cuadro de búsqueda, escriba `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="b94a4-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="b94a4-137">Elija la configuración **de diagnóstico de JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="b94a4-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="b94a4-138">Elija **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="b94a4-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio Modificar la pestaña Componentes individuales" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="b94a4-140">Visual Studio Modificar la pestaña Componentes individuales</span><span class="sxs-lookup"><span data-stu-id="b94a4-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="b94a4-141">Habilitar la depuración de scripts para aplicaciones webView2.</span><span class="sxs-lookup"><span data-stu-id="b94a4-141">Enable script debugging for WebView2 apps.</span></span>  
    1.  <span data-ttu-id="b94a4-142">En el proyecto WebView2, abra el menú contextual \(haga clic con el botón secundario\) y elija **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="b94a4-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="b94a4-143">En Propiedades **de configuración,** elija **Depuración**.</span><span class="sxs-lookup"><span data-stu-id="b94a4-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="b94a4-144">En Tipo **de depurador,** elija **JavaScript (WebView2).**</span><span class="sxs-lookup"><span data-stu-id="b94a4-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Visual Studio Debugging Configuration (propiedad)" lightbox="./media/enbjs.png":::
           <span data-ttu-id="b94a4-146">Visual Studio de **depuración de** propiedades de configuración</span><span class="sxs-lookup"><span data-stu-id="b94a4-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="b94a4-147">Complete las siguientes acciones para depurar la aplicación WebView2.</span><span class="sxs-lookup"><span data-stu-id="b94a4-147">Complete the following actions to debug your WebView2 app.</span></span>  

1.  <span data-ttu-id="b94a4-148">Para establecer un punto de interrupción en el código fuente, mantenga el mouse a la izquierda del número de línea y elija establecer un punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="b94a4-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="b94a4-149">El adaptador de depuración JS/TS no realiza la asignación de ruta de acceso de origen.</span><span class="sxs-lookup"><span data-stu-id="b94a4-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="b94a4-150">Debe abrir exactamente la misma ruta de acceso asociada a su WebView2.</span><span class="sxs-lookup"><span data-stu-id="b94a4-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio agregar punto de interrupción" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="b94a4-152">Visual Studio agregar punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="b94a4-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b94a4-153">Para ejecutar el depurador, elija el tamaño de bits de la plataforma y, a continuación, elija el botón de reproducción verde junto a **Local Windows Debugger**.</span><span class="sxs-lookup"><span data-stu-id="b94a4-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="b94a4-154">La aplicación se ejecuta y el depurador se conecta al primer proceso de WebView2 que se crea.</span><span class="sxs-lookup"><span data-stu-id="b94a4-154">The app runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Visual Studio Depurador Windows local" lightbox="./media/run.png"::: 
       <span data-ttu-id="b94a4-156">Visual Studio depurador **de Windows local**</span><span class="sxs-lookup"><span data-stu-id="b94a4-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b94a4-157">En la **Consola de depuración,** busque el resultado del depurador.</span><span class="sxs-lookup"><span data-stu-id="b94a4-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio Consola de depuración" lightbox="./media/console.png"::: 
       <span data-ttu-id="b94a4-159">Visual Studio de **depuración**</span><span class="sxs-lookup"><span data-stu-id="b94a4-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
## [<a name="visual-studio-code"></a><span data-ttu-id="b94a4-160">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b94a4-160">Visual Studio Code</span></span>](#tab/visualstudiocode)  

<span data-ttu-id="b94a4-161">Use Microsoft Visual Studio code para depurar scripts que se ejecutan en controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="b94a4-161">Use Microsoft Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

<span data-ttu-id="b94a4-162">En Visual Studio Code, realice las siguientes acciones para depurar el código.</span><span class="sxs-lookup"><span data-stu-id="b94a4-162">In Visual Studio Code, complete the following actions to debug your code.</span></span> 

1.  <span data-ttu-id="b94a4-163">Es necesario que el proyecto tenga un `launch.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="b94a4-163">Your project is required to have a `launch.json` file.</span></span>  <span data-ttu-id="b94a4-164">Si el proyecto no tiene un archivo, copie el siguiente fragmento de código `launch.json` y cree un nuevo `launch.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="b94a4-164">If your project doesn't have a `launch.json` file, copy the following code snippet and create a new `launch.json` file.</span></span>  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",
        "env": {
            // Customize for your app location if needed
            "Path": "%path%;e:/path/to/your/app/location; "
        },
        "useWebView": true,
        // The following two lines setup source path mapping, where `url` is the start page of your app, and `webRoot` is the top level directory with all your code files.
        "url": "file:///${workspaceFolder}/path/to/your/toplevel/foo.html",
        "webRoot": "${workspaceFolder}/path/to/your/assets"
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="b94a4-165">Visual Studio Code asignación de ruta de origen ahora requiere la dirección URL, por lo que la aplicación ahora recibe un parámetro de línea de comandos cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="b94a4-165">Visual Studio Code source path mapping now requires the URL, so your app now receives a command-line parameter when it starts.</span></span>  <span data-ttu-id="b94a4-166">Puede omitir el parámetro `url` de forma segura si es necesario.</span><span class="sxs-lookup"><span data-stu-id="b94a4-166">You may safely ignore the `url` parameter if needed.</span></span>  
    
1.  <span data-ttu-id="b94a4-167">Para establecer un punto de interrupción en el código fuente, mantenga el mouse en la línea y seleccione</span><span class="sxs-lookup"><span data-stu-id="b94a4-167">To set a breakpoint in your source code, hover on the line, and select</span></span> `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="El punto de interrupción se establece en Visual Studio Code" lightbox="./media/breakpointvs.png":::
       <span data-ttu-id="b94a4-169">El punto de interrupción se establece en Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b94a4-169">Breakpoint is set in Visual Studio Code</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="b94a4-170">Ejecute el código.</span><span class="sxs-lookup"><span data-stu-id="b94a4-170">Run the code.</span></span>  
    1.  <span data-ttu-id="b94a4-171">En la **pestaña Ejecutar,** elija la configuración de inicio en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="b94a4-171">On the **Run** tab, choose the launch configuration from the dropdown menu.</span></span>  
    1.  <span data-ttu-id="b94a4-172">Para empezar a depurar la aplicación, elija Iniciar depuración, que es el triángulo verde junto a la lista desplegable de configuración de inicio.</span><span class="sxs-lookup"><span data-stu-id="b94a4-172">To start debugging your app, choose Start Debugging, which is the green triangle next to the launch configuration drop down.</span></span>  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Visual Studio Code Pestaña Ejecutar" lightbox="./media/runvs.png":::
           <span data-ttu-id="b94a4-174">Visual Studio Code Pestaña Ejecutar</span><span class="sxs-lookup"><span data-stu-id="b94a4-174">Visual Studio Code Run tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="b94a4-175">Abra **la Consola de depuración** para ver el resultado de depuración y los errores.</span><span class="sxs-lookup"><span data-stu-id="b94a4-175">Open **Debug Console** to view the debug output and errors.</span></span>  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Visual Studio Code Consola de depuración" lightbox="./media/resultsvs.png":::
       <span data-ttu-id="b94a4-177">Visual Studio Code Consola de depuración</span><span class="sxs-lookup"><span data-stu-id="b94a4-177">Visual Studio Code Debug Console</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b94a4-178">**Opciones Configuración**:</span><span class="sxs-lookup"><span data-stu-id="b94a4-178">**Advanced Settings**:</span></span>  

*   <span data-ttu-id="b94a4-179">Depuración de vista web dirigida.</span><span class="sxs-lookup"><span data-stu-id="b94a4-179">Targeted Webview debugging.</span></span> 
    
    <span data-ttu-id="b94a4-180">En algunas aplicaciones webView2, puede usar más de un control WebView2.</span><span class="sxs-lookup"><span data-stu-id="b94a4-180">In some WebView2 apps, you may use more than one WebView2 control.</span></span> <span data-ttu-id="b94a4-181">Para elegir el control WebView2 para depurar en esta situación, puede usar la depuración de webview2 dirigida</span><span class="sxs-lookup"><span data-stu-id="b94a4-181">To pick the WebView2 control to debug in this situation you can use targeted webview2 debugging</span></span> 
    
    <span data-ttu-id="b94a4-182">Abra y complete las siguientes acciones para usar la depuración `launch.json` de Webview dirigida.</span><span class="sxs-lookup"><span data-stu-id="b94a4-182">Open `launch.json` and complete the following actions to use targeted Webview debugging.</span></span>  
    
    1.  <span data-ttu-id="b94a4-183">Confirme que el `useWebview` parámetro está establecido en `true` .</span><span class="sxs-lookup"><span data-stu-id="b94a4-183">Confirm that the `useWebview` parameter is set to `true`.</span></span>  
    1.  <span data-ttu-id="b94a4-184">Agregue el `urlFilter` parámetro.</span><span class="sxs-lookup"><span data-stu-id="b94a4-184">Add the `urlFilter` parameter.</span></span>  <span data-ttu-id="b94a4-185">Cuando el control WebView2 navega a una dirección URL, el valor del parámetro se usa para comparar las cadenas que `urlFilter` aparecen en la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="b94a4-185">When the WebView2 control navigates to a URL, the `urlFilter` parameter value is used to compare strings that appear in the URL.</span></span>  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    <span data-ttu-id="b94a4-186">Al depurar la aplicación, es posible que deba pasar por el código desde el principio del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="b94a4-186">When debugging your app, you may need to step through the code from the beginning of the rendering process.</span></span> <span data-ttu-id="b94a4-187">Si está representando páginas web en sitios y no tiene acceso al código fuente, puede usar la opción, ya que las páginas web omiten parámetros no `?=value`  reconocidos.</span><span class="sxs-lookup"><span data-stu-id="b94a4-187">If you are rendering webpages on sites and you don't have access to the source code, you can use the `?=value` option, because webpages ignore unrecognized parameters.</span></span>   
    
    > [!IMPORTANT]
    > <span data-ttu-id="b94a4-188">Después de encontrar la primera coincidencia en la dirección URL, el depurador se detiene.</span><span class="sxs-lookup"><span data-stu-id="b94a4-188">After the first match is found in the URL, the debugger stops.</span></span>  <span data-ttu-id="b94a4-189">No puede depurar dos controles WebView2 al mismo tiempo porque todos los controles WebView2 comparten el puerto CDP y usan un único número de puerto.</span><span class="sxs-lookup"><span data-stu-id="b94a4-189">You cannot debug two WebView2 controls at the same time because the CDP port is shared by all WebView2 controls, and uses a single port number.</span></span>  
    
*   <span data-ttu-id="b94a4-190">Depurar procesos en ejecución</span><span class="sxs-lookup"><span data-stu-id="b94a4-190">Debug running processes</span></span>  
    
    <span data-ttu-id="b94a4-191">Es posible que deba adjuntar el depurador a los procesos de WebView2 en ejecución.</span><span class="sxs-lookup"><span data-stu-id="b94a4-191">You may need to attach the debugger to running WebView2 processes.</span></span> <span data-ttu-id="b94a4-192">Para ello, en `launch.json` , actualice el parámetro a `request` `attach` .</span><span class="sxs-lookup"><span data-stu-id="b94a4-192">To do that, in `launch.json`, update the `request` parameter to `attach`.</span></span>
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    <span data-ttu-id="b94a4-193">El control WebView2 debe abrir el puerto CDP para permitir la depuración del control WebView2.</span><span class="sxs-lookup"><span data-stu-id="b94a4-193">Your WebView2 control must open the CDP port to allow debugging of the WebView2 control.</span></span>  <span data-ttu-id="b94a4-194">El código debe crearse para asegurarse de que solo un control WebView2 tiene abierto un puerto de Protocolo para desarrolladores de Chrome (CDP), antes de iniciar el depurador.</span><span class="sxs-lookup"><span data-stu-id="b94a4-194">Your code must be built to ensure that only one WebView2 control has a Chrome Developer Protocol (CDP) port open, before starting the debugger.</span></span>  
    
*   <span data-ttu-id="b94a4-195">Opciones de seguimiento de depuración</span><span class="sxs-lookup"><span data-stu-id="b94a4-195">Debug tracing options</span></span>  
    
    <span data-ttu-id="b94a4-196">Agregue el `trace` parámetro para launch.jspara habilitar el seguimiento de depuración.</span><span class="sxs-lookup"><span data-stu-id="b94a4-196">Add the `trace` parameter to launch.json to enable debug tracing.</span></span>  
    
    1.  <span data-ttu-id="b94a4-197">Parámetro `trace` Add.</span><span class="sxs-lookup"><span data-stu-id="b94a4-197">Add `trace` parameter.</span></span>  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Guarde el resultado de depuración en un archivo de registro." lightbox="./media/tracelog.png":::
                 <span data-ttu-id="b94a4-199">Guardar resultados de depuración en un archivo de registro</span><span class="sxs-lookup"><span data-stu-id="b94a4-199">Save debug output to a log file</span></span>  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Salida detallada" lightbox="./media/verbose.png":::
                 <span data-ttu-id="b94a4-201">Visual Studio Code Depurar salida con seguimiento detallado activado</span><span class="sxs-lookup"><span data-stu-id="b94a4-201">Visual Studio Code Debug Output with verbose tracing turned on</span></span>  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   <span data-ttu-id="b94a4-202">Depurar Office complementos.</span><span class="sxs-lookup"><span data-stu-id="b94a4-202">Debug Office Add-ins.</span></span>  
    
    <span data-ttu-id="b94a4-203">Si va a depurar Office complementos, abra el código fuente del complemento en una instancia independiente de Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="b94a4-203">If you're debugging Office Add-ins, open the add-in source code in a separate instance of Visual Studio Code.</span></span>  <span data-ttu-id="b94a4-204">Abra launch.jsen la aplicación WebView2 y agregue el siguiente fragmento de código para adjuntar el depurador al Office complemento.</span><span class="sxs-lookup"><span data-stu-id="b94a4-204">Open launch.json in your WebView2 app and add the following code snippet to attach the debugger to the Office add-in.</span></span>
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   <span data-ttu-id="b94a4-205">Solución de problemas del depurador</span><span class="sxs-lookup"><span data-stu-id="b94a4-205">Troubleshooting the debugger</span></span>  
    
    <span data-ttu-id="b94a4-206">Es posible que encuentre los siguientes escenarios al usar el depurador.</span><span class="sxs-lookup"><span data-stu-id="b94a4-206">You may encounter the following scenarios when using the debugger.</span></span>  
    
    *   <span data-ttu-id="b94a4-207">El depurador no se detiene en el punto de interrupción y tiene resultados de depuración.</span><span class="sxs-lookup"><span data-stu-id="b94a4-207">The debugger doesn't stop at the breakpoint, and you have debug output.</span></span>  <span data-ttu-id="b94a4-208">Para solucionar el problema, confirme que el archivo con el punto de interrupción es el mismo archivo que usa el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="b94a4-208">To solve the issue, confirm that the file with the breakpoint is the same file that's used by the WebView2 control.</span></span>  <span data-ttu-id="b94a4-209">El depurador no realiza la asignación de ruta de acceso de origen.</span><span class="sxs-lookup"><span data-stu-id="b94a4-209">The debugger doesn't perform source path mapping.</span></span>  
    *   <span data-ttu-id="b94a4-210">No se puede adjuntar a un proceso en ejecución y se produce un error de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="b94a4-210">You can't attach to a running process, and you get a timeout error.</span></span>  <span data-ttu-id="b94a4-211">Para solucionar el problema, confirme que el control WebView2 abrió el puerto CDP.</span><span class="sxs-lookup"><span data-stu-id="b94a4-211">To solve the issue, confirm that the WebView2 control opened the CDP port.</span></span>  <span data-ttu-id="b94a4-212">Asegúrese de  `additionalBrowserArguments`  que el valor del Registro es correcto o de que las opciones son correctas.</span><span class="sxs-lookup"><span data-stu-id="b94a4-212">Ensure your `additionalBrowserArguments` value in the registry is correct, or the options are correct.</span></span>  <span data-ttu-id="b94a4-213">Para obtener más información, vaya a [additionalBrowserArguments para dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] y [additionalBrowserArguments para Win32][Webview2ReferenceWin32Webview2IdlParameters].</span><span class="sxs-lookup"><span data-stu-id="b94a4-213">For more information, navigate to [additionalBrowserArguments for dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] and [additionalBrowserArguments for Win32][Webview2ReferenceWin32Webview2IdlParameters].</span></span>  
    
* * *  

## <a name="see-also"></a><span data-ttu-id="b94a4-214">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b94a4-214">See also</span></span>  

*   <span data-ttu-id="b94a4-215">Para empezar a usar WebView2, vaya a [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="b94a4-215">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="b94a4-216">Para obtener un ejemplo completo de las funcionalidades de WebView2, vaya al repositorio [WebView2Samples][GithubMicrosoftedgeWebview2samples] en GitHub.</span><span class="sxs-lookup"><span data-stu-id="b94a4-216">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="b94a4-217">Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="b94a4-217">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="b94a4-218">Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="b94a4-218">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="b94a4-219">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="b94a4-219">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "Propiedad CoreWebView2EnvironmentOptions.AdditionalBrowserArguments (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment: global | Microsoft Docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2 API Reference | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

---
description: Más información sobre cómo depurar controles WebView2.
title: Introducción a la depuración de aplicaciones de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/21/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 78c0fb982de8ccce71a8df2b59447b55f64fdc2f
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/22/2020
ms.locfileid: "11052166"
---
# <span data-ttu-id="f7f01-104">Introducción a la depuración de aplicaciones de WebView2</span><span class="sxs-lookup"><span data-stu-id="f7f01-104">Get started debugging WebView2 applications</span></span>  

<span data-ttu-id="f7f01-105">El objetivo del control Microsoft Edge WebView2 es combinar lo mejor de las características y herramientas de desarrollo de aplicaciones nativas y Web.</span><span class="sxs-lookup"><span data-stu-id="f7f01-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native application development features and tools.</span></span>  <span data-ttu-id="f7f01-106">Al desarrollar su aplicación de WebView2, debe depurar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f7f01-106">When you develop your WebView2 application, you should debug your application.</span></span>  <span data-ttu-id="f7f01-107">En este artículo se describen las distintas herramientas que se usan para depurar el código web y nativo de la aplicación WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7f01-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 application.</span></span>  

## [<span data-ttu-id="f7f01-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f7f01-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="f7f01-109">Use [las herramientas de desarrollador de Microsoft Edge (cromo)][DevtoolsGuideChromiumMain] para depurar contenido web que se muestra en controles WebView2, de la misma manera que puede depurar para otra página web que se muestra en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f7f01-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="f7f01-110">Para abrir la DevTools, establezca el foco en el control WebView y, a continuación, use una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="f7f01-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="f7f01-111">Seleccione `F12` .</span><span class="sxs-lookup"><span data-stu-id="f7f01-111">Select `F12`.</span></span>  
*   <span data-ttu-id="f7f01-112">Seleccione `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="f7f01-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="f7f01-113">Abra el menú contextual \ (haga clic con el botón derecho \) y elija `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="f7f01-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  

<span data-ttu-id="f7f01-114">Para obtener más información, consulte [información general de DevTools][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="f7f01-114">For more information, see [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="Depuración DevTools" lightbox="./media/f12.png":::
   <span data-ttu-id="f7f01-116">Depuración DevTools</span><span class="sxs-lookup"><span data-stu-id="f7f01-116">DevTools debugging</span></span>  
:::image-end:::  

## [<span data-ttu-id="f7f01-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7f01-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="f7f01-118">Visual Studio proporciona varias herramientas de depuración para el código nativo y Web en aplicaciones de WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7f01-118">Visual Studio provides various debugging tools for web and native code in WebView2 applications.</span></span>  <span data-ttu-id="f7f01-119">En la sección de Visual Studio, el foco principal es la depuración de controles de WebView, pero los otros métodos de depuración en Visual Studio están disponibles de la forma habitual.</span><span class="sxs-lookup"><span data-stu-id="f7f01-119">In the Visual Studio section, the primary focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="f7f01-120">Use el siguiente proceso para depurar código nativo y web solo en aplicaciones Win32 o complementos de Office.</span><span class="sxs-lookup"><span data-stu-id="f7f01-120">Use the following process to debug web and native code in Win32 applications or Office Add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="f7f01-121">Cuando depure la aplicación en Visual Studio con el depurador nativo adjunto, seleccionar `F12` puede desencadenar el depurador nativo en lugar de las herramientas de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="f7f01-121">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="f7f01-122">Seleccione `Ctrl` + `Shift` + `I` o use el menú contextual \ (haga clic con el botón derecho \) para evitar la situación.</span><span class="sxs-lookup"><span data-stu-id="f7f01-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="f7f01-123">Antes de empezar, asegúrese de que se cumplan los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="f7f01-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="f7f01-124">Para depurar scripts, la aplicación debe iniciarse desde Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f7f01-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="f7f01-125">No puede adjuntar un depurador a un proceso de WebView2 en ejecución.</span><span class="sxs-lookup"><span data-stu-id="f7f01-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="f7f01-126">Instale Visual Studio 2019 versión 16,4 Preview 2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f7f01-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  

<span data-ttu-id="f7f01-127">Instale y configure las herramientas de depurador de scripts en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f7f01-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="f7f01-128">Complete las acciones siguientes para instalar el componente de **diagnóstico de JavaScript** en el **desarrollo de escritorio con C++**.</span><span class="sxs-lookup"><span data-stu-id="f7f01-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  

    1. <span data-ttu-id="f7f01-129">En la barra del explorador de Windows, escriba `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="f7f01-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1. <span data-ttu-id="f7f01-130">Elija **instalador de Visual Studio** para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="f7f01-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1. <span data-ttu-id="f7f01-131">En el instalador de Visual Studio, en la versión instalada, haga clic en el botón **más** y, a continuación, elija **modificar**.</span><span class="sxs-lookup"><span data-stu-id="f7f01-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1. <span data-ttu-id="f7f01-132">En Visual Studio, en **cargas de trabajo**, elija la opción **desarrollo de escritorio en C++** .</span><span class="sxs-lookup"><span data-stu-id="f7f01-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Pantalla modificando cargas de trabajo de Visual Studio" lightbox="./media/workloads.png":::
            <span data-ttu-id="f7f01-134">Pantalla modificando cargas de trabajo de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7f01-134">Visual Studio Modifying Workloads Screen</span></span> :::image-end:::  
        
    1.  <span data-ttu-id="f7f01-135">Elija **componentes individuales**.</span><span class="sxs-lookup"><span data-stu-id="f7f01-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="f7f01-136">En el cuadro de búsqueda, escriba `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="f7f01-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="f7f01-137">Elija la configuración de **diagnóstico de JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="f7f01-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="f7f01-138">Elija **modificar**.</span><span class="sxs-lookup"><span data-stu-id="f7f01-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Ficha modificar componentes individuales de Visual Studio" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="f7f01-140">Ficha modificar componentes individuales de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7f01-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="f7f01-141">Habilite la depuración de scripts para aplicaciones de WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7f01-141">Enable script debugging for WebView2 applications.</span></span>  
    1.  <span data-ttu-id="f7f01-142">En el proyecto WebView2, abra el menú contextual \ (haga clic con el botón derecho \) y elija **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="f7f01-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="f7f01-143">En las **propiedades de configuración**, elija **depuración**.</span><span class="sxs-lookup"><span data-stu-id="f7f01-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="f7f01-144">En el **tipo de depuración**, elija **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="f7f01-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Propiedad de configuración de depuración de Visual Studio" lightbox="./media/enbjs.png":::
           <span data-ttu-id="f7f01-146">Propiedad de configuración de **depuración** de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7f01-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="f7f01-147">Complete las acciones siguientes para depurar su aplicación de WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7f01-147">Complete the following actions to debug your WebView2 application.</span></span>  

1.  <span data-ttu-id="f7f01-148">Para establecer un punto de interrupción en el código fuente, coloque el puntero a la izquierda del número de línea y elija establecer un punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="f7f01-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="f7f01-149">El adaptador de depuración JS/TS no realiza asignaciones de ruta de origen.</span><span class="sxs-lookup"><span data-stu-id="f7f01-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="f7f01-150">Debe abrir exactamente la misma ruta asociada con su WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7f01-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Agregar punto de interrupción en Visual Studio" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="f7f01-152">Agregar punto de interrupción en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7f01-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f7f01-153">Para ejecutar el depurador, elija el tamaño de bit de la plataforma y, a continuación, elija el botón verde reproducir junto al **depurador local de Windows**.</span><span class="sxs-lookup"><span data-stu-id="f7f01-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="f7f01-154">La aplicación se ejecuta y el depurador se conecta al primer proceso WebView2 que se crea.</span><span class="sxs-lookup"><span data-stu-id="f7f01-154">The application runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Depurador local de Windows de Visual Studio" lightbox="./media/run.png"::: 
       <span data-ttu-id="f7f01-156">**Depurador local de Windows** de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7f01-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f7f01-157">En la **consola de depuración**, busque la salida del depurador.</span><span class="sxs-lookup"><span data-stu-id="f7f01-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Consola de depuración de Visual Studio" lightbox="./media/console.png"::: 
       <span data-ttu-id="f7f01-159">Consola de **depuración** de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7f01-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
## [<span data-ttu-id="f7f01-160">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="f7f01-160">Visual Studio Code</span></span>](#tab/visualstudiocode)  

<span data-ttu-id="f7f01-161">Use código de Microsoft Visual Studio para depurar scripts que se ejecutan en controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7f01-161">Use Microsoft Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

<span data-ttu-id="f7f01-162">En Visual Studio Code, completa las siguientes acciones para depurar el código.</span><span class="sxs-lookup"><span data-stu-id="f7f01-162">In Visual Studio Code, complete the following actions to debug your code.</span></span> 

1.  <span data-ttu-id="f7f01-163">Es necesario que el proyecto tenga un `launch.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="f7f01-163">Your project is required to have a `launch.json` file.</span></span>  <span data-ttu-id="f7f01-164">Si el proyecto no tiene un `launch.json` archivo, copie el siguiente fragmento de código y cree un `launch.json` archivo nuevo.</span><span class="sxs-lookup"><span data-stu-id="f7f01-164">If your project doesn't have a `launch.json` file, copy the following code snippet and create a new `launch.json` file.</span></span>  
        
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",
        "env": {
            // Customize for your application location if needed
            "Path": "%path%;e:/path/to/your/application/location; "
        },
        "useWebView": true,
    ```  
        
1.  <span data-ttu-id="f7f01-165">Para establecer un punto de interrupción en el código fuente, desplace el puntero sobre la línea y seleccione</span><span class="sxs-lookup"><span data-stu-id="f7f01-165">To set a breakpoint in your source code, hover on the line, and select</span></span> `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="El punto de interrupción se establece en código de Visual Studio" lightbox="./media/breakpointvs.png":::
       <span data-ttu-id="f7f01-167">El punto de interrupción se establece en código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7f01-167">Breakpoint is set in Visual Studio Code</span></span>  
    :::image-end:::
    
    > [!NOTE]
    > <span data-ttu-id="f7f01-168">Dado que el código de Visual Studio no realiza la asignación de origen, asegúrate de establecer puntos de interrupción en el mismo archivo que use WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7f01-168">Because Visual Studio Code does not perform source mapping, ensure you set breakpoints in the same file that WebView2 uses.</span></span>  <span data-ttu-id="f7f01-169">Si las rutas no coinciden, el código de Visual Studio no detiene el código en ejecución en el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="f7f01-169">If the paths do not match, Visual Studio Code does not pause the running code at the breakpoint.</span></span>  
    
1.  <span data-ttu-id="f7f01-170">Ejecute el código.</span><span class="sxs-lookup"><span data-stu-id="f7f01-170">Run the code.</span></span>  
    1.  <span data-ttu-id="f7f01-171">En la pestaña **Ejecutar** , elija la configuración de inicio en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="f7f01-171">On the **Run** tab, choose the launch configuration from the dropdown menu.</span></span>  
    1.  <span data-ttu-id="f7f01-172">Para iniciar la depuración de la aplicación, elija iniciar depuración, que es el triángulo verde junto a la lista desplegable iniciar configuración.</span><span class="sxs-lookup"><span data-stu-id="f7f01-172">To start debugging your application, choose Start Debugging, which is the green triangle next to the launch configuration drop down.</span></span>  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Pestaña ejecución de código de Visual Studio" lightbox="./media/runvs.png":::
           <span data-ttu-id="f7f01-174">Pestaña ejecución de código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7f01-174">Visual Studio Code Run tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="f7f01-175">Abra la **consola de depuración** para ver los errores y resultados de la depuración.</span><span class="sxs-lookup"><span data-stu-id="f7f01-175">Open **Debug Console** to view the debug output and errors.</span></span>  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Consola de depuración de código de Visual Studio" lightbox="./media/resultsvs.png":::
       <span data-ttu-id="f7f01-177">Consola de depuración de código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7f01-177">Visual Studio Code Debug Console</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f7f01-178">**Configuración avanzada**:</span><span class="sxs-lookup"><span data-stu-id="f7f01-178">**Advanced Settings**:</span></span>  

*   <span data-ttu-id="f7f01-179">Depuración de WebView dirigida.</span><span class="sxs-lookup"><span data-stu-id="f7f01-179">Targeted Webview debugging.</span></span> 

    <span data-ttu-id="f7f01-180">En algunas aplicaciones WebView2, puedes usar más de un control de WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7f01-180">In some WebView2 applications, you may use more than one WebView2 control.</span></span> <span data-ttu-id="f7f01-181">Para seleccionar el control WebView2 para depurar en esta situación, puede usar la depuración de WebView2 de destino</span><span class="sxs-lookup"><span data-stu-id="f7f01-181">To pick the WebView2 control to debug in this situation you can use targeted webview2 debugging</span></span> 
    
    <span data-ttu-id="f7f01-182">Abra `launch.json` y complete las siguientes acciones para usar la depuración de WebView dirigida.</span><span class="sxs-lookup"><span data-stu-id="f7f01-182">Open `launch.json` and complete the following actions to use targeted Webview debugging.</span></span>  
    
    1.  <span data-ttu-id="f7f01-183">Confirme que el `useWebview` parámetro está establecido en `true` .</span><span class="sxs-lookup"><span data-stu-id="f7f01-183">Confirm that the `useWebview` parameter is set to `true`.</span></span>  
    1.  <span data-ttu-id="f7f01-184">Agregue el `urlFilter` parámetro.</span><span class="sxs-lookup"><span data-stu-id="f7f01-184">Add the `urlFilter` parameter.</span></span>  <span data-ttu-id="f7f01-185">Cuando el control WebView2 navega a una dirección URL, el `urlFilter` valor del parámetro se usa para comparar cadenas que aparecen en la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f7f01-185">When the WebView2 control navigates to a URL, the `urlFilter` parameter value is used to compare strings that appear in the URL.</span></span>  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    <span data-ttu-id="f7f01-186">Al depurar la aplicación, es posible que tenga que recorrer el código desde el principio del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="f7f01-186">When debugging your application, you may need to step through the code from the beginning of the rendering process.</span></span> <span data-ttu-id="f7f01-187">Si está representando páginas web en sitios y no tiene acceso al código fuente, puede usar la `?=value`  opción, porque las páginas web omiten los parámetros no reconocidos.</span><span class="sxs-lookup"><span data-stu-id="f7f01-187">If you are rendering webpages on sites and you don't have access to the source code, you can use the `?=value` option, because webpages ignore unrecognized parameters.</span></span>   
    
    > [!IMPORTANT]
    > <span data-ttu-id="f7f01-188">Después de que se encuentre la primera coincidencia en la dirección URL, el depurador se detendrá.</span><span class="sxs-lookup"><span data-stu-id="f7f01-188">After the first match is found in the URL, the debugger stops.</span></span>  <span data-ttu-id="f7f01-189">No se pueden depurar dos controles de WebView2 al mismo tiempo porque el puerto CDP está compartido por todos los controles de WebView2 y usa un único número de puerto.</span><span class="sxs-lookup"><span data-stu-id="f7f01-189">You cannot debug two WebView2 controls at the same time because the CDP port is shared by all WebView2 controls, and uses a single port number.</span></span>  
    
*   <span data-ttu-id="f7f01-190">Depurar procesos en ejecución</span><span class="sxs-lookup"><span data-stu-id="f7f01-190">Debug running processes</span></span>  
    
    <span data-ttu-id="f7f01-191">Es posible que necesite adjuntar el depurador para ejecutar procesos de WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7f01-191">You may need to attach the debugger to running WebView2 processes.</span></span> <span data-ttu-id="f7f01-192">Para hacerlo, en `launch.json` , actualice el `request` parámetro a `attach` .</span><span class="sxs-lookup"><span data-stu-id="f7f01-192">To do that, in `launch.json`, update the `request` parameter to `attach`.</span></span>
        
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
        
    <span data-ttu-id="f7f01-193">El control WebView2 debe abrir el puerto CDP para permitir la depuración del control WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7f01-193">Your WebView2 control must open the CDP port to allow debugging of the WebView2 control.</span></span>  <span data-ttu-id="f7f01-194">Para asegurarte de que solo un control de WebView2 tiene abierto un puerto de protocolo de desarrollador de cromo (CDP) antes de iniciar el depurador, debes compilar el código.</span><span class="sxs-lookup"><span data-stu-id="f7f01-194">Your code must be built to ensure that only one WebView2 control has a Chrome Developer Protocol (CDP) port open, before starting the debugger.</span></span>  
    
*   <span data-ttu-id="f7f01-195">Depurar opciones de seguimiento</span><span class="sxs-lookup"><span data-stu-id="f7f01-195">Debug tracing options</span></span>  
    
    <span data-ttu-id="f7f01-196">Agregue el `trace` parámetro a launch.jsactivado para habilitar el seguimiento de depuración.</span><span class="sxs-lookup"><span data-stu-id="f7f01-196">Add the `trace` parameter to launch.json to enable debug tracing.</span></span>  
    
    1.  <span data-ttu-id="f7f01-197">Agregar `trace` parámetro.</span><span class="sxs-lookup"><span data-stu-id="f7f01-197">Add `trace` parameter.</span></span>  
        
 
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Guarde el resultado de depuración en un archivo de registro." lightbox="./media/tracelog.png":::
                 <span data-ttu-id="f7f01-199">Guardar el resultado de la depuración en un archivo de registro</span><span class="sxs-lookup"><span data-stu-id="f7f01-199">Save debug output to a log file</span></span>  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Resultado detallado" lightbox="./media/verbose.png":::
                 <span data-ttu-id="f7f01-201">Salida de depuración de código de Visual Studio con seguimiento detallado activado</span><span class="sxs-lookup"><span data-stu-id="f7f01-201">Visual Studio Code Debug Output with verbose tracing turned on</span></span>  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   <span data-ttu-id="f7f01-202">Depure complementos de Office.</span><span class="sxs-lookup"><span data-stu-id="f7f01-202">Debug Office Add-ins.</span></span>
    
    <span data-ttu-id="f7f01-203">Si depura complementos de Office, abra el código fuente del complemento en una instancia independiente de código de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f7f01-203">If you're debugging Office Add-ins, open the add-in source code in a separate instance of Visual Studio Code.</span></span>  <span data-ttu-id="f7f01-204">Abra launch.jsen la aplicación WebView2 y agregue el siguiente fragmento de código para adjuntar el depurador al complemento de Office.</span><span class="sxs-lookup"><span data-stu-id="f7f01-204">Open launch.json in your WebView2 application and add the following code snippet to attach the debugger to the Office add-in.</span></span>
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   <span data-ttu-id="f7f01-205">Solución de problemas del depurador</span><span class="sxs-lookup"><span data-stu-id="f7f01-205">Troubleshooting the debugger</span></span>  
    
    <span data-ttu-id="f7f01-206">Puede encontrarse con los siguientes escenarios al utilizar el depurador.</span><span class="sxs-lookup"><span data-stu-id="f7f01-206">You may encounter the following scenarios when using the debugger.</span></span>  

    *   <span data-ttu-id="f7f01-207">El depurador no se detiene en el punto de interrupción y tiene un resultado de depuración.</span><span class="sxs-lookup"><span data-stu-id="f7f01-207">The debugger doesn't stop at the breakpoint, and you have debug output.</span></span>  <span data-ttu-id="f7f01-208">Para solucionar el problema, confirme que el archivo con el punto de interrupción es el mismo archivo utilizado por el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7f01-208">To solve the issue, confirm that the file with the breakpoint is the same file that's used by the WebView2 control.</span></span>  <span data-ttu-id="f7f01-209">El depurador no realiza la asignación de la ruta de origen.</span><span class="sxs-lookup"><span data-stu-id="f7f01-209">The debugger doesn't perform source path mapping.</span></span>  
    *   <span data-ttu-id="f7f01-210">No puede adjuntar a un proceso en ejecución y recibe un error de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="f7f01-210">You can't attach to a running process, and you get a timeout error.</span></span>  <span data-ttu-id="f7f01-211">Para solucionar el problema, confirme que el control WebView2 abrió el puerto CDP.</span><span class="sxs-lookup"><span data-stu-id="f7f01-211">To solve the issue, confirm that the WebView2 control opened the CDP port.</span></span>  <span data-ttu-id="f7f01-212">Asegúrese de  `additionalBrowserArguments`  que su valor en el registro es correcto o de que las opciones son correctas.</span><span class="sxs-lookup"><span data-stu-id="f7f01-212">Ensure your `additionalBrowserArguments` value in the registry is correct, or the options are correct.</span></span>  <span data-ttu-id="f7f01-213">Para obtener más información, consulte [additionalBrowserArguments for dotnet] [Webview2ReferenceDotnet09515MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] and [additionalBrowserArguments for Win32] [Webview2ReferenceWin3209538Webview2IdlParameters].</span><span class="sxs-lookup"><span data-stu-id="f7f01-213">For more information, see [additionalBrowserArguments for dotnet][Webview2ReferenceDotnet09515MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] and [additionalBrowserArguments for Win32][Webview2ReferenceWin3209538Webview2IdlParameters].</span></span>  
    
* * *  


* * *  

## <span data-ttu-id="f7f01-214">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f7f01-214">See also</span></span>  

*   <span data-ttu-id="f7f01-215">Para comenzar a usar WebView2, consulte [WebView2 guías de introducción][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="f7f01-215">To get started using WebView2, see [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="f7f01-216">Para obtener un ejemplo completo de las capacidades de WebView2, consulta el repositorio de [WebView2Samples][GithubMicrosoftedgeWebview2samples] en github.</span><span class="sxs-lookup"><span data-stu-id="f7f01-216">For a comprehensive example of WebView2 capabilities, see the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="f7f01-217">Para obtener información más detallada sobre las API de WebView2, consulta referencia de la [API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="f7f01-217">For more detailed information about WebView2 APIs, see [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="f7f01-218">Para obtener más información sobre WebView2, consulte [recursos WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="f7f01-218">For more information about WebView2, see [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="f7f01-219">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f7f01-219">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions clase | Microsoft docs"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-Globals | Microsoft docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Referencia de la API de Microsoft Edge WebView2 | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "¿Qué novedades hay? -Depurador de JavaScript para Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicaciones de WebView de Microsoft Edge (cromo): depurador de código de Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  

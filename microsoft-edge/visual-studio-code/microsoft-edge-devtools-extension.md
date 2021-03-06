---
description: Cómo usar elementos para Microsoft Edge (Chromium) desde Visual Studio código
title: Elementos para Microsoft Edge (Chromium) de Visual Studio código
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, vs code, visual studio code, elements
ms.openlocfilehash: 83bac187fa2a9b1766a52f3f2cd176f171846e02
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398458"
---
# <a name="microsoft-edge-devtools-for-visual-studio-code-extension"></a><span data-ttu-id="2c488-104">Microsoft Edge DevTools para la Visual Studio de código</span><span class="sxs-lookup"><span data-stu-id="2c488-104">Microsoft Edge DevTools for Visual Studio Code extension</span></span>  

<span data-ttu-id="2c488-105">Usar</span><span class="sxs-lookup"><span data-stu-id="2c488-105">Use</span></span> <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] --><span data-ttu-id="2c488-106">esta extensión para tener acceso en Microsoft Edge DevTools dentro de [Microsoft Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="2c488-106">this extension to access in Microsoft Edge DevTools inside [Microsoft Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="2c488-107">Tiene acceso a las herramientas **Elements** y **Network** en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2c488-107">You have access to the **Elements** and **Network** tools in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="2c488-108">Puede iniciar o adjuntar a una instancia de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c488-108">You may either launch or attach to an instance of Microsoft Edge.</span></span>  <span data-ttu-id="2c488-109">Después de conectarse, puede mostrar la estructura HTML en tiempo de ejecución, modificar el diseño, solucionar problemas de estilo e inspeccionar el tráfico de red.</span><span class="sxs-lookup"><span data-stu-id="2c488-109">After you connect you may display the runtime HTML structure, alter the layout, fix styling issues, and inspect network traffic.</span></span>  

## <a name="elements-tool"></a><span data-ttu-id="2c488-110">Herramienta Elementos</span><span class="sxs-lookup"><span data-stu-id="2c488-110">Elements tool</span></span>  

<span data-ttu-id="2c488-111">De forma predeterminada, la extensión inicia una instancia del explorador en una ventana única y le proporciona la funcionalidad **Elements** de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2c488-111">By default, the extension launches a browser instance in a unique window and gives you the **Elements** functionality of Microsoft Edge DevTools.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools para Visual Studio código que se ejecuta con una ventana completa del explorador" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   <span data-ttu-id="2c488-113">Microsoft Edge DevTools para Visual Studio código que se ejecuta con una ventana completa del explorador</span><span class="sxs-lookup"><span data-stu-id="2c488-113">Microsoft Edge DevTools for Visual Studio Code running with a full browser window</span></span>  
:::image-end:::  

<span data-ttu-id="2c488-114">En la configuración de extensión, puede habilitar más funciones como **Modo sin cabeza** y **Red**.</span><span class="sxs-lookup"><span data-stu-id="2c488-114">In the extension settings, you may enable more functionality like **Headless Mode** and **Network**.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Habilitar (o deshabilitar) el modo sin cabeza y la inspección de red en la configuración de extensión" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   <span data-ttu-id="2c488-116">Habilitar el modo sin cabeza \(o deshabilitar\) y la inspección de red en la configuración de extensión</span><span class="sxs-lookup"><span data-stu-id="2c488-116">Enabling \(or disabling\) headless mode and Network inspection in the extension settings</span></span>  
:::image-end:::  

## <a name="headless-mode"></a><span data-ttu-id="2c488-117">Modo sin cabeza</span><span class="sxs-lookup"><span data-stu-id="2c488-117">Headless Mode</span></span>  

<span data-ttu-id="2c488-118">En modo sin cabeza, esta extensión no inicia una instancia completa del explorador para depurar.</span><span class="sxs-lookup"><span data-stu-id="2c488-118">In headless mode, this extension does not launch a full browser instance to debug.</span></span>  <span data-ttu-id="2c488-119">Ejecuta una instancia en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="2c488-119">It runs an instance in the background.</span></span>  <span data-ttu-id="2c488-120">Es posible que tenga que permanecer dentro del editor e interactuar con el explorador incrustado.</span><span class="sxs-lookup"><span data-stu-id="2c488-120">You may have to stay inside the editor and interact with the embedded browser.</span></span>  <span data-ttu-id="2c488-121">No se muestra un icono de explorador adicional en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="2c488-121">An extra browser icon is not be displayed in your task bar.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools para Visual Studio código que se ejecuta con un headless" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   <span data-ttu-id="2c488-123">Microsoft Edge DevTools para Visual Studio código que se ejecuta con un explorador sin cabeza</span><span class="sxs-lookup"><span data-stu-id="2c488-123">Microsoft Edge DevTools for Visual Studio Code running with a headless browser</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="2c488-124">En macOS, debes activar el modo sin cabeza como el modo preferido.</span><span class="sxs-lookup"><span data-stu-id="2c488-124">On macOS, you should turn on headless mode as your preferred mode.</span></span>  <span data-ttu-id="2c488-125">El uso del modo sin cabeza debe resolver un problema en el que, si la ventana no está visible, la ventana del explorador informa de que es `Not Active` .</span><span class="sxs-lookup"><span data-stu-id="2c488-125">Using headless mode should solve an issue where, if the window is not visible, the browser window reports that it is `Not Active`.</span></span>  

## <a name="network-tool"></a><span data-ttu-id="2c488-126">Herramienta Red</span><span class="sxs-lookup"><span data-stu-id="2c488-126">Network tool</span></span>  

<span data-ttu-id="2c488-127">Si también desea inspeccionar el tráfico de red de la aplicación, abra la configuración y active la **pestaña** Red.</span><span class="sxs-lookup"><span data-stu-id="2c488-127">If you also want to inspect the network traffic of your application, open the settings and turn on the **Network** tab.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Inspección de red en Microsoft Edge DevTools para Visual Studio código" lightbox="./media/edge-devtools-for-vscode-network.png":::
    <span data-ttu-id="2c488-129">Inspección de red en Microsoft Edge DevTools para Visual Studio código</span><span class="sxs-lookup"><span data-stu-id="2c488-129">Network inspection in Microsoft Edge DevTools for Visual Studio Code</span></span>  
:::image-end:::  

## <a name="launching-microsoft-edge-from-the-extension"></a><span data-ttu-id="2c488-130">Iniciar Microsoft Edge desde la extensión</span><span class="sxs-lookup"><span data-stu-id="2c488-130">Launching Microsoft Edge From the extension</span></span>  

<span data-ttu-id="2c488-131">Vaya a Herramientas de Microsoft Edge en la **barra de actividades**.</span><span class="sxs-lookup"><span data-stu-id="2c488-131">Navigate to Microsoft Edge Tools in the **Activity Bar**.</span></span>  <span data-ttu-id="2c488-132">Junto a donde dice **Herramientas de Microsoft Edge: Destinos,** hay un signo más que abre el explorador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2c488-132">Next to where it says **Microsoft Edge Tools: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="2c488-133">Si eliges la opción **about:blank,** debes navegar a la aplicación web en el explorador para que aparezca en el **panel** Elementos de Visual Studio Código.</span><span class="sxs-lookup"><span data-stu-id="2c488-133">If you choose the **about:blank** option, you must navigate to your web app in the browser for it to appear in the **Elements** panel in Visual Studio Code.</span></span>  

## <a name="launching-microsoft-edge-from-the-debug-view"></a><span data-ttu-id="2c488-134">Iniciar Microsoft Edge desde la vista Depurar</span><span class="sxs-lookup"><span data-stu-id="2c488-134">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="2c488-135">Si está acostumbrado a usar la vista Depurar en Visual Studio, acceda a Microsoft Edge DevTools desde ella.</span><span class="sxs-lookup"><span data-stu-id="2c488-135">If you are accustomed to using the Debug view in Visual Studio Code, access Microsoft Edge DevTools from it.</span></span>  

1.  <span data-ttu-id="2c488-136">En Visual Studio, vaya a la vista Depurar</span><span class="sxs-lookup"><span data-stu-id="2c488-136">In Visual Studio Code, navigate to the Debug view</span></span> 
    *   <span data-ttu-id="2c488-137">Seleccione `Ctrl` + `Shift` + `D` en Windows/Linux \( `Command` + `Shift` + `D` en macOS\).</span><span class="sxs-lookup"><span data-stu-id="2c488-137">Select `Ctrl`+`Shift`+`D` on Windows/Linux  \(`Command`+`Shift`+`D` on macOS\).</span></span>  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  <span data-ttu-id="2c488-138">Si no tiene ninguna configuración en Visual Studio Code, complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="2c488-138">If you do not have any configurations in Visual Studio Code, complete one of the following actions.</span></span>  
>     *   <span data-ttu-id="2c488-139">Seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="2c488-139">Select `F5`.</span></span>  
>     *   <span data-ttu-id="2c488-140">Elija el **botón Reproducir** \(verde\).</span><span class="sxs-lookup"><span data-stu-id="2c488-140">Choose the **Play** \(green\) button.</span></span>  
> 1.  <span data-ttu-id="2c488-141">En el desplegable, elija **Edge** en el desplegable.</span><span class="sxs-lookup"><span data-stu-id="2c488-141">In the dropdown, choose **Edge** in the dropdown.</span></span>  
> 1.  <span data-ttu-id="2c488-142">Se `launch.json` debe mostrar un archivo que contenga la siguiente configuración.</span><span class="sxs-lookup"><span data-stu-id="2c488-142">A `launch.json` file should be displayed that contains the following configuration.</span></span>  
>     
>     ```json
>     {
>       "version": "0.2.0",
>       "configurations": [
>         {
>           "name": "Launch Microsoft Edge and open the Edge DevTools",
>           "request": "launch",
>           "type": "vscode-edge-devtools.debug",
>           "url": "http://localhost:8080"
>         }
>       ]
>     }
>     ```  
>     
> <span data-ttu-id="2c488-143">Después de cargar la configuración correcta, realice la siguiente acción.</span><span class="sxs-lookup"><span data-stu-id="2c488-143">After you load the correct configuration, complete the following action.</span></span>  

1.  <span data-ttu-id="2c488-144">Para iniciar la **herramienta Elementos** desde Visual Studio code, realice una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="2c488-144">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="2c488-145">Seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="2c488-145">Select `F5`.</span></span>  
    *   <span data-ttu-id="2c488-146">Elija el **botón Reproducir** \(verde\).</span><span class="sxs-lookup"><span data-stu-id="2c488-146">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="2c488-147">Ahora, puede realizar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="2c488-147">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="2c488-148">Obtenga acceso a una difusión en pantalla del explorador.</span><span class="sxs-lookup"><span data-stu-id="2c488-148">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="2c488-149">Inspeccione el DOM y el estilo de los componentes de la página.</span><span class="sxs-lookup"><span data-stu-id="2c488-149">Inspect the DOM and the styling of the components on your page.</span></span>  

## <a name="attaching-to-microsoft-edge"></a><span data-ttu-id="2c488-150">Adjuntar a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2c488-150">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="2c488-151">Para abrir un explorador y adjuntar la instancia a Visual Studio Code, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="2c488-151">To open a browser and attach the instance to Visual Studio Code, complete the following steps.</span></span> 

1.  <span data-ttu-id="2c488-152">Para abrir una instancia de Microsoft Edge \(Chromium\), copie y ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="2c488-152">To open an instance of Microsoft Edge \(Chromium\), copy and run the following command.</span></span>  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="2c488-153">Después de iniciar la instancia, copie y pegue el siguiente fragmento de código en el `launch.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="2c488-153">After the instance launches, copy and paste the following code snippet into your `launch.json` file.</span></span>  
    
    ```json
    {
        "type": "vscode-edge-devtools.debug",
        "request": "attach",
        "name": "Attach to Microsoft Edge and open the developer tools",
        "url": "http://localhost:3000/",
        "webRoot": "${workspaceFolder}/out",
        "port": 9222
    }
    ```  
    
1.  <span data-ttu-id="2c488-154">En Visual Studio, abra el \*\*\*\* menú desplegable Depurador y elija Adjuntar a **Microsoft Edge y abra las herramientas para desarrolladores.**</span><span class="sxs-lookup"><span data-stu-id="2c488-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span></span>  
1.  <span data-ttu-id="2c488-155">Para iniciar la **herramienta Elementos** desde Visual Studio code, realice una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="2c488-155">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="2c488-156">Seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="2c488-156">Select `F5`.</span></span>  
    *   <span data-ttu-id="2c488-157">Elija el **botón Reproducir** \(verde\).</span><span class="sxs-lookup"><span data-stu-id="2c488-157">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="2c488-158">Ahora, puede realizar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="2c488-158">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="2c488-159">Obtenga acceso a una difusión en pantalla del explorador.</span><span class="sxs-lookup"><span data-stu-id="2c488-159">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="2c488-160">Inspeccione el DOM y el estilo de los componentes de la página.</span><span class="sxs-lookup"><span data-stu-id="2c488-160">Inspect the DOM and the styling of the components on your page.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-for-visual-studio-code-extension-team"></a><span data-ttu-id="2c488-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span><span class="sxs-lookup"><span data-stu-id="2c488-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span></span>  

<span data-ttu-id="2c488-162">Envíe sus comentarios mediante [la presentación de un problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] en el repositorio de [GitHub][GithubMicrosoftVscodeEdgeDevtools] de la extensión.</span><span class="sxs-lookup"><span data-stu-id="2c488-162">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="2c488-163">Si desea ayudar a hacer</span><span class="sxs-lookup"><span data-stu-id="2c488-163">If you want to help make</span></span> <!--the Microsoft Edge DevTools for Visual Studio Code --><span data-ttu-id="2c488-164">esta extensión es mejor, sus contribuciones son bienvenidas.</span><span class="sxs-lookup"><span data-stu-id="2c488-164">this extension better, your contributions are welcome.</span></span>  <span data-ttu-id="2c488-165">Encuentre todo lo que necesita para empezar en el repositorio [de GitHub][GithubMicrosoftVscodeEdgeDevtools] de la extensión.</span><span class="sxs-lookup"><span data-stu-id="2c488-165">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio código"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Visual Studio código"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Nuevo problema: microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code"  

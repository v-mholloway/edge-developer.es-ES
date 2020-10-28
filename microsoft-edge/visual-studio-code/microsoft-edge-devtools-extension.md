---
description: Cómo usar los elementos de Microsoft Edge (cromo) del código de Visual Studio
title: Elementos de Microsoft Edge (cromo) del código de Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, elementos
ms.openlocfilehash: 81488c08a76a16b80a415cbd17cd0617df916f54
ms.sourcegitcommit: 1cfcf2c8970a6c2221cfbf09a23d36b08bd60690
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/27/2020
ms.locfileid: "11135508"
---
# <span data-ttu-id="e40df-104">Extensión de código de Microsoft Edge DevTools para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e40df-104">Microsoft Edge DevTools for Visual Studio Code extension</span></span>  

<span data-ttu-id="e40df-105">Usar</span><span class="sxs-lookup"><span data-stu-id="e40df-105">Use</span></span> <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] --><span data-ttu-id="e40df-106">Esta extensión para acceder a Microsoft Edge DevTools dentro de [Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="e40df-106">this extension to access in Microsoft Edge DevTools inside [Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="e40df-107">Tiene acceso a los **elementos** y las herramientas de **red** en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e40df-107">You have access to the **Elements** and **Network** tools in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="e40df-108">Puede iniciar o adjuntar a una instancia de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e40df-108">You may either launch or attach to an instance of Microsoft Edge.</span></span>  <span data-ttu-id="e40df-109">Después de la conexión, puede mostrar la estructura HTML en tiempo de ejecución, modificar el diseño, corregir problemas de estilo e inspeccionar el tráfico de red.</span><span class="sxs-lookup"><span data-stu-id="e40df-109">After you connect you may display the runtime HTML structure, alter the layout, fix styling issues, and inspect network traffic.</span></span>  

## <span data-ttu-id="e40df-110">Herramienta elementos</span><span class="sxs-lookup"><span data-stu-id="e40df-110">Elements tool</span></span>  

<span data-ttu-id="e40df-111">De forma predeterminada, la extensión inicia una instancia de explorador en una ventana única y proporciona la funcionalidad de **elementos** de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e40df-111">By default, the extension launches a browser instance in a unique window and gives you the **Elements** functionality of Microsoft Edge DevTools.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Código de Microsoft Edge DevTools para Visual Studio que se ejecuta en una ventana de explorador completa" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   <span data-ttu-id="e40df-113">Código de Microsoft Edge DevTools para Visual Studio que se ejecuta en una ventana de explorador completa</span><span class="sxs-lookup"><span data-stu-id="e40df-113">Microsoft Edge DevTools for Visual Studio Code running with a full browser window</span></span>  
:::image-end:::  

<span data-ttu-id="e40df-114">En la configuración de extensión, puede habilitar más funciones, como la **red**y el **modo sin encabezado** .</span><span class="sxs-lookup"><span data-stu-id="e40df-114">In the extension settings, you may enable more functionality like **Headless Mode** and **Network**.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Habilitar (o deshabilitar) el modo desatendido y la inspección de red en la configuración de la extensión" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   <span data-ttu-id="e40df-116">Habilitar \ (o deshabilitar \) el modo desatendido y la inspección de red en la configuración de la extensión</span><span class="sxs-lookup"><span data-stu-id="e40df-116">Enabling \(or disabling\) headless mode and Network inspection in the extension settings</span></span>  
:::image-end:::  

## <span data-ttu-id="e40df-117">Modo sin periféricos</span><span class="sxs-lookup"><span data-stu-id="e40df-117">Headless Mode</span></span>  

<span data-ttu-id="e40df-118">En el modo sin encabezado, esta extensión no inicia una instancia de explorador completa para depurar.</span><span class="sxs-lookup"><span data-stu-id="e40df-118">In headless mode, this extension does not launch a full browser instance to debug.</span></span>  <span data-ttu-id="e40df-119">Se ejecuta una instancia en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e40df-119">It runs an instance in the background.</span></span>  <span data-ttu-id="e40df-120">Es posible que tenga que permanecer dentro del editor e interactuar con el explorador integrado.</span><span class="sxs-lookup"><span data-stu-id="e40df-120">You may have to stay inside the editor and interact with the embedded browser.</span></span>  <span data-ttu-id="e40df-121">No se muestra un icono de explorador adicional en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="e40df-121">An extra browser icon is not be displayed in your task bar.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools para Visual Studio código que se ejecuta con un encabezado" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   <span data-ttu-id="e40df-123">Código de Microsoft Edge DevTools para Visual Studio ejecutándose con un explorador sin periféricos</span><span class="sxs-lookup"><span data-stu-id="e40df-123">Microsoft Edge DevTools for Visual Studio Code running with a headless browser</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e40df-124">En macOS, debe activar el modo sin encabezado como modo preferido.</span><span class="sxs-lookup"><span data-stu-id="e40df-124">On macOS, you should turn on headless mode as your preferred mode.</span></span>  <span data-ttu-id="e40df-125">El uso del modo desatendido debería resolver un problema en el que, si la ventana no está visible, la ventana del explorador informa que es `Not Active` .</span><span class="sxs-lookup"><span data-stu-id="e40df-125">Using headless mode should solve an issue where, if the window is not visible, the browser window reports that it is `Not Active`.</span></span>  

## <span data-ttu-id="e40df-126">Herramienta red</span><span class="sxs-lookup"><span data-stu-id="e40df-126">Network tool</span></span>  

<span data-ttu-id="e40df-127">Si también desea inspeccionar el tráfico de red de la aplicación, abra la configuración y active la pestaña **red** .</span><span class="sxs-lookup"><span data-stu-id="e40df-127">If you also want to inspect the network traffic of your application, open the settings and turn on the **Network** tab.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Inspección de red en Microsoft Edge DevTools para Visual Studio Code" lightbox="./media/edge-devtools-for-vscode-network.png":::
    <span data-ttu-id="e40df-129">Inspección de red en Microsoft Edge DevTools para Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e40df-129">Network inspection in Microsoft Edge DevTools for Visual Studio Code</span></span>  
:::image-end:::  

## <span data-ttu-id="e40df-130">Iniciando Microsoft Edge desde la extensión</span><span class="sxs-lookup"><span data-stu-id="e40df-130">Launching Microsoft Edge From the extension</span></span>  

<span data-ttu-id="e40df-131">Vaya a herramientas de Microsoft Edge en la **barra de actividades**.</span><span class="sxs-lookup"><span data-stu-id="e40df-131">Navigate to Microsoft Edge Tools in the **Activity Bar**.</span></span>  <span data-ttu-id="e40df-132">Junto a donde dice **herramientas de Microsoft Edge: destinos,** hay un signo más que abre el explorador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e40df-132">Next to where it says **Microsoft Edge Tools: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="e40df-133">Si elige la opción **acerca de: en blanco** , debe ir a la aplicación web en el explorador para que aparezca en el panel **elementos** en Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="e40df-133">If you choose the **about:blank** option, you must navigate to your web app in the browser for it to appear in the **Elements** panel in Visual Studio Code.</span></span>  

## <span data-ttu-id="e40df-134">Iniciar Microsoft Edge desde la vista de depuración</span><span class="sxs-lookup"><span data-stu-id="e40df-134">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="e40df-135">Si estás acostumbrado a usar la vista de depuración en Visual Studio Code, accede a Microsoft Edge DevTools desde ella.</span><span class="sxs-lookup"><span data-stu-id="e40df-135">If you are accustomed to using the Debug view in Visual Studio Code, access Microsoft Edge DevTools from it.</span></span>  

1.  <span data-ttu-id="e40df-136">En Visual Studio Code, navegue a la vista de depuración</span><span class="sxs-lookup"><span data-stu-id="e40df-136">In Visual Studio Code, navigate to the Debug view</span></span> 
    *   <span data-ttu-id="e40df-137">Seleccione `Ctrl` + `Shift` + `D` on Windows/Linux \ ( `Command` + `Shift` + `D` en MacOS \).</span><span class="sxs-lookup"><span data-stu-id="e40df-137">Select `Ctrl`+`Shift`+`D` on Windows/Linux  \(`Command`+`Shift`+`D` on macOS\).</span></span>  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  <span data-ttu-id="e40df-138">Si no tienes ninguna configuración en Visual Studio Code, completa una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e40df-138">If you do not have any configurations in Visual Studio Code, complete one of the following actions.</span></span>  
>     *   <span data-ttu-id="e40df-139">Seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e40df-139">Select `F5`.</span></span>  
>     *   <span data-ttu-id="e40df-140">Elija el botón **reproducir** \ (verde \).</span><span class="sxs-lookup"><span data-stu-id="e40df-140">Choose the **Play** \(green\) button.</span></span>  
> 1.  <span data-ttu-id="e40df-141">En la lista desplegable, elija **borde** en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="e40df-141">In the dropdown, choose **Edge** in the dropdown.</span></span>  
> 1.  <span data-ttu-id="e40df-142">`launch.json`Debe mostrarse un archivo que contenga la configuración siguiente.</span><span class="sxs-lookup"><span data-stu-id="e40df-142">A `launch.json` file should be displayed that contains the following configuration.</span></span>  
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
> <span data-ttu-id="e40df-143">Después de cargar la configuración correcta, complete la siguiente acción.</span><span class="sxs-lookup"><span data-stu-id="e40df-143">After you load the correct configuration, complete the following action.</span></span>  

1.  <span data-ttu-id="e40df-144">Para iniciar la herramienta **elementos** desde código de Visual Studio, realice una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e40df-144">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="e40df-145">Seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e40df-145">Select `F5`.</span></span>  
    *   <span data-ttu-id="e40df-146">Elija el botón **reproducir** \ (verde \).</span><span class="sxs-lookup"><span data-stu-id="e40df-146">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="e40df-147">Ahora, puede realizar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e40df-147">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="e40df-148">Obtener acceso al screencast de su explorador.</span><span class="sxs-lookup"><span data-stu-id="e40df-148">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="e40df-149">Inspeccione el DOM y el estilo de los componentes de la página.</span><span class="sxs-lookup"><span data-stu-id="e40df-149">Inspect the DOM and the styling of the components on your page.</span></span>  

## <span data-ttu-id="e40df-150">Adjuntar a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e40df-150">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="e40df-151">Siga los pasos que se indican a continuación para abrir un explorador y adjuntar la instancia al código de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e40df-151">To open a browser and attach the instance to Visual Studio Code, complete the following steps.</span></span> 

1.  <span data-ttu-id="e40df-152">Para abrir una instancia de Microsoft Edge \ (cromo \), copie y ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="e40df-152">To open an instance of Microsoft Edge \(Chromium\), copy and run the following command.</span></span>  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="e40df-153">Una vez iniciada la instancia, copie y pegue el siguiente fragmento de código en el `launch.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="e40df-153">After the instance launches, copy and paste the following code snippet into your `launch.json` file.</span></span>  
    
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
    
1.  <span data-ttu-id="e40df-154">En Visual Studio Code, abre el menú desplegable **Debugger** y elige **adjuntar a Microsoft Edge y abrir las herramientas para desarrolladores**.</span><span class="sxs-lookup"><span data-stu-id="e40df-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span></span>  
1.  <span data-ttu-id="e40df-155">Para iniciar la herramienta **elementos** desde código de Visual Studio, realice una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e40df-155">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="e40df-156">Seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e40df-156">Select `F5`.</span></span>  
    *   <span data-ttu-id="e40df-157">Elija el botón **reproducir** \ (verde \).</span><span class="sxs-lookup"><span data-stu-id="e40df-157">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="e40df-158">Ahora, puede realizar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e40df-158">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="e40df-159">Obtener acceso al screencast de su explorador.</span><span class="sxs-lookup"><span data-stu-id="e40df-159">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="e40df-160">Inspeccione el DOM y el estilo de los componentes de la página.</span><span class="sxs-lookup"><span data-stu-id="e40df-160">Inspect the DOM and the styling of the components on your page.</span></span>  
    
## <span data-ttu-id="e40df-161">Ponerse en contacto con el equipo de extensión de código de Microsoft Edge DevTools para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e40df-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span></span>  

<span data-ttu-id="e40df-162">Envíe sus comentarios [archivando un problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] con el [repositorio de github][GithubMicrosoftVscodeEdgeDevtools] de la extensión.</span><span class="sxs-lookup"><span data-stu-id="e40df-162">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="e40df-163">Si desea ayudar a que</span><span class="sxs-lookup"><span data-stu-id="e40df-163">If you want to help make</span></span> <!--the Microsoft Edge DevTools for Visual Studio Code --><span data-ttu-id="e40df-164">Esta ampliación mejora, tus contribuciones son bienvenidos.</span><span class="sxs-lookup"><span data-stu-id="e40df-164">this extension better, your contributions are welcome.</span></span>  <span data-ttu-id="e40df-165">Encuentra todo lo que necesitas para empezar a trabajar en el [repositorio de github][GithubMicrosoftVscodeEdgeDevtools] de la extensión.</span><span class="sxs-lookup"><span data-stu-id="e40df-165">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Código de Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Código de Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-DevTools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Nuevo problema-Microsoft/vscode-Edge-DevTools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para código de VS"  

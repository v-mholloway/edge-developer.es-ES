---
description: Cómo usar los elementos de Microsoft Edge (cromo) del código VS
title: Elementos de Microsoft Edge (cromo) del código VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, elementos
ms.openlocfilehash: ef516d8364c68b550f889bcad0fe762a73ce5f99
ms.sourcegitcommit: 652009c5cea9e75c22b077f0cbcdc0d96bd337ac
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2020
ms.locfileid: "10694865"
---
# <span data-ttu-id="f3255-104">Elementos de la extensión de código de Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="f3255-104">Elements For Microsoft Edge VS Code Extension</span></span>  

<span data-ttu-id="f3255-105">Con los [elementos de][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] la extensión de código de Microsoft Edge vs, usa la herramienta elementos del explorador Microsoft Edge en [Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="f3255-105">With the [Elements for Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] VS Code extension, use the Elements tool of the Microsoft Edge browser from within [Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="f3255-106">Al iniciar o adjuntar, la herramienta elementos se conecta a una instancia de Microsoft Edge, muestra la estructura HTML en tiempo de ejecución y le permite modificar el diseño o corregir problemas de estilo.</span><span class="sxs-lookup"><span data-stu-id="f3255-106">By either launching or attaching, the Elements tool connects to an instance of Microsoft Edge, displays the runtime HTML structure, and allows you to alter the layout or fix styling issues.</span></span>  

:::image type="complex" source="./media/elements-for-edge.gif" alt-text="Elementos de la extensión de código perimetral de VS en el trabajo":::
   <span data-ttu-id="f3255-108">Elementos de la extensión de código perimetral de VS en el trabajo</span><span class="sxs-lookup"><span data-stu-id="f3255-108">Elements for Edge VS Code extension at work</span></span>  
:::image-end:::

<!--![Elements for Edge VS Code extension at work][ImageGifElementsEdge]  -->  

## <span data-ttu-id="f3255-109">Iniciar Microsoft Edge desde la extensión de elementos</span><span class="sxs-lookup"><span data-stu-id="f3255-109">Launching Microsoft Edge From the Elements extension</span></span>  

<span data-ttu-id="f3255-110">Vaya a los elementos de la **barra de actividades**.</span><span class="sxs-lookup"><span data-stu-id="f3255-110">Navigate to Elements in the **Activity Bar**.</span></span>  <span data-ttu-id="f3255-111">Junto a donde dice **los elementos de Microsoft Edge: destinos,** hay un signo más que abre el explorador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f3255-111">Next to where it says **Elements for Microsoft Edge: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="f3255-112">Si seleccionó la opción **acerca de: en blanco** , debe ir a la aplicación web en el explorador para que aparezca en el panel elementos en vs Code.</span><span class="sxs-lookup"><span data-stu-id="f3255-112">If you selected the **about:blank** option, you must navigate to your web app in the browser for it to appear in the Elements panel in VS Code.</span></span>  

## <span data-ttu-id="f3255-113">Iniciar Microsoft Edge desde la vista de depuración</span><span class="sxs-lookup"><span data-stu-id="f3255-113">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="f3255-114">Si está acostumbrado a usar la vista de depuración en Visual Studio Code, obtenga acceso a los elementos de esa herramienta.</span><span class="sxs-lookup"><span data-stu-id="f3255-114">If you are accustomed to using the Debug view in Visual Studio Code, access Elements from that tool.</span></span>  <span data-ttu-id="f3255-115">Vaya a la vista de depuración \ ( `Ctrl` + `Shift` + `D` en Windows o `Command` + `Shift` + `D` en MacOS \).</span><span class="sxs-lookup"><span data-stu-id="f3255-115">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\).</span></span>  

<span data-ttu-id="f3255-116">Si no tiene ninguna configuración en VS Code, pulse `F5` en Windows o MacOS o seleccione el botón verde de **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="f3255-116">If you do not have any configurations in VS Code, press `F5` on Windows or macOS or select the green **Play** button.</span></span> <span data-ttu-id="f3255-117">Seleccione **borde** en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="f3255-117">Select **Edge** in the dropdown.</span></span> <span data-ttu-id="f3255-118">Debería ver un `launch.json` archivo con la configuración siguiente.</span><span class="sxs-lookup"><span data-stu-id="f3255-118">You should see a `launch.json` file with the following configuration.</span></span>  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            
            "name": "Launch Microsoft Edge and open the Elements tool",
            "request": "launch",
            "type": "vscode-edge-devtools.debug",
            "url": "http://localhost:3000"
        
        }
    ]
}
```  

<span data-ttu-id="f3255-119">Ahora que ha cargado la configuración correcta, pulse `F5` en Windows o MacOS o seleccione el botón verde de **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="f3255-119">Now that you have loaded the correct configuration, either press `F5` on Windows or macOS or select the green **Play** button.</span></span> <span data-ttu-id="f3255-120">La herramienta elementos, que le resulta familiar, desde el explorador Microsoft Edge se inicia en VS Code, lo que le permite acceder a un screencast de su explorador y examinar los componentes de la página.</span><span class="sxs-lookup"><span data-stu-id="f3255-120">The Elements tool, that is familiar to you, from the Microsoft Edge browser launches in VS Code, allowing you to access a screencast of your browser and examine the components of your page.</span></span>  

## <span data-ttu-id="f3255-121">Adjuntar a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f3255-121">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="f3255-122">Para adjuntar código de VS a una instancia de Microsoft Edge \ (cromo \), debe iniciar el explorador ejecutando el siguiente comando desde el terminal.</span><span class="sxs-lookup"><span data-stu-id="f3255-122">To attach VS Code to an instance of Microsoft Edge\(Chromium\), you must start the browser by running the following command from your terminal.</span></span>  

`start msedge --remote-debugging-port=9222`  

<span data-ttu-id="f3255-123">Una vez que se inicie la aplicación, agregue la siguiente configuración al archivo **Launch. JSON** :</span><span class="sxs-lookup"><span data-stu-id="f3255-123">Once the app has launched, add the configuration below to your **launch.json** file:</span></span>  

```json
{
    "type": "vscode-edge-devtools.debug",
    "request": "attach",
    "name": "Attach to Microsoft Edge and open the Elements tool",
    "url": "http://localhost:3000/",
    "webRoot": "${workspaceFolder}/out",
    "port": 9222
}
```  

<span data-ttu-id="f3255-124">Seleccione **adjuntar a Microsoft Edge y abra la herramienta elementos** del menú desplegable Debugger.</span><span class="sxs-lookup"><span data-stu-id="f3255-124">Select **Attach to Microsoft Edge and open the Elements tool** from the Debugger drop-down menu.</span></span>  <span data-ttu-id="f3255-125">A continuación, pulse `F5` en Windows o MacOS, o bien seleccione el botón verde de **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="f3255-125">Next, either press `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="f3255-126">Código de VS inicia la herramienta elementos, lo que permite acceder a un screencast del explorador, inspeccionar el DOM y el estilo de los componentes de la página.</span><span class="sxs-lookup"><span data-stu-id="f3255-126">VS Code launches the Elements tool, allowing you to access a screencast of your browser, inspect the DOM, and the styling of the components on your page.</span></span>  

## <span data-ttu-id="f3255-127">Ponerse en contacto con los elementos del equipo de extensión de código de Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="f3255-127">Getting in touch with the Elements for Microsoft Edge VS Code extension team</span></span>  

<span data-ttu-id="f3255-128">Envíe sus comentarios [archivando un problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] con el [repositorio de github][GithubMicrosoftVscodeEdgeDevtools] de la extensión.</span><span class="sxs-lookup"><span data-stu-id="f3255-128">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="f3255-129">Si deseas mejorar el rendimiento de los elementos de la extensión de código de Microsoft Edge VS, te agradecerás tus contribuciones.</span><span class="sxs-lookup"><span data-stu-id="f3255-129">If you want to help make the Elements for Microsoft Edge VS Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="f3255-130">Encuentra todo lo que necesitas para empezar a trabajar en el [repositorio de github][GithubMicrosoftVscodeEdgeDevtools] de la extensión.</span><span class="sxs-lookup"><span data-stu-id="f3255-130">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!-- image links -->  

<!--[ImageGifElementsEdge]: ./media/elements-for-edge.gif "Elements for Edge VS Code extension in action"  -->  
[ImagePngElementsEdge]: elementos./Media/Elements-for-Edge.png para la extensión de código perimetral de VS en la acción "  

<!--links -->  

[VscodeElementsEdge]: ./elements-for-edge.md "Elementos de la extensión de código de Microsoft Edge VS | Microsoft docs"  

[VisualstudioCode]: https://code.visualstudio.com "Código de Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Código de Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-DevTools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Nuevo problema-Microsoft/vscode-Edge-DevTools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elementos de Microsoft Edge (cromo) | Marketplace de Visual Studio"  

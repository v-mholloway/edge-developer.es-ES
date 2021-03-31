---
description: Cómo depurar Microsoft Edge (Chromium) y Microsoft Edge (EdgeHTML) desde Visual Studio código
title: Depurar Microsoft Edge (Chromium) desde Visual Studio código
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, vs code, visual studio code, depurador
ms.openlocfilehash: e36348fc1ef5e30a511e6eda73c7646a85d8717e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399298"
---
# <a name="debugger-for-microsoft-edge-visual-studio-code-extension"></a><span data-ttu-id="7b9ab-104">Depurador para Microsoft Edge Visual Studio de código</span><span class="sxs-lookup"><span data-stu-id="7b9ab-104">Debugger For Microsoft Edge Visual Studio Code Extension</span></span>  

<span data-ttu-id="7b9ab-105">Con la extensión de código Visual Studio depurador de [Microsoft Edge,][VisualstudioMarketplaceDebuggerMicrosoftEdge] depura la línea de código JavaScript front-end y consulta instrucciones directamente desde `console.log()` Visual Studio [Code][VisualstudioCode]!</span><span class="sxs-lookup"><span data-stu-id="7b9ab-105">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line by line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode]!</span></span>  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Depurador para la extensión Visual Studio código perimetral en el trabajo" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="7b9ab-107">Depurador para la extensión Visual Studio código perimetral en el trabajo</span><span class="sxs-lookup"><span data-stu-id="7b9ab-107">Debugger for Edge Visual Studio Code extension at work</span></span>  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <a name="launching-microsoft-edge"></a><span data-ttu-id="7b9ab-108">Iniciar Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7b9ab-108">Launching Microsoft Edge</span></span>  

<span data-ttu-id="7b9ab-109">Vaya a la vista Depurar \( `Ctrl` + `Shift` + `D` en Windows o `Command` + `Shift` + `D` en macOS\) en la barra **de actividades**.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-109">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\) in the **Activity Bar**.</span></span>  <span data-ttu-id="7b9ab-110">Si no tienes ninguna configuración en el código Visual Studio, selecciona en Windows o `F5` macOS o selecciona el botón **verde Reproducir.**</span><span class="sxs-lookup"><span data-stu-id="7b9ab-110">If you do not have any configurations in Visual Studio Code, select `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="7b9ab-111">Seleccione **Edge** en el desplegable.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-111">Select **Edge** in the dropdown.</span></span>  <span data-ttu-id="7b9ab-112">Debería ver un `launch.json` archivo con la siguiente configuración.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-112">You should see a `launch.json` file with the following configuration.</span></span>  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "edge",
            "request": "launch",
            "name": "Launch Edge against localhost",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```  

<span data-ttu-id="7b9ab-113">Si seleccionas en Windows o macOS o vuelves a seleccionar el botón verde Reproducir, Visual Studio Code inicia `F5` Microsoft Edge \(EdgeHTML\) y puedes depurar cualquier proyecto web que se ejecute en el puerto directamente desde Visual Studio  `8080` Code.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-113">If you select `F5` on Windows or macOS or select the green **Play** button again, Visual Studio Code launches Microsoft Edge \(EdgeHTML\) and you are able to debug any web project you have running on port `8080` directly from Visual Studio Code!</span></span>  

### <a name="microsoft-edge-chromium"></a><span data-ttu-id="7b9ab-114">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="7b9ab-114">Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="7b9ab-115">Si desea iniciar Microsoft Edge \(Chromium\), el nuevo Microsoft Edge, en lugar de Microsoft Edge \(EdgeHTML\), simplemente agregue un atributo a la configuración existente con la versión de Microsoft Edge \(Chromium\) que desea iniciar `version` \( , , o `dev` `beta` `canary` \).</span><span class="sxs-lookup"><span data-stu-id="7b9ab-115">If you want to launch Microsoft Edge \(Chromium\), the new Microsoft Edge, instead of Microsoft Edge \(EdgeHTML\), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge \(Chromium\) you want to launch \(`dev`, `beta`, or `canary`\).</span></span>  <span data-ttu-id="7b9ab-116">La siguiente configuración inicia la versión canary de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="7b9ab-116">The following configuration below launches the Canary version of Microsoft Edge \(Chromium\).</span></span>  

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Edge against localhost",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}"
}
```  

## <a name="attaching-to-microsoft-edge"></a><span data-ttu-id="7b9ab-117">Adjuntar a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7b9ab-117">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="7b9ab-118">Adjuntar Visual Studio código a Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="7b9ab-118">Attach Visual Studio Code to Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="7b9ab-119">Desde el terminal, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-119">From your terminal, run the following command.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="7b9ab-120">Agregue la configuración siguiente al `launch.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-120">Add the configuration below to your `launch.json` file.</span></span>   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

<span data-ttu-id="7b9ab-121">Si ahora ejecuta esta configuración, Visual Studio code se adjunta a Microsoft Edge \(Chromium\) y comienza la depuración.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-121">If you now run this configuration, Visual Studio Code attaches to Microsoft Edge \(Chromium\) and start debugging.</span></span>  

## <a name="getting-in-touch-with-the-elements-for-microsoft-edge-visual-studio-code-extension-team"></a><span data-ttu-id="7b9ab-122">Getting in touch with the Elements for Microsoft Edge Visual Studio Code extension team</span><span class="sxs-lookup"><span data-stu-id="7b9ab-122">Getting in touch with the Elements for Microsoft Edge Visual Studio Code extension team</span></span>    

<span data-ttu-id="7b9ab-123">Envíe sus comentarios mediante [la presentación de un problema][GithubMicrosoftVscodeEdgeDebug2NewIssue] en el repositorio de [GitHub][GithubMicrosoftVscodeEdgeDebug2] de la extensión.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-123">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDebug2NewIssue] against in the [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  <span data-ttu-id="7b9ab-124">Incluya el archivo de registro del adaptador de depuración, que se crea para cada ejecución en el `%temp%` directorio con el nombre `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="7b9ab-124">Please include the debug adapter log file, which is created for each run in the `%temp%` directory with the name `vscode-edge-debug2.txt`.</span></span>  <span data-ttu-id="7b9ab-125">Arrastre este archivo a un comentario de problema para cargarlo en GitHub.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-125">Drag this file into an issue comment to upload it to GitHub.</span></span>  

<span data-ttu-id="7b9ab-126">Para ayudar a mejorar la extensión elements for Microsoft Edge Visual Studio Code, sus contribuciones son bienvenidas.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-126">To help make the Elements for Microsoft Edge Visual Studio Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="7b9ab-127">Busca todo lo que necesitas para empezar en [github repositorio][GithubMicrosoftVscodeEdgeDebug2] de la extensión.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-127">Find everything you need to get started in [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]: ./media/debugger-for-edge.png "Debugger for Edge Visual Studio Code extension in action"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio código"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Visual Studio código"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "microsoft/vscode-edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Nuevo problema: microsoft/vscode-edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  

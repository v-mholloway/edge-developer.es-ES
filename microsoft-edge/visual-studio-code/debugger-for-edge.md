---
description: Cómo depurar Microsoft Edge (cromo) y Microsoft Edge (EdgeHTML) desde el código de VS
title: Depurar Microsoft Edge (cromo) del código VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, depurador
ms.openlocfilehash: 58bcbc927505f4c5a1f493349c3e9475cb75e1be
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695869"
---
# <span data-ttu-id="f6a99-104">Depurador para la extensión de código de Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="f6a99-104">Debugger For Microsoft Edge VS Code Extension</span></span>  

<span data-ttu-id="f6a99-105">Con el [depurador para la extensión de código de Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] vs, depura el código de JavaScript front-end por línea y consulta las `console.log()` instrucciones directamente desde [Visual Studio Code][VisualstudioCode]!</span><span class="sxs-lookup"><span data-stu-id="f6a99-105">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] VS Code extension, debug your front-end JavaScript code line by line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode]!</span></span>  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Depurador para la extensión de código perimetral de VS en el trabajo":::
   <span data-ttu-id="f6a99-107">Depurador para la extensión de código perimetral de VS en el trabajo</span><span class="sxs-lookup"><span data-stu-id="f6a99-107">Debugger for Edge VS Code extension at work</span></span>  
:::image-end:::

<!--![Debugger for Edge VS Code extension at work][ImageGifDebuggerEdge]  -->  

## <span data-ttu-id="f6a99-108">Iniciar Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6a99-108">Launching Microsoft Edge</span></span>  

<span data-ttu-id="f6a99-109">Vaya a la vista de depuración \ ( `Ctrl` + `Shift` + `D` en Windows o `Command` + `Shift` + `D` en MacOS \) en la **barra de actividades**.</span><span class="sxs-lookup"><span data-stu-id="f6a99-109">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\) in the **Activity Bar**.</span></span>  <span data-ttu-id="f6a99-110">Si no tiene ninguna configuración en VS Code, pulse `F5` en Windows o MacOS o seleccione el botón verde de **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="f6a99-110">If you do not have any configurations in VS Code, press `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="f6a99-111">Seleccione **borde** en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="f6a99-111">Select **Edge** in the dropdown.</span></span>  <span data-ttu-id="f6a99-112">Debería ver un `launch.json` archivo con la configuración siguiente.</span><span class="sxs-lookup"><span data-stu-id="f6a99-112">You should see a `launch.json` file with the following configuration.</span></span>  

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

<span data-ttu-id="f6a99-113">Si pulsa `F5` en Windows o MacOS o selecciona el botón verde **reproducir** , el código de vs inicia Microsoft Edge \ (EdgeHTML \) y podrá depurar cualquier proyecto web que se ejecute en el puerto `8080` directamente desde el código de vs.</span><span class="sxs-lookup"><span data-stu-id="f6a99-113">If you press `F5` on Windows or macOS or select the green **Play** button again, VS Code launches Microsoft Edge \(EdgeHTML\) and you are able to debug any web project you have running on port `8080` directly from VS Code!</span></span>  

### <span data-ttu-id="f6a99-114">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="f6a99-114">Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="f6a99-115">Si deseas iniciar Microsoft Edge \ (cromo \), la siguiente versión de Microsoft Edge, en lugar de Microsoft Edge \ (EdgeHTML \), simplemente agrega un `version` atributo a la configuración existente con la versión de Microsoft Edge \ (cromo \) que deseas iniciar \ ( `dev` , `beta` o `canary` \).</span><span class="sxs-lookup"><span data-stu-id="f6a99-115">If you want to launch Microsoft Edge \(Chromium\), the next version of Microsoft Edge, instead of Microsoft Edge \(EdgeHTML\), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge \(Chromium\) you want to launch \(`dev`, `beta`, or `canary`\).</span></span> <span data-ttu-id="f6a99-116">La siguiente configuración inicia la versión Canarias de Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="f6a99-116">The following configuration below launches the Canary version of Microsoft Edge \(Chromium\).</span></span>  

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

## <span data-ttu-id="f6a99-117">Adjuntar a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6a99-117">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="f6a99-118">Adjunta código de VS a Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="f6a99-118">Attach VS Code to Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="f6a99-119">Desde el terminal, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="f6a99-119">From your terminal, run the following command.</span></span>  

```console
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="f6a99-120">Agregue la configuración que se muestra a continuación al `launch.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="f6a99-120">Add the configuration below to your `launch.json` file.</span></span>   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

<span data-ttu-id="f6a99-121">Si ahora ejecuta esta configuración, VS Code se conecta a Microsoft Edge \ (cromo \) y comienza a depurar.</span><span class="sxs-lookup"><span data-stu-id="f6a99-121">If you now run this configuration, VS Code attaches to Microsoft Edge \(Chromium\) and start debugging!</span></span>  

## <span data-ttu-id="f6a99-122">Ponerse en contacto con los elementos del equipo de extensión de código de Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="f6a99-122">Getting in touch with the Elements for Microsoft Edge VS Code extension team</span></span>    

<span data-ttu-id="f6a99-123">Envíe sus comentarios [archivando un problema][GithubMicrosoftVscodeEdgeDebug2NewIssue] en el [repositorio de github][GithubMicrosoftVscodeEdgeDebug2] de la extensión.</span><span class="sxs-lookup"><span data-stu-id="f6a99-123">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDebug2NewIssue] against in the [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  <span data-ttu-id="f6a99-124">Incluya el archivo de registro del adaptador de depuración, que se crea para cada ejecución en el `%temp%` directorio con el nombre `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="f6a99-124">Please include the debug adapter log file, which is created for each run in the `%temp%` directory with the name `vscode-edge-debug2.txt`.</span></span>  <span data-ttu-id="f6a99-125">Arrastre este archivo a un Comentario de problema para cargarlo en GitHub.</span><span class="sxs-lookup"><span data-stu-id="f6a99-125">Drag this file into an issue comment to upload it to GitHub.</span></span>  

<span data-ttu-id="f6a99-126">Para que los elementos de la extensión de código de Microsoft Edge VS sean mejores, tus contribuciones son bienvenidos.</span><span class="sxs-lookup"><span data-stu-id="f6a99-126">To help make the Elements for Microsoft Edge VS Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="f6a99-127">Encuentre todo lo que necesita para empezar a trabajar en el [repositorio de github][GithubMicrosoftVscodeEdgeDebug2] de la extensión.</span><span class="sxs-lookup"><span data-stu-id="f6a99-127">Find everything you need to get started in [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge VS Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/Debugger-for-Edge.png "depurador para la extensión de código perimetral de VS en acción"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Código de Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Código de Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Nuevo problema-Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Marketplace de Visual Studio"  

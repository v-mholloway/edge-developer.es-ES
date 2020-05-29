---
description: Cómo depurar Microsoft Edge (cromo) y Microsoft Edge (EdgeHTML) desde el código de VS
title: Depurar Microsoft Edge (cromo) del código VS
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/10/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, depurador
ms.openlocfilehash: 7d8d2f87500b3e81866b49de32db91c0a525baf2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574871"
---
# <span data-ttu-id="3a3de-104">Depurador para la extensión de código de Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="3a3de-104">Debugger for Microsoft Edge VS Code extension</span></span>

<span data-ttu-id="3a3de-105">Con el [depurador de la extensión de código de Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs, puedes depurar la línea de código de JavaScript front-end por línea y ver `console.log()` todas las instrucciones directamente desde [Visual Studio Code](https://code.visualstudio.com/)!</span><span class="sxs-lookup"><span data-stu-id="3a3de-105">With the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can debug your front-end JavaScript code line by line and see `console.log()` statements all directly from [Visual Studio Code](https://code.visualstudio.com/)!</span></span>

![GIF de la extensión de depurador para Edge VS en el trabajo](./media/debugger-for-edge.gif)

## <span data-ttu-id="3a3de-107">Iniciar Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3a3de-107">Launching Microsoft Edge</span></span>

<span data-ttu-id="3a3de-108">Vaya a la vista de depuración ( `Ctrl`  +  `Shift`  +  `D` en Windows o `Command`  +  `Shift`  +  `D` en Mac) en la **barra de actividades**.</span><span class="sxs-lookup"><span data-stu-id="3a3de-108">Navigate to the Debug view (`Ctrl` + `Shift` + `D` on Windows or `Command` + `Shift` + `D` on Mac) in the **Activity Bar**.</span></span> <span data-ttu-id="3a3de-109">Si no tiene ninguna configuración en VS Code, pulse `F5` en Windows o Mac, o haga clic en el botón verde de **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="3a3de-109">If you do not have any configurations in VS Code, press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="3a3de-110">Seleccione "borde" en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="3a3de-110">Select "Edge" in the dropdown.</span></span> <span data-ttu-id="3a3de-111">Ahora verá un archivo **Launch. JSON** con la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="3a3de-111">You will now see a **launch.json** file with the following configuration:</span></span>

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

<span data-ttu-id="3a3de-112">Si ahora pulsa `F5` en Windows o Mac o vuelve a hacer clic en el botón verde **reproducir** , el código de vs iniciará Microsoft Edge (EdgeHTML) y podrá depurar cualquier proyecto web que se ejecute en el puerto **8080** directamente desde vs Code.</span><span class="sxs-lookup"><span data-stu-id="3a3de-112">If you now press `F5` on Windows or Mac or click the green **Play** button again, VS Code will launch Microsoft Edge (EdgeHTML) and you will be able to debug any web project you have running on port **8080** directly from VS Code!</span></span>

### <span data-ttu-id="3a3de-113">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="3a3de-113">Microsoft Edge (Chromium)</span></span>

<span data-ttu-id="3a3de-114">Si desea iniciar Microsoft Edge (cromo), la siguiente versión de Microsoft Edge, en lugar de Microsoft Edge (EdgeHTML), simplemente agregue un `version` atributo a la configuración existente con la versión de Microsoft Edge (cromo) que desea iniciar ( `dev` , `beta` , o `canary` ).</span><span class="sxs-lookup"><span data-stu-id="3a3de-114">If you want to launch Microsoft Edge (Chromium), the next version of Microsoft Edge, instead of Microsoft Edge (EdgeHTML), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge (Chromium) you want to launch (`dev`, `beta`, or `canary`).</span></span> <span data-ttu-id="3a3de-115">La configuración siguiente iniciará la versión Canarias de Microsoft Edge (cromo):</span><span class="sxs-lookup"><span data-stu-id="3a3de-115">The configuration below will launch the Canary version of Microsoft Edge (Chromium):</span></span>

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

## <span data-ttu-id="3a3de-116">Adjuntar a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3a3de-116">Attaching to Microsoft Edge</span></span>

<span data-ttu-id="3a3de-117">También puedes adjuntar código de VS a Microsoft Edge (cromo).</span><span class="sxs-lookup"><span data-stu-id="3a3de-117">You can also attach VS Code to Microsoft Edge (Chromium).</span></span> <span data-ttu-id="3a3de-118">Desde el terminal, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="3a3de-118">From your terminal, run the following command:</span></span>

`start msedge --remote-debugging-port=9222`

<span data-ttu-id="3a3de-119">Agregue la siguiente configuración al archivo **Launch. JSON** :</span><span class="sxs-lookup"><span data-stu-id="3a3de-119">Add the configuration below to your **launch.json** file:</span></span>

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```

<span data-ttu-id="3a3de-120">Si ahora ejecuta esta configuración, el código de VS se adjuntará a Microsoft Edge (cromo) y podrá iniciar la depuración.</span><span class="sxs-lookup"><span data-stu-id="3a3de-120">If you now run this configuration, VS Code will attach to Microsoft Edge (Chromium) and you can start debugging!</span></span>

## <span data-ttu-id="3a3de-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a3de-121">Feedback</span></span>

<span data-ttu-id="3a3de-122">Envíenos sus comentarios [archivando un problema](https://github.com/Microsoft/vscode-edge-debug2/issues/new) en el repositorio de [GitHub](https://github.com/Microsoft/vscode-edge-debug2)de esta extensión.</span><span class="sxs-lookup"><span data-stu-id="3a3de-122">Send us your feedback by [filing an issue](https://github.com/Microsoft/vscode-edge-debug2/issues/new) against this extension's [GitHub repo](https://github.com/Microsoft/vscode-edge-debug2).</span></span> <span data-ttu-id="3a3de-123">Incluya el archivo de registro del adaptador de depuración, que se crea para cada ejecución en el directorio% Temp% con el nombre `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="3a3de-123">Please include the debug adapter log file, which is created for each run in the %temp% directory with the name `vscode-edge-debug2.txt`.</span></span> <span data-ttu-id="3a3de-124">Puede arrastrar este archivo a un Comentario de problema para cargarlo en GitHub.</span><span class="sxs-lookup"><span data-stu-id="3a3de-124">You can drag this file into an issue comment to upload it to GitHub.</span></span>

<span data-ttu-id="3a3de-125">Si desea ayudarnos a mejorar esta extensión, le damos la bienvenida a sus contribuciones.</span><span class="sxs-lookup"><span data-stu-id="3a3de-125">If you want to help us make this extension better, we welcome your contributions!</span></span> <span data-ttu-id="3a3de-126">Puedes encontrar todo lo que necesitas para comenzar a usar [nuestro repositorio de github](https://github.com/Microsoft/vscode-edge-debug2).</span><span class="sxs-lookup"><span data-stu-id="3a3de-126">You can find everything you need to get started in [our GitHub repo](https://github.com/Microsoft/vscode-edge-debug2).</span></span>
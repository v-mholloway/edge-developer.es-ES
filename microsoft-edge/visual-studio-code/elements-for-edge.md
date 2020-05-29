---
description: Cómo usar los elementos de Microsoft Edge (cromo) del código VS
title: Elementos de Microsoft Edge (cromo) del código VS
author: erdraud
ms.author: erdraud
ms.date: 08/08/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, elementos
ms.openlocfilehash: 4875a4665fe1561ecf587a050bbd44e116d9ce5e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574875"
---
# <span data-ttu-id="ebf18-104">Elementos de la extensión de código de Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="ebf18-104">Elements for Microsoft Edge VS Code extension</span></span>

<span data-ttu-id="ebf18-105">Al agregar los [elementos de la extensión de código de Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs, puedes usar la herramienta elementos del explorador desde el [código de Visual Studio](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="ebf18-105">By adding the [Elements for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) VS Code extension, you can use the browser's Elements tool from within [Visual Studio Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="ebf18-106">Al iniciar o adjuntar, la herramienta elementos se conectará a una instancia de Microsoft Edge, mostrará la estructura HTML en tiempo de ejecución y le permitirá modificar el diseño o corregir problemas de estilo.</span><span class="sxs-lookup"><span data-stu-id="ebf18-106">By either launching or attaching, the Elements tool will connect to an instance of Microsoft Edge, display the runtime HTML structure, and allow you to alter the layout or fix styling issues.</span></span>

![GIF de los elementos de la extensión de código perimetral de VS en el trabajo](./media/elements-for-edge.gif)

## <span data-ttu-id="ebf18-108">Iniciar Microsoft Edge desde la extensión de elementos</span><span class="sxs-lookup"><span data-stu-id="ebf18-108">Launching Microsoft Edge From the Elements extension</span></span> 

<span data-ttu-id="ebf18-109">Vaya a los elementos de la **barra de actividades**.</span><span class="sxs-lookup"><span data-stu-id="ebf18-109">Navigate to Elements in the **Activity Bar**.</span></span> <span data-ttu-id="ebf18-110">Junto a donde dice "elementos de Microsoft Edge: destinos", hay un signo más que abrirá el explorador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ebf18-110">Next to where it says "Elements for Microsoft Edge: Targets," there is a plus sign that will open the browser for your app.</span></span> <span data-ttu-id="ebf18-111">Si seleccionó la opción *acerca de: en blanco* , tendrá que desplazarse a su aplicación web en el explorador para que aparezca en el panel elementos en vs Code.</span><span class="sxs-lookup"><span data-stu-id="ebf18-111">If you selected the *about:blank* option, you will have to navigate to your web app in the browser for it to appear in the Elements panel in VS Code.</span></span>

## <span data-ttu-id="ebf18-112">Iniciar Microsoft Edge desde la vista de depuración</span><span class="sxs-lookup"><span data-stu-id="ebf18-112">Launching Microsoft Edge from the Debug view</span></span>

<span data-ttu-id="ebf18-113">Si está acostumbrado a usar la vista de depuración en Visual Studio Code, puede obtener acceso a los elementos de esa herramienta.</span><span class="sxs-lookup"><span data-stu-id="ebf18-113">If you are accustomed to using the Debug view in Visual Studio Code, you can access Elements from that tool.</span></span> <span data-ttu-id="ebf18-114">Vaya a la vista de depuración ( `Ctrl`  +  `Shift`  +  `D` en Windows o `Command`  +  `Shift`  +  `D` en Mac).</span><span class="sxs-lookup"><span data-stu-id="ebf18-114">Navigate to the Debug view (`Ctrl` + `Shift` + `D` on Windows or `Command` + `Shift` + `D` on Mac).</span></span> 

<span data-ttu-id="ebf18-115">Si no tiene ninguna configuración en VS Code, pulse `F5` en Windows o Mac, o haga clic en el botón verde de **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="ebf18-115">If you do not have any configurations in VS Code, press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="ebf18-116">Seleccione "borde" en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="ebf18-116">Select "Edge" in the dropdown.</span></span> <span data-ttu-id="ebf18-117">Ahora verá un archivo **Launch. JSON** con la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="ebf18-117">You will now see a **launch.json** file with the following configuration:</span></span>

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

<span data-ttu-id="ebf18-118">Ahora que ha cargado la configuración correcta, pulse `F5` en Windows o Mac, o haga clic en el botón verde de **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="ebf18-118">Now that you have loaded the correct configuration, either press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="ebf18-119">La herramienta elementos que ya conoce del explorador Microsoft Edge se iniciará en VS Code, lo que le permitirá acceder a un screencast de su explorador y examinar los componentes de la página.</span><span class="sxs-lookup"><span data-stu-id="ebf18-119">The Elements tool you are familiar with from the Microsoft Edge browser will now launch in VS Code, allowing you to access a screencast of your browser and examine the components of your page.</span></span>

## <span data-ttu-id="ebf18-120">Adjuntar a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ebf18-120">Attaching to Microsoft Edge</span></span>
<span data-ttu-id="ebf18-121">Si desea adjuntar código de VS a una instancia de Microsoft Edge (cromo), debe iniciar el explorador ejecutando el siguiente comando desde su Teminal:</span><span class="sxs-lookup"><span data-stu-id="ebf18-121">If you'd like to attach VS Code to an instance of Microsoft Edge (Chromium), you must start the browser by running the following command from your teminal:</span></span>

`start msedge --remote-debugging-port=9222`

<span data-ttu-id="ebf18-122">Una vez que se inicie la aplicación, agregue la siguiente configuración al archivo **Launch. JSON** :</span><span class="sxs-lookup"><span data-stu-id="ebf18-122">Once the app has launched, add the configuration below to your **launch.json** file:</span></span>

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

<span data-ttu-id="ebf18-123">Seleccione "adjuntar a Microsoft Edge y abrir la herramienta elementos" en el menú desplegable del depurador.</span><span class="sxs-lookup"><span data-stu-id="ebf18-123">Select "Attach to Microsoft Edge and open the Elements tool" from the Debugger drop-down menu.</span></span> <span data-ttu-id="ebf18-124">A continuación, presione `F5` en Windows o Mac, o haga clic en el botón verde de **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="ebf18-124">Next, either press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="ebf18-125">El código de VS inicia la herramienta elementos, lo que permite acceder a un screencast del explorador, inspeccionar el DOM y el estilo de los componentes de la página.</span><span class="sxs-lookup"><span data-stu-id="ebf18-125">VS Code will launch the Elements tool, allowing you to access a screencast of your browser, inspect the DOM, and the styling of the components on your page.</span></span>

## <span data-ttu-id="ebf18-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ebf18-126">Feedback</span></span>
<span data-ttu-id="ebf18-127">Envíenos sus comentarios [archivando un problema](https://github.com/microsoft/vscode-edge-devtools/issues/new) en el repositorio de [GitHub](https://github.com/microsoft/vscode-edge-devtools)de esta extensión.</span><span class="sxs-lookup"><span data-stu-id="ebf18-127">Send us your feedback by [filing an issue](https://github.com/microsoft/vscode-edge-devtools/issues/new) against this extension's [GitHub repo](https://github.com/microsoft/vscode-edge-devtools).</span></span> 

<span data-ttu-id="ebf18-128">Si desea ayudarnos a mejorar esta extensión, le damos la bienvenida a sus contribuciones.</span><span class="sxs-lookup"><span data-stu-id="ebf18-128">If you want to help us make this extension better, we welcome your contributions!</span></span> <span data-ttu-id="ebf18-129">Puedes encontrar todo lo que necesitas para comenzar a usar [nuestro repositorio de github](https://github.com/microsoft/vscode-edge-devtools).</span><span class="sxs-lookup"><span data-stu-id="ebf18-129">You can find everything you need to get started in [our GitHub repo](https://github.com/microsoft/vscode-edge-devtools).</span></span>
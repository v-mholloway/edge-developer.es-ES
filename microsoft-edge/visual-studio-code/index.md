---
description: Código de Microsoft Edge (cromo) y Visual Studio
title: Visual Studio Code
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/12/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, depurador, webhint
ms.openlocfilehash: 94148864edbd43adbe2dc9f3d0c2fa0c1f7f0b43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574874"
---
# <span data-ttu-id="06ee3-104">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="06ee3-104">Visual Studio Code</span></span>

<span data-ttu-id="06ee3-105">[Visual Studio Code](https://code.visualstudio.com/Docs) es un editor de código fuente ligero pero eficaz que se ejecuta en el escritorio y está disponible para Windows, MacOS y Linux.</span><span class="sxs-lookup"><span data-stu-id="06ee3-105">[Visual Studio Code](https://code.visualstudio.com/Docs) is a lightweight but powerful source code editor which runs on your desktop and is available for Windows, macOS and Linux.</span></span> <span data-ttu-id="06ee3-106">Viene con compatibilidad integrada para JavaScript, TypeScript y node. js, por lo que es una excelente herramienta para desarrolladores web listos para utilizar.</span><span class="sxs-lookup"><span data-stu-id="06ee3-106">It comes with built-in support for JavaScript, TypeScript and Node.js so it's a great tool for web developers right out of the box!</span></span> <span data-ttu-id="06ee3-107">Vaya a [esta página](https://code.visualstudio.com/) para descargar el código de Visual Studio si aún no lo está usando.</span><span class="sxs-lookup"><span data-stu-id="06ee3-107">Head to [this page](https://code.visualstudio.com/) to download Visual Studio Code if you aren't using it yet.</span></span>

## <span data-ttu-id="06ee3-108">Extensions</span><span class="sxs-lookup"><span data-stu-id="06ee3-108">Extensions</span></span>

<!-- We want to put something like the tiles for extensions VS Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page. I think it's a web page. I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->

<span data-ttu-id="06ee3-109">Para adquirir cualquiera de las extensiones resaltadas a continuación, vaya a extensiones ( `Ctrl`  +  `Shift`  +  `X` en Windows o `Command`  +  `Shift`  +  `X` en Mac) en vs Code.</span><span class="sxs-lookup"><span data-stu-id="06ee3-109">To acquire any of the extensions highlighted below, navigate to Extensions (`Ctrl` + `Shift` + `X` on Windows or `Command` + `Shift` + `X` on Mac) in VS Code.</span></span>

<span data-ttu-id="06ee3-110">Busque la extensión específica en el Marketplace y seleccione **instalar**.</span><span class="sxs-lookup"><span data-stu-id="06ee3-110">Search the Marketplace for the specific extension and select **Install**.</span></span>

![Instalar el depurador para la extensión de código de Microsoft Edge VS](./media/vscode-debugger-install.png)

## <span data-ttu-id="06ee3-112">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="06ee3-112">Debugger for Microsoft Edge</span></span>

<span data-ttu-id="06ee3-113">Depura el código de JavaScript front-end línea por línea y muestra las `console.log()` instrucciones directamente en [Visual Studio Code](https://code.visualstudio.com/) usando la extensión [de código de depurador para Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs.</span><span class="sxs-lookup"><span data-stu-id="06ee3-113">Debug your front-end JavaScript code line by line and display `console.log()` statements directly in [Visual Studio Code](https://code.visualstudio.com/) using the the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension!</span></span>

<span data-ttu-id="06ee3-114">Usa el [depurador para la extensión de código de Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs para iniciar o adjuntar a Microsoft Edge (EdgeHTML) y Microsoft Edge (cromo).</span><span class="sxs-lookup"><span data-stu-id="06ee3-114">Use the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension to launch or attach to both Microsoft Edge (EdgeHTML) and Microsoft Edge (Chromium).</span></span> <span data-ttu-id="06ee3-115">Consulte [esta página](./debugger-for-edge.md) para obtener un tutorial sobre la depuración de Microsoft Edge desde vs Code y la configuración de ejemplo de **lanzamiento. JSON** .</span><span class="sxs-lookup"><span data-stu-id="06ee3-115">Check out [this page](./debugger-for-edge.md) for a walkthrough of debugging Microsoft Edge from VS Code and sample **launch.json** configurations.</span></span>

![GIF del depurador para la extensión de código perimetral de VS en acción.](./media/debugger-for-edge.gif)

## <span data-ttu-id="06ee3-117">Elementos de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="06ee3-117">Elements for Microsoft Edge</span></span>

<span data-ttu-id="06ee3-118">Al agregar los [elementos de la extensión de código de Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs, puedes usar la herramienta elementos del explorador desde el código de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="06ee3-118">By adding the [Elements for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) VS Code extension, you can use the browser's Elements tool from within Visual Studio Code.</span></span> <span data-ttu-id="06ee3-119">Al iniciar o adjuntar, la herramienta elementos se conectará a una instancia de Microsoft Edge, mostrará la estructura HTML en tiempo de ejecución y le permitirá modificar el diseño o corregir problemas de estilo.</span><span class="sxs-lookup"><span data-stu-id="06ee3-119">By either launching or attaching, the Elements tool will connect to an instance of Microsoft Edge, display the runtime HTML structure, and allow you to alter the layout or fix styling issues.</span></span>

<span data-ttu-id="06ee3-120">Para obtener más información, consulta [esta página](./elements-for-edge.md).</span><span class="sxs-lookup"><span data-stu-id="06ee3-120">For more information, check out [this page](./elements-for-edge.md).</span></span>

![GIF de los elementos de la extensión de código perimetral de VS en acción.](./media/elements-for-edge.gif)

## <span data-ttu-id="06ee3-122">sugerencia</span><span class="sxs-lookup"><span data-stu-id="06ee3-122">webhint</span></span>

<span data-ttu-id="06ee3-123">Use [webhint](https://webhint.io), una herramienta de desplegable personalizable, para mejorar la accesibilidad, el rendimiento, la compatibilidad entre exploradores, la compatibilidad de PWA y la seguridad de su sitio.</span><span class="sxs-lookup"><span data-stu-id="06ee3-123">Use [webhint](https://webhint.io), a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span> <span data-ttu-id="06ee3-124">Comprueba los procedimientos recomendados y los errores comunes de tu código.</span><span class="sxs-lookup"><span data-stu-id="06ee3-124">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="06ee3-125">Este proyecto de código abierto, desarrollado inicialmente por el equipo de Microsoft Edge, ahora forma parte de la [OpenJS Foundation](https://openjsf.org/).</span><span class="sxs-lookup"><span data-stu-id="06ee3-125">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation](https://openjsf.org/).</span></span> <span data-ttu-id="06ee3-126">El equipo de Microsoft Edge continúa contribuyendo a la webhint junto con los desarrolladores web de la comunidad.</span><span class="sxs-lookup"><span data-stu-id="06ee3-126">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>

![Captura de pantalla de extensión de código webhint VS](./media/webhint-extension.png)

<span data-ttu-id="06ee3-128">Identifique y solucione problemas en HTML, CSS, JavaScript, TypeScript y más agregando la [extensión webhint para vs Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span><span class="sxs-lookup"><span data-stu-id="06ee3-128">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span></span> <span data-ttu-id="06ee3-129">Las sugerencias aparecen como líneas de subrayado y se resumen en el panel problemas.</span><span class="sxs-lookup"><span data-stu-id="06ee3-129">Hints appear as inline underlines and are summarized in the Problems pane.</span></span>

<span data-ttu-id="06ee3-130">Para obtener más información, consulta [Cómo usar webhint en Visual Studio Code](./webhint.md).</span><span class="sxs-lookup"><span data-stu-id="06ee3-130">For more information, see [How to use webhint in Visual Studio Code](./webhint.md).</span></span>

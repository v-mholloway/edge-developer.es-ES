---
description: Código de Microsoft Edge (cromo) y Visual Studio
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, depurador, webhint
ms.openlocfilehash: 0d13c6eb9411f89e3a681176ade0caf8d59d46d8
ms.sourcegitcommit: 02c602379537ab3b9d0a355cea7fcf96fdbd8870
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2020
ms.locfileid: "11182755"
---
# <span data-ttu-id="4f836-104">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="4f836-104">Visual Studio Code</span></span>  

<span data-ttu-id="4f836-105">El [código de Visual Studio][VisualStudioCodeDocs] es un editor de código fuente ligero pero eficaz.</span><span class="sxs-lookup"><span data-stu-id="4f836-105">[Visual Studio Code][VisualStudioCodeDocs] is a lightweight, but powerful source code editor.</span></span>  <span data-ttu-id="4f836-106">El [código de Visual Studio][VisualStudioCodeDocs] está disponible para Windows, Linux y MacOS.</span><span class="sxs-lookup"><span data-stu-id="4f836-106">[Visual Studio Code][VisualStudioCodeDocs] is available for Windows, Linux, and macOS.</span></span>  <span data-ttu-id="4f836-107">Incluye compatibilidad integrada para JavaScript, TypeScript y Node.js, por lo que es una excelente herramienta para los desarrolladores web antes de personalizarla.</span><span class="sxs-lookup"><span data-stu-id="4f836-107">It includes built-in support for JavaScript, TypeScript, and Node.js, so it is a great tool for web developers before you customize it.</span></span>  <span data-ttu-id="4f836-108">Si aún no lo usas, descarga el [código de Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="4f836-108">If you are not using it yet, download [Visual Studio Code][VisualstudioCode].</span></span>  

## <span data-ttu-id="4f836-109">Extensions</span><span class="sxs-lookup"><span data-stu-id="4f836-109">Extensions</span></span>  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

<span data-ttu-id="4f836-110">Para adquirir cualquiera de las extensiones resaltadas a continuación, vaya a extensiones \ (seleccione `Ctrl` + `Shift` + `X` en Windows/Linux o `Command` + `Shift` + `X` en MacOS \) en código de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4f836-110">To acquire any of the extensions highlighted below, navigate to Extensions \(select `Ctrl`+`Shift`+`X` on Windows/Linux or `Command`+`Shift`+`X` on macOS\) in Visual Studio Code.</span></span>  

<span data-ttu-id="4f836-111">Busque la extensión específica en el Marketplace y elija **instalar**.</span><span class="sxs-lookup"><span data-stu-id="4f836-111">Search the Marketplace for the specific extension and choose **Install**.</span></span>  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Instalar el depurador para la extensión de código de Microsoft Edge Visual Studio" lightbox="./media/vscode-debugger-install.png":::
   <span data-ttu-id="4f836-113">Instalar el **depurador para la extensión de código de Microsoft Edge** Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4f836-113">Install the **Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Depurador para la extensión de código de Microsoft Edge Visual Studio" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         <span data-ttu-id="4f836-115">**Depurador para Microsoft Edge** Extensión de código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4f836-115">**Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="4f836-116">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4f836-116">Debugger for Microsoft Edge</span></span>](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Herramientas de Microsoft Edge para Visual Studio Code Visual Studio Code" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         <span data-ttu-id="4f836-118">**Herramientas de Microsoft Edge para Visual Studio** Extensión de código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4f836-118">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="4f836-119">Herramientas de Microsoft Edge para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4f836-119">Microsoft Edge Tools for Visual Studio Code</span></span>](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="extensión de código webhint de Visual Studio" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         <span data-ttu-id="4f836-121">**sugerencia** Extensión de código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4f836-121">**webhint** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="4f836-122">webhint</span><span class="sxs-lookup"><span data-stu-id="4f836-122">webhint</span></span>](#webhint)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="4f836-123">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4f836-123">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="4f836-124">Con el [depurador de la extensión de código de Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio, depura el código de JavaScript front-end línea a línea y muestra las `console.log()` instrucciones directamente desde el [código de Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="4f836-124">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line-by-line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode].</span></span>  
      
<span data-ttu-id="4f836-125">Con la herramienta de depuración, puedes iniciar o adjuntar a Microsoft Edge \ (EdgeHTML \) y Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="4f836-125">Using the Debugger tool, you may launch or attach to both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="4f836-126">Para obtener un tutorial sobre la depuración de Microsoft Edge desde código de Visual Studio y configuraciones de ejemplo `launch.json` , navegue hasta el [depurador de la extensión de código de Microsoft Edge Visual Studio][VisualStudioCodeDebuggerEdge].</span><span class="sxs-lookup"><span data-stu-id="4f836-126">For a walkthrough of debugging Microsoft Edge from Visual Studio Code and sample `launch.json` configurations, navigate to [Debugger For Microsoft Edge Visual Studio Code Extension][VisualStudioCodeDebuggerEdge].</span></span>  <span data-ttu-id="4f836-127">Elija la siguiente imagen para ver la extensión en acción.</span><span class="sxs-lookup"><span data-stu-id="4f836-127">Choose the following image to see the extension in action.</span></span>  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Depurador para la extensión de código perimetral de Visual Studio en acción" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="4f836-129">**Depurador para Microsoft Edge** Extensión de código de Visual Studio en acción</span><span class="sxs-lookup"><span data-stu-id="4f836-129">**Debugger for Microsoft Edge** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="4f836-130">Herramientas de Microsoft Edge para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4f836-130">Microsoft Edge Tools for Visual Studio Code</span></span>

<span data-ttu-id="4f836-131">Con la extensión de código Visual Studio [de las herramientas de Microsoft Edge para Visual Studio][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] , usa la herramienta **elementos** del explorador Microsoft Edge dentro de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4f836-131">With the [Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code extension, use the **Elements** tool of the Microsoft Edge browser within Visual Studio Code.</span></span>  <span data-ttu-id="4f836-132">Úsela para las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4f836-132">Use it for the following actions.</span></span>  

*   <span data-ttu-id="4f836-133">Adjunte a una instancia o inicie una instancia de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4f836-133">Attach to an instance or launch an instance of Microsoft Edge.</span></span>  
*   <span data-ttu-id="4f836-134">Mostrar la estructura HTML en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4f836-134">Display the runtime HTML structure.</span></span>  
*   <span data-ttu-id="4f836-135">Actualice el diseño.</span><span class="sxs-lookup"><span data-stu-id="4f836-135">Update the layout.</span></span>  
*   <span data-ttu-id="4f836-136">Solucione problemas de estilo.</span><span class="sxs-lookup"><span data-stu-id="4f836-136">Fix styling issues.</span></span>  
    
<span data-ttu-id="4f836-137">Para obtener más información, vaya a [Microsoft Edge Tools para Visual Studio Code Visual Studio Code Extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span><span class="sxs-lookup"><span data-stu-id="4f836-137">For more information, navigate to [Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Tools para Visual Studio Code Visual Studio Code Extension on Action" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   <span data-ttu-id="4f836-139">**Herramientas de Microsoft Edge para Visual Studio** Extensión de código de Visual Studio en acción</span><span class="sxs-lookup"><span data-stu-id="4f836-139">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="4f836-140">webhint</span><span class="sxs-lookup"><span data-stu-id="4f836-140">webhint</span></span>  
      
<span data-ttu-id="4f836-141">Use [webhint][WebhintMain], una herramienta de deshacer la personalizable, para mejorar la siguiente funcionalidad de su sitio.</span><span class="sxs-lookup"><span data-stu-id="4f836-141">Use [webhint][WebhintMain], a customizable linting tool, to improve the following functionality of your site.</span></span>  

*   <span data-ttu-id="4f836-142">Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="4f836-142">Accessibility</span></span>
*   <span data-ttu-id="4f836-143">Rendimiento</span><span class="sxs-lookup"><span data-stu-id="4f836-143">Performance</span></span>
*   <span data-ttu-id="4f836-144">Compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="4f836-144">Cross-browser compatibility</span></span>
*   <span data-ttu-id="4f836-145">Compatibilidad de PWA</span><span class="sxs-lookup"><span data-stu-id="4f836-145">PWA compatibility</span></span>
*   <span data-ttu-id="4f836-146">Seguridad</span><span class="sxs-lookup"><span data-stu-id="4f836-146">Security</span></span>

<span data-ttu-id="4f836-147">Comprueba el código de las prácticas de programación y los errores comunes.</span><span class="sxs-lookup"><span data-stu-id="4f836-147">It checks your code for coding practices and common errors.</span></span> <span data-ttu-id="4f836-148">El proyecto de código abierto webhint, desarrollado inicialmente por el equipo de Microsoft Edge, ahora forma parte de la [OpenJS Foundation][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="4f836-148">The webhint open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="4f836-149">El equipo de Microsoft Edge continúa contribuyendo a la webhint junto con los desarrolladores web de la comunidad.</span><span class="sxs-lookup"><span data-stu-id="4f836-149">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de pantalla de la extensión de código webhint de Visual Studio" lightbox="./media/webhint-extension.png":::
   <span data-ttu-id="4f836-151">Captura de pantalla de la extensión de código **webhint** de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4f836-151">Screenshot of **webhint** Visual Studio Code extension</span></span>  
:::image-end:::  
      
<span data-ttu-id="4f836-152">Identifique y solucione los problemas de su sitio web agregando la [extensión webhint para Visual Studio Code][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="4f836-152">Identify and fix problems in your website by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="4f836-153">Sugerencias para examinar HTML, CSS, JavaScript, TypeScript y mucho más.</span><span class="sxs-lookup"><span data-stu-id="4f836-153">Hints examine HTML, CSS, JavaScript, TypeScript, and more.</span></span>  <span data-ttu-id="4f836-154">Las sugerencias aparecen como líneas de subrayado y se resumen en el panel **problemas** .</span><span class="sxs-lookup"><span data-stu-id="4f836-154">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  
      
<span data-ttu-id="4f836-155">Para obtener más información, vaya a [Cómo usar webhint en Visual Studio Code][VisualStudioCodeWebhint].</span><span class="sxs-lookup"><span data-stu-id="4f836-155">For more information, navigate to [How to use webhint in Visual Studio Code][VisualStudioCodeWebhint].</span></span>  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Depurador para la extensión de código de Microsoft Edge Visual Studio | Microsoft docs"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Microsoft Edge DevTools para la extensión de código de Visual Studio | Microsoft docs"  
[VisualStudioCodeWebhint]: ./webhint.md "Extensión de código webhint de Visual Studio | Microsoft docs"  

[VisualstudioCode]: https://code.visualstudio.com "Código de Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Código de Visual Studio"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Marketplace de Visual Studio"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio Code | Marketplace de Visual Studio"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Marketplace de Visual Studio"  

[WebhintMain]:  https://webhint.io "sugerencia"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

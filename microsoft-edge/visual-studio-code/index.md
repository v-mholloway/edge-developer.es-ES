---
description: Microsoft Edge (Chromium) y Visual Studio Code
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, vs code, visual studio code, debugger, webhint
ms.openlocfilehash: 1aa5b66043e87ebb0f1b848dcd60e2553b378f36
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230694"
---
# <span data-ttu-id="97e1c-104">Información general sobre Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="97e1c-104">Visual Studio Code overview</span></span>  

<span data-ttu-id="97e1c-105">[Visual Studio Code][VisualStudioCodeDocs] es un editor de código fuente ligero, pero eficaz.</span><span class="sxs-lookup"><span data-stu-id="97e1c-105">[Visual Studio Code][VisualStudioCodeDocs] is a lightweight, but powerful source code editor.</span></span>  <span data-ttu-id="97e1c-106">[Visual Studio Code][VisualStudioCodeDocs] está disponible para Windows, Linux y macOS.</span><span class="sxs-lookup"><span data-stu-id="97e1c-106">[Visual Studio Code][VisualStudioCodeDocs] is available for Windows, Linux, and macOS.</span></span>  <span data-ttu-id="97e1c-107">Incluye compatibilidad integrada con JavaScript, TypeScript y Node.js, por lo que es una excelente herramienta para desarrolladores web antes de personalizarlo.</span><span class="sxs-lookup"><span data-stu-id="97e1c-107">It includes built-in support for JavaScript, TypeScript, and Node.js, so it is a great tool for web developers before you customize it.</span></span>  <span data-ttu-id="97e1c-108">Si aún no lo está usando, descargue [Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="97e1c-108">If you are not using it yet, download [Visual Studio Code][VisualstudioCode].</span></span>  

## <span data-ttu-id="97e1c-109">Extensiones</span><span class="sxs-lookup"><span data-stu-id="97e1c-109">Extensions</span></span>  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

<span data-ttu-id="97e1c-110">Para adquirir cualquiera de las extensiones resaltadas a continuación, vaya a Extensiones \(seleccione en Windows/Linux o en `Ctrl` + `Shift` + `X` `Command` + `Shift` + `X` macOS\) en Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="97e1c-110">To acquire any of the extensions highlighted below, navigate to Extensions \(select `Ctrl`+`Shift`+`X` on Windows/Linux or `Command`+`Shift`+`X` on macOS\) in Visual Studio Code.</span></span>  

<span data-ttu-id="97e1c-111">Busque en Marketplace la extensión específica y elija **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="97e1c-111">Search the Marketplace for the specific extension and choose **Install**.</span></span>  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Instalar el depurador para Microsoft Edge Visual Studio Code extensión" lightbox="./media/vscode-debugger-install.png":::
   <span data-ttu-id="97e1c-113">Instalar el **depurador para Microsoft Edge** Visual Studio Code extensión</span><span class="sxs-lookup"><span data-stu-id="97e1c-113">Install the **Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Depurador para Microsoft Edge Visual Studio Code extensión" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         <span data-ttu-id="97e1c-115">**Depurador para Microsoft Edge** Visual Studio Code extensión</span><span class="sxs-lookup"><span data-stu-id="97e1c-115">**Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="97e1c-116">Depurador de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="97e1c-116">Debugger for Microsoft Edge</span></span>](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Microsoft Edge Herramientas para Visual Studio Code Visual Studio Code extensión" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         <span data-ttu-id="97e1c-118">**Microsoft Edge herramientas para Visual Studio Code** Visual Studio Code extensión</span><span class="sxs-lookup"><span data-stu-id="97e1c-118">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="97e1c-119">Microsoft Edge Herramientas para Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="97e1c-119">Microsoft Edge Tools for Visual Studio Code</span></span>](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="extensión webhint Visual Studio Code webhint" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         <span data-ttu-id="97e1c-121">**webhint Visual Studio Code** extensión</span><span class="sxs-lookup"><span data-stu-id="97e1c-121">**webhint** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="97e1c-122">webhint</span><span class="sxs-lookup"><span data-stu-id="97e1c-122">webhint</span></span>](#webhint)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="97e1c-123">Depurador de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="97e1c-123">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="97e1c-124">Con la [extensión Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code, depure el código front-end de JavaScript línea por línea y vea instrucciones directamente desde `console.log()` [Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="97e1c-124">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line-by-line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode].</span></span>  
      
<span data-ttu-id="97e1c-125">Con la herramienta Depurador, puede iniciar o adjuntar a Microsoft Edge \(EdgeHTML\) y Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="97e1c-125">Using the Debugger tool, you may launch or attach to both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="97e1c-126">Para obtener un tutorial de depuración Microsoft Edge desde Visual Studio Code y configuraciones de ejemplo, vaya a `launch.json` Depurador para Microsoft Edge Visual Studio Code [extensión][VisualStudioCodeDebuggerEdge].</span><span class="sxs-lookup"><span data-stu-id="97e1c-126">For a walkthrough of debugging Microsoft Edge from Visual Studio Code and sample `launch.json` configurations, navigate to [Debugger For Microsoft Edge Visual Studio Code Extension][VisualStudioCodeDebuggerEdge].</span></span>  <span data-ttu-id="97e1c-127">Elija la siguiente imagen para ver la extensión en acción.</span><span class="sxs-lookup"><span data-stu-id="97e1c-127">Choose the following image to see the extension in action.</span></span>  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Depurador para la extensión Visual Studio Code edge en acción" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="97e1c-129">**Depurador para Microsoft Edge** Visual Studio Code en acción</span><span class="sxs-lookup"><span data-stu-id="97e1c-129">**Debugger for Microsoft Edge** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="97e1c-130">Microsoft Edge Herramientas para Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="97e1c-130">Microsoft Edge Tools for Visual Studio Code</span></span>

<span data-ttu-id="97e1c-131">Con la [Microsoft Edge tools para Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code, use la herramienta **Elementos** del Microsoft Edge en Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="97e1c-131">With the [Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code extension, use the **Elements** tool of the Microsoft Edge browser within Visual Studio Code.</span></span>  <span data-ttu-id="97e1c-132">Úselo para las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="97e1c-132">Use it for the following actions.</span></span>  

*   <span data-ttu-id="97e1c-133">Adjunte a una instancia o inicie una instancia de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="97e1c-133">Attach to an instance or launch an instance of Microsoft Edge.</span></span>  
*   <span data-ttu-id="97e1c-134">Mostrar la estructura HTML en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="97e1c-134">Display the runtime HTML structure.</span></span>  
*   <span data-ttu-id="97e1c-135">Actualice el diseño.</span><span class="sxs-lookup"><span data-stu-id="97e1c-135">Update the layout.</span></span>  
*   <span data-ttu-id="97e1c-136">Se solucionan problemas de estilo.</span><span class="sxs-lookup"><span data-stu-id="97e1c-136">Fix styling issues.</span></span>  
    
<span data-ttu-id="97e1c-137">Para obtener más información, vaya [a Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span><span class="sxs-lookup"><span data-stu-id="97e1c-137">For more information, navigate to [Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Herramientas para Visual Studio Code Visual Studio Code extensión en acción" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   <span data-ttu-id="97e1c-139">**Microsoft Edge herramientas para Visual Studio Code** Visual Studio Code en acción</span><span class="sxs-lookup"><span data-stu-id="97e1c-139">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="97e1c-140">webhint</span><span class="sxs-lookup"><span data-stu-id="97e1c-140">webhint</span></span>  
      
<span data-ttu-id="97e1c-141">Use [webhint][WebhintMain], una herramienta de linting personalizable, para mejorar la siguiente funcionalidad del sitio.</span><span class="sxs-lookup"><span data-stu-id="97e1c-141">Use [webhint][WebhintMain], a customizable linting tool, to improve the following functionality of your site.</span></span>  

*   <span data-ttu-id="97e1c-142">Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="97e1c-142">Accessibility</span></span>
*   <span data-ttu-id="97e1c-143">Rendimiento</span><span class="sxs-lookup"><span data-stu-id="97e1c-143">Performance</span></span>
*   <span data-ttu-id="97e1c-144">Compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="97e1c-144">Cross-browser compatibility</span></span>
*   <span data-ttu-id="97e1c-145">PWA compatibilidad</span><span class="sxs-lookup"><span data-stu-id="97e1c-145">PWA compatibility</span></span>
*   <span data-ttu-id="97e1c-146">Seguridad</span><span class="sxs-lookup"><span data-stu-id="97e1c-146">Security</span></span>

<span data-ttu-id="97e1c-147">Comprueba el código en busca de prácticas de codificación y errores comunes.</span><span class="sxs-lookup"><span data-stu-id="97e1c-147">It checks your code for coding practices and common errors.</span></span> <span data-ttu-id="97e1c-148">El proyecto de código abierto de webhint, desarrollado inicialmente por el equipo de Microsoft Edge, ahora forma parte de [OpenJS Foundation][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="97e1c-148">The webhint open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="97e1c-149">El Microsoft Edge continúa contribuyendo a la webhint junto con los desarrolladores web de la comunidad.</span><span class="sxs-lookup"><span data-stu-id="97e1c-149">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de pantalla de webhint Visual Studio Code extensión" lightbox="./media/webhint-extension.png":::
   <span data-ttu-id="97e1c-151">Captura de pantalla **de webhint** Visual Studio Code extensión</span><span class="sxs-lookup"><span data-stu-id="97e1c-151">Screenshot of **webhint** Visual Studio Code extension</span></span>  
:::image-end:::  
      
<span data-ttu-id="97e1c-152">Identifique y corrija problemas en su sitio web agregando la [extensión webhint para Visual Studio Code][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="97e1c-152">Identify and fix problems in your website by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="97e1c-153">Las sugerencias examinan HTML, CSS, JavaScript, TypeScript y mucho más.</span><span class="sxs-lookup"><span data-stu-id="97e1c-153">Hints examine HTML, CSS, JavaScript, TypeScript, and more.</span></span>  <span data-ttu-id="97e1c-154">Las sugerencias aparecen como subrayados en línea y se resumen en el **panel** Problemas.</span><span class="sxs-lookup"><span data-stu-id="97e1c-154">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  
      
<span data-ttu-id="97e1c-155">Para obtener más información, vaya [a Cómo usar webhint en Visual Studio Code][VisualStudioCodeWebhint].</span><span class="sxs-lookup"><span data-stu-id="97e1c-155">For more information, navigate to [How to use webhint in Visual Studio Code][VisualStudioCodeWebhint].</span></span>  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Depurador para Microsoft Edge Visual Studio Code extensión | Microsoft Docs"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Microsoft Edge DevTools para Visual Studio Code extensión | Microsoft Docs"  
[VisualStudioCodeWebhint]: ./webhint.md "Webhint Visual Studio Code extensión | Microsoft Docs"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Visual Studio Code"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio Code | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

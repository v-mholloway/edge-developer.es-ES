---
description: Microsoft Edge (Chromium) y Visual Studio Code
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/26/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, vs code, visual studio code, debugger, webhint
ms.openlocfilehash: 33ad223f7991eca1b87b7cb9db9c3fd9d159b557
ms.sourcegitcommit: 8924ea959b1e246aa1a3db8730cd35227abe73dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/25/2021
ms.locfileid: "11925215"
---
# <a name="visual-studio-code-overview"></a>Información general sobre Visual Studio Code  

[Visual Studio Code][VisualStudioCodeDocs] es un editor de código fuente ligero pero eficaz.  [Visual Studio Code][VisualStudioCodeDocs] está disponible para Windows, Linux y macOS.  Incluye compatibilidad integrada con JavaScript, TypeScript y Node.js, por lo que es una excelente herramienta para desarrolladores web antes de personalizarlo.  Si aún no lo está usando, descargue [Visual Studio Code][VisualstudioCode].  

## <a name="extensions"></a>Extensiones  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Para adquirir cualquiera de las extensiones resaltadas a continuación, vaya a **Extensiones** \(seleccione en Windows/Linux o en `Ctrl` + `Shift` + `X` `Command` + `Shift` + `X` macOS\) en Visual Studio Code.  

Busque la extensión en Marketplace, seleccione la extensión y, a continuación, **seleccione Instalar**.  

:::image type="complex" source="./media/vscode-edge-tools-install.png" alt-text="Instalar las herramientas Microsoft Edge para Visual Studio Code extensión" lightbox="./media/vscode-edge-tools-install.png":::
   Instalar la **Microsoft Edge tools Visual Studio Code** extensión  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Microsoft Edge Herramientas para Visual Studio Code Visual Studio Code extensión" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         **Microsoft Edge herramientas para Visual Studio Code** Visual Studio Code extensión  
      :::image-end:::  
      [Microsoft Edge Herramientas para Visual Studio Code](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="extensión webhint Visual Studio Code webhint" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         **webhint Visual Studio Code** extensión  
      :::image-end:::  
      [webhint](#webhint)  
   :::column-end:::
:::row-end:::  

## <a name="microsoft-edge-tools-for-visual-studio-code"></a>Microsoft Edge Herramientas para Visual Studio Code

Con la [Microsoft Edge tools para Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code, use la herramienta **Elementos** del Microsoft Edge en Visual Studio Code.  Úselo para las siguientes acciones.  

*   Adjunte a una instancia o inicie una instancia de Microsoft Edge.  
*   Mostrar la estructura HTML en tiempo de ejecución.  
*   Actualice el diseño.  
*   Se solucionan problemas de estilo.  
    
Para obtener más información, vaya [a Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Herramientas para Visual Studio Code Visual Studio Code extensión en acción" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   **Microsoft Edge herramientas para Visual Studio Code** Visual Studio Code en acción  
:::image-end:::  

## <a name="webhint"></a>webhint  
      
Use [webhint][WebhintMain], una herramienta de linting personalizable, para mejorar la siguiente funcionalidad del sitio.  

*   Accesibilidad
*   Rendimiento
*   Compatibilidad entre exploradores
*   PWA compatibilidad
*   Seguridad

Webhint comprueba el código en busca de prácticas de codificación y errores comunes. El proyecto de código abierto de webhint, desarrollado inicialmente por el equipo de Microsoft Edge, ahora forma parte de [OpenJS Foundation][OpenjsFoundation].  El Microsoft Edge continúa contribuyendo a la webhint junto con los desarrolladores web de la comunidad.  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de pantalla de webhint Visual Studio Code extensión" lightbox="./media/webhint-extension.png":::
   Captura de pantalla **de webhint** Visual Studio Code extensión  
:::image-end:::  
      
Identifique y corrija problemas en su sitio web agregando la [extensión webhint para Visual Studio Code][VisualstudioMarketplaceWebhint].  Las sugerencias examinan HTML, CSS, JavaScript, TypeScript y mucho más.  Las sugerencias aparecen como subrayados ondulados en el editor de texto y se resumen en el **panel** Problemas.  
      
Para obtener más información, vaya [a Cómo usar webhint en Visual Studio Code][VisualStudioCodeWebhint].  

<!--links -->  
 
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Microsoft Edge DevTools para Visual Studio Code extensión | Microsoft Docs"  
[VisualStudioCodeWebhint]: ./webhint.md "Webhint Visual Studio Code extensión | Microsoft Docs"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Visual Studio Code"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio Code | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

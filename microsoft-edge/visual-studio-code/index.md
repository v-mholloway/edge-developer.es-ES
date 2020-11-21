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
# Visual Studio Code  

El [código de Visual Studio][VisualStudioCodeDocs] es un editor de código fuente ligero pero eficaz.  El [código de Visual Studio][VisualStudioCodeDocs] está disponible para Windows, Linux y MacOS.  Incluye compatibilidad integrada para JavaScript, TypeScript y Node.js, por lo que es una excelente herramienta para los desarrolladores web antes de personalizarla.  Si aún no lo usas, descarga el [código de Visual Studio][VisualstudioCode].  

## Extensions  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Para adquirir cualquiera de las extensiones resaltadas a continuación, vaya a extensiones \ (seleccione `Ctrl` + `Shift` + `X` en Windows/Linux o `Command` + `Shift` + `X` en MacOS \) en código de Visual Studio.  

Busque la extensión específica en el Marketplace y elija **instalar**.  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Instalar el depurador para la extensión de código de Microsoft Edge Visual Studio" lightbox="./media/vscode-debugger-install.png":::
   Instalar el **depurador para la extensión de código de Microsoft Edge** Visual Studio  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Depurador para la extensión de código de Microsoft Edge Visual Studio" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         **Depurador para Microsoft Edge** Extensión de código de Visual Studio  
      :::image-end:::  
      [Depurador para Microsoft Edge](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Herramientas de Microsoft Edge para Visual Studio Code Visual Studio Code" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         **Herramientas de Microsoft Edge para Visual Studio** Extensión de código de Visual Studio  
      :::image-end:::  
      [Herramientas de Microsoft Edge para Visual Studio](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="extensión de código webhint de Visual Studio" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         **sugerencia** Extensión de código de Visual Studio  
      :::image-end:::  
      [webhint](#webhint)  
   :::column-end:::
:::row-end:::  

## Depurador para Microsoft Edge  

Con el [depurador de la extensión de código de Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio, depura el código de JavaScript front-end línea a línea y muestra las `console.log()` instrucciones directamente desde el [código de Visual Studio][VisualstudioCode].  
      
Con la herramienta de depuración, puedes iniciar o adjuntar a Microsoft Edge \ (EdgeHTML \) y Microsoft Edge \ (cromo \).  Para obtener un tutorial sobre la depuración de Microsoft Edge desde código de Visual Studio y configuraciones de ejemplo `launch.json` , navegue hasta el [depurador de la extensión de código de Microsoft Edge Visual Studio][VisualStudioCodeDebuggerEdge].  Elija la siguiente imagen para ver la extensión en acción.  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Depurador para la extensión de código perimetral de Visual Studio en acción" lightbox="./media/debugger-for-edge.gif":::
   **Depurador para Microsoft Edge** Extensión de código de Visual Studio en acción  
:::image-end:::  

## Herramientas de Microsoft Edge para Visual Studio

Con la extensión de código Visual Studio [de las herramientas de Microsoft Edge para Visual Studio][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] , usa la herramienta **elementos** del explorador Microsoft Edge dentro de Visual Studio.  Úsela para las siguientes acciones.  

*   Adjunte a una instancia o inicie una instancia de Microsoft Edge.  
*   Mostrar la estructura HTML en tiempo de ejecución.  
*   Actualice el diseño.  
*   Solucione problemas de estilo.  
    
Para obtener más información, vaya a [Microsoft Edge Tools para Visual Studio Code Visual Studio Code Extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Tools para Visual Studio Code Visual Studio Code Extension on Action" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   **Herramientas de Microsoft Edge para Visual Studio** Extensión de código de Visual Studio en acción  
:::image-end:::  

## webhint  
      
Use [webhint][WebhintMain], una herramienta de deshacer la personalizable, para mejorar la siguiente funcionalidad de su sitio.  

*   Accesibilidad
*   Rendimiento
*   Compatibilidad entre exploradores
*   Compatibilidad de PWA
*   Seguridad

Comprueba el código de las prácticas de programación y los errores comunes. El proyecto de código abierto webhint, desarrollado inicialmente por el equipo de Microsoft Edge, ahora forma parte de la [OpenJS Foundation][OpenjsFoundation].  El equipo de Microsoft Edge continúa contribuyendo a la webhint junto con los desarrolladores web de la comunidad.  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de pantalla de la extensión de código webhint de Visual Studio" lightbox="./media/webhint-extension.png":::
   Captura de pantalla de la extensión de código **webhint** de Visual Studio  
:::image-end:::  
      
Identifique y solucione los problemas de su sitio web agregando la [extensión webhint para Visual Studio Code][VisualstudioMarketplaceWebhint].  Sugerencias para examinar HTML, CSS, JavaScript, TypeScript y mucho más.  Las sugerencias aparecen como líneas de subrayado y se resumen en el panel **problemas** .  
      
Para obtener más información, vaya a [Cómo usar webhint en Visual Studio Code][VisualStudioCodeWebhint].  

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

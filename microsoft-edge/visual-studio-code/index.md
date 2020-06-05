---
description: Código de Microsoft Edge (cromo) y Visual Studio
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, depurador, webhint
ms.openlocfilehash: e178612d9db8ce3223bb5158c4557675d3314e15
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695890"
---
# Visual Studio Code  

[Visual Studio Code][VisualStudioCodeDocs] es un editor de código fuente ligero pero eficaz que se ejecuta en el escritorio y está disponible para Windows, MacOS y Linux.  Viene con compatibilidad integrada para JavaScript, TypeScript y node. js, por lo que es una excelente herramienta para desarrolladores web listos para utilizar.  Si aún no lo usas, descarga el [código de Visual Studio][VisualstudioCode].  

## Extensions  

<!--Todo: We want to put something like the tiles for extensions VS Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Para adquirir cualquiera de las extensiones resaltadas a continuación, vaya a Extensions \ ( `Ctrl` + `Shift` + `X` en Windows o `Command` + `Shift` + `X` en MacOS \) en vs Code.  

Busque la extensión específica en el Marketplace y seleccione **instalar**.  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Instalar el depurador para la extensión de código de Microsoft Edge VS":::
   Instalar el depurador para la extensión de código de Microsoft Edge VS  
:::image-end:::  

:::row:::
   :::column span="1":::
      ### Depurador para Microsoft Edge  

      Con el [depurador para la extensión de código de Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] vs, depura el código de JavaScript front-end línea a línea y muestra las `console.log()` instrucciones directamente desde el [código de Visual Studio][VisualstudioCode].  
      
      Con la herramienta de depuración, puedes iniciar o adjuntar a Microsoft Edge \ (EdgeHTML \) y Microsoft Edge \ (cromo \).  Para obtener un tutorial sobre la depuración de Microsoft Edge desde VS Code y `launch.json` configuraciones de ejemplo, consulta [depurador para Microsoft Edge vs extensión de código][VscodeDebuggerEdge].  Seleccione la imagen siguiente para ver la extensión en acción.  

      :::image type="content" source="./media/debugger-for-edge.png" alt-text="Depurador para la extensión de código perimetral de VS en acción" lightbox="./media/debugger-for-edge.gif":::  
   :::column-end:::
   :::column span="1":::
      ### Elementos de Microsoft Edge  
      
      Con los [elementos de][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] la extensión de código de Microsoft Edge vs, usa la herramienta elementos del explorador Microsoft Edge en Visual Studio.  Al iniciar o adjuntar, la herramienta elementos se conecta a una instancia de Microsoft Edge, muestra la estructura HTML en tiempo de ejecución y le permite modificar el diseño o corregir problemas de estilo.  
      
      Para obtener más información, consulta [elementos de la extensión de código de Microsoft Edge vs][VscodeElementsEdge].  Seleccione la imagen siguiente para ver la extensión en acción.  
      
      :::image type="content" source="./media/elements-for-edge.png" alt-text="Elementos de la extensión de código perimetral de VS en acción" lightbox="./media/elements-for-edge.gif":::  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      ### webhint
      
      Use [webhint][WebhintMain], una herramienta de desplegable personalizable, para mejorar la accesibilidad, el rendimiento, la compatibilidad entre exploradores, la compatibilidad de PWA y la seguridad de su sitio.  Comprueba los procedimientos recomendados y los errores comunes de tu código. El proyecto de código abierto webhint, desarrollado inicialmente por el equipo de Microsoft Edge, ahora forma parte de la [OpenJS Foundation][OpenjsFoundation].  El equipo de Microsoft Edge continúa contribuyendo a la webhint junto con los desarrolladores web de la comunidad.  <!--Select the following image to see the extension in action.  -->  
      
      :::image type="content" source="./media/webhint-extension.png" alt-text="Captura de pantalla de extensión de código webhint VS" lightbox="./media/webhint-extension.png":::  
      
      Identifique y solucione problemas en HTML, CSS, JavaScript, TypeScript y más agregando la [extensión webhint para vs Code][VisualstudioMarketplaceWebhint].  Las sugerencias aparecen como líneas de subrayado y se resumen en el panel **problemas** .  
      
      Para obtener más información, consulta [Cómo usar webhint en Visual Studio Code][VscodeWebhint].  
   :::column-end:::
   :::column span="1":::
      <!--Empty to retain grid  -->  
   :::column-end:::
:::row-end:::

<!-- image links -->  

<!--links -->  

[VscodeDebuggerEdge]: ./debugger-for-edge.md "Depurador para la extensión de código de Microsoft Edge VS | Microsoft docs"  
[VscodeElementsEdge]: ./elements-for-edge.md "Elementos de la extensión de código de Microsoft Edge VS | Microsoft docs"  
[VscodeWebhint]: ./webhint.md "Extensión de código de VS webhint | Microsoft docs"  

[VisualstudioCode]: https://code.visualstudio.com "Código de Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Código de Visual Studio"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Marketplace de Visual Studio"  
[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elementos de Microsoft Edge (cromo) | Marketplace de Visual Studio"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Marketplace de Visual Studio"  

[WebhintMain]:  https://webhint.io "sugerencia"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

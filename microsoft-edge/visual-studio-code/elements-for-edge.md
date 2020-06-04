---
description: Cómo usar los elementos de Microsoft Edge (cromo) del código VS
title: Elementos de Microsoft Edge (cromo) del código VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, elementos
ms.openlocfilehash: ef516d8364c68b550f889bcad0fe762a73ce5f99
ms.sourcegitcommit: 652009c5cea9e75c22b077f0cbcdc0d96bd337ac
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2020
ms.locfileid: "10694865"
---
# Elementos de la extensión de código de Microsoft Edge VS  

Con los [elementos de][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] la extensión de código de Microsoft Edge vs, usa la herramienta elementos del explorador Microsoft Edge en [Visual Studio][VisualstudioCode].  Al iniciar o adjuntar, la herramienta elementos se conecta a una instancia de Microsoft Edge, muestra la estructura HTML en tiempo de ejecución y le permite modificar el diseño o corregir problemas de estilo.  

:::image type="complex" source="./media/elements-for-edge.gif" alt-text="Elementos de la extensión de código perimetral de VS en el trabajo":::
   Elementos de la extensión de código perimetral de VS en el trabajo  
:::image-end:::

<!--![Elements for Edge VS Code extension at work][ImageGifElementsEdge]  -->  

## Iniciar Microsoft Edge desde la extensión de elementos  

Vaya a los elementos de la **barra de actividades**.  Junto a donde dice **los elementos de Microsoft Edge: destinos,** hay un signo más que abre el explorador de la aplicación.  Si seleccionó la opción **acerca de: en blanco** , debe ir a la aplicación web en el explorador para que aparezca en el panel elementos en vs Code.  

## Iniciar Microsoft Edge desde la vista de depuración  

Si está acostumbrado a usar la vista de depuración en Visual Studio Code, obtenga acceso a los elementos de esa herramienta.  Vaya a la vista de depuración \ ( `Ctrl` + `Shift` + `D` en Windows o `Command` + `Shift` + `D` en MacOS \).  

Si no tiene ninguna configuración en VS Code, pulse `F5` en Windows o MacOS o seleccione el botón verde de **reproducción** . Seleccione **borde** en la lista desplegable. Debería ver un `launch.json` archivo con la configuración siguiente.  

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

Ahora que ha cargado la configuración correcta, pulse `F5` en Windows o MacOS o seleccione el botón verde de **reproducción** . La herramienta elementos, que le resulta familiar, desde el explorador Microsoft Edge se inicia en VS Code, lo que le permite acceder a un screencast de su explorador y examinar los componentes de la página.  

## Adjuntar a Microsoft Edge  

Para adjuntar código de VS a una instancia de Microsoft Edge \ (cromo \), debe iniciar el explorador ejecutando el siguiente comando desde el terminal.  

`start msedge --remote-debugging-port=9222`  

Una vez que se inicie la aplicación, agregue la siguiente configuración al archivo **Launch. JSON** :  

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

Seleccione **adjuntar a Microsoft Edge y abra la herramienta elementos** del menú desplegable Debugger.  A continuación, pulse `F5` en Windows o MacOS, o bien seleccione el botón verde de **reproducción** .  Código de VS inicia la herramienta elementos, lo que permite acceder a un screencast del explorador, inspeccionar el DOM y el estilo de los componentes de la página.  

## Ponerse en contacto con los elementos del equipo de extensión de código de Microsoft Edge VS  

Envíe sus comentarios [archivando un problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] con el [repositorio de github][GithubMicrosoftVscodeEdgeDevtools] de la extensión.  

Si deseas mejorar el rendimiento de los elementos de la extensión de código de Microsoft Edge VS, te agradecerás tus contribuciones.  Encuentra todo lo que necesitas para empezar a trabajar en el [repositorio de github][GithubMicrosoftVscodeEdgeDevtools] de la extensión.  

<!-- image links -->  

<!--[ImageGifElementsEdge]: ./media/elements-for-edge.gif "Elements for Edge VS Code extension in action"  -->  
[ImagePngElementsEdge]: elementos./Media/Elements-for-Edge.png para la extensión de código perimetral de VS en la acción "  

<!--links -->  

[VscodeElementsEdge]: ./elements-for-edge.md "Elementos de la extensión de código de Microsoft Edge VS | Microsoft docs"  

[VisualstudioCode]: https://code.visualstudio.com "Código de Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Código de Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-DevTools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Nuevo problema-Microsoft/vscode-Edge-DevTools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elementos de Microsoft Edge (cromo) | Marketplace de Visual Studio"  

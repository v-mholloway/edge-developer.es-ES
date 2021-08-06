---
description: Cómo depurar Microsoft Edge (Chromium) y Microsoft Edge (EdgeHTML) desde Visual Studio Code
title: Depurar Microsoft Edge (Chromium) desde Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, vs code, visual studio code, depurador
ms.openlocfilehash: 24b6912ee99a6c6d0bf961f6e76167bfe8f536184cc460d9ebbe030f5b68a7b4
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11798816"
---
# <a name="debugger-for-microsoft-edge-visual-studio-code-extension"></a>Depurador para Microsoft Edge Visual Studio Code extensión  

Con la [extensión Depurador Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code, depura la línea de código javaScript front-end y consulta instrucciones directamente desde `console.log()` [Visual Studio Code][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Depurador para la extensión Visual Studio Code edge en el trabajo" lightbox="./media/debugger-for-edge.gif":::
   Depurador para la extensión Visual Studio Code edge en el trabajo  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <a name="launching-microsoft-edge"></a>Iniciar Microsoft Edge  

Vaya a la vista Depurar \( `Ctrl` + `Shift` + `D` en Windows o `Command` + `Shift` + `D` en macOS\) en la **barra de actividades**.  Si no tienes ninguna configuración en Visual Studio Code, selecciona en Windows o macOS o selecciona `F5` el botón verde **Reproducir.**  Seleccione **Edge** en el desplegable.  Debería ver un `launch.json` archivo con la siguiente configuración.  

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

Si selecciona en Windows o macOS o vuelve a seleccionar el botón verde Reproducir, Visual Studio Code inicia `F5` Microsoft Edge \(EdgeHTML\) y puede depurar cualquier proyecto web que tenga en ejecución en el puerto directamente desde **** `8080` Visual Studio Code.  

### <a name="microsoft-edge-chromium"></a>Microsoft Edge (Chromium)  

Si desea iniciar Microsoft Edge \(Chromium\), el nuevo Microsoft Edge, en lugar de Microsoft Edge \(EdgeHTML\), simplemente agregue un atributo a la configuración existente con la versión de Microsoft Edge \(Chromium\) que desea iniciar `version` \( `dev` , o `beta` `canary` \).  La siguiente configuración inicia la versión canary de Microsoft Edge \(Chromium\).  

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

## <a name="attaching-to-microsoft-edge"></a>Adjuntar a Microsoft Edge  

Adjuntar Visual Studio Code a Microsoft Edge \(Chromium\).  Desde el terminal, ejecute el siguiente comando.  

```shell
start msedge --remote-debugging-port=9222
```  

Agregue la configuración siguiente al `launch.json` archivo.   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

Si ahora ejecuta esta configuración, Visual Studio Code se Microsoft Edge \(Chromium\) e inicie la depuración.  

## <a name="getting-in-touch-with-the-elements-for-microsoft-edge-visual-studio-code-extension-team"></a>Getting in touch with the Elements for Microsoft Edge Visual Studio Code extension team    

Envíe sus comentarios mediante [la presentación de un problema][GithubMicrosoftVscodeEdgeDebug2NewIssue] en el repositorio GitHub [de][GithubMicrosoftVscodeEdgeDebug2] la extensión.  Incluya el archivo de registro del adaptador de depuración, que se crea para cada ejecución en el `%temp%` directorio con el nombre `vscode-edge-debug2.txt` .  Arrastre este archivo a un comentario de problema para cargarlo en GitHub.  

Para ayudar a mejorar la extensión elements for Microsoft Edge Visual Studio Code, sus contribuciones son bienvenidas.  Encuentre todo lo que necesita para empezar en [GitHub repositorio][GithubMicrosoftVscodeEdgeDebug2] de la extensión.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]: ./media/debugger-for-edge.png "Debugger for Edge Visual Studio Code extension in action"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "microsoft/vscode-edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Nuevo problema: microsoft/vscode-edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  

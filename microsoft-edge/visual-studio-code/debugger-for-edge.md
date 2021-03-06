---
description: Cómo depurar Microsoft Edge (Chromium) y Microsoft Edge (EdgeHTML) desde Visual Studio código
title: Depurar Microsoft Edge (Chromium) desde Visual Studio código
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, vs code, visual studio code, depurador
ms.openlocfilehash: e36348fc1ef5e30a511e6eda73c7646a85d8717e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399298"
---
# <a name="debugger-for-microsoft-edge-visual-studio-code-extension"></a>Depurador para Microsoft Edge Visual Studio de código  

Con la extensión de código Visual Studio depurador de [Microsoft Edge,][VisualstudioMarketplaceDebuggerMicrosoftEdge] depura la línea de código JavaScript front-end y consulta instrucciones directamente desde `console.log()` Visual Studio [Code][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Depurador para la extensión Visual Studio código perimetral en el trabajo" lightbox="./media/debugger-for-edge.gif":::
   Depurador para la extensión Visual Studio código perimetral en el trabajo  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <a name="launching-microsoft-edge"></a>Iniciar Microsoft Edge  

Vaya a la vista Depurar \( `Ctrl` + `Shift` + `D` en Windows o `Command` + `Shift` + `D` en macOS\) en la barra **de actividades**.  Si no tienes ninguna configuración en el código Visual Studio, selecciona en Windows o `F5` macOS o selecciona el botón **verde Reproducir.**  Seleccione **Edge** en el desplegable.  Debería ver un `launch.json` archivo con la siguiente configuración.  

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

Si seleccionas en Windows o macOS o vuelves a seleccionar el botón verde Reproducir, Visual Studio Code inicia `F5` Microsoft Edge \(EdgeHTML\) y puedes depurar cualquier proyecto web que se ejecute en el puerto directamente desde Visual Studio **** `8080` Code.  

### <a name="microsoft-edge-chromium"></a>Microsoft Edge (Chromium)  

Si desea iniciar Microsoft Edge \(Chromium\), el nuevo Microsoft Edge, en lugar de Microsoft Edge \(EdgeHTML\), simplemente agregue un atributo a la configuración existente con la versión de Microsoft Edge \(Chromium\) que desea iniciar `version` \( , , o `dev` `beta` `canary` \).  La siguiente configuración inicia la versión canary de Microsoft Edge \(Chromium\).  

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

Adjuntar Visual Studio código a Microsoft Edge \(Chromium\).  Desde el terminal, ejecute el siguiente comando.  

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

Si ahora ejecuta esta configuración, Visual Studio code se adjunta a Microsoft Edge \(Chromium\) y comienza la depuración.  

## <a name="getting-in-touch-with-the-elements-for-microsoft-edge-visual-studio-code-extension-team"></a>Getting in touch with the Elements for Microsoft Edge Visual Studio Code extension team    

Envíe sus comentarios mediante [la presentación de un problema][GithubMicrosoftVscodeEdgeDebug2NewIssue] en el repositorio de [GitHub][GithubMicrosoftVscodeEdgeDebug2] de la extensión.  Incluya el archivo de registro del adaptador de depuración, que se crea para cada ejecución en el `%temp%` directorio con el nombre `vscode-edge-debug2.txt` .  Arrastre este archivo a un comentario de problema para cargarlo en GitHub.  

Para ayudar a mejorar la extensión elements for Microsoft Edge Visual Studio Code, sus contribuciones son bienvenidas.  Busca todo lo que necesitas para empezar en [github repositorio][GithubMicrosoftVscodeEdgeDebug2] de la extensión.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]: ./media/debugger-for-edge.png "Debugger for Edge Visual Studio Code extension in action"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio código"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Visual Studio código"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "microsoft/vscode-edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Nuevo problema: microsoft/vscode-edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  

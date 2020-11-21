---
description: Cómo depurar Microsoft Edge (cromo) y Microsoft Edge (EdgeHTML) desde código de Visual Studio
title: Depurar Microsoft Edge (cromo) desde el código de Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, depurador
ms.openlocfilehash: df15b76cc26ad01d3b8508362aa4b86998f8b41b
ms.sourcegitcommit: acf8ad7cb6c8ecf83a6170f8eeb9bec32878f8ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182508"
---
# Depurador para la extensión de código de Microsoft Edge Visual Studio  

Con el [depurador de la extensión de código de Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio, depura tu código de JavaScript front-end por línea y consulta las `console.log()` instrucciones directamente desde [Visual Studio Code][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Depurador para la extensión de código de Visual Studio Edge en el trabajo" lightbox="./media/debugger-for-edge.gif":::
   Depurador para la extensión de código de Visual Studio Edge en el trabajo  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## Iniciar Microsoft Edge  

Vaya a la vista de depuración \ ( `Ctrl` + `Shift` + `D` en Windows o `Command` + `Shift` + `D` en MacOS \) en la **barra de actividades**.  Si no tiene ninguna configuración en Visual Studio Code, presione `F5` Windows o MacOS o seleccione el botón verde de **reproducción** .  Seleccione **borde** en la lista desplegable.  Debería ver un `launch.json` archivo con la configuración siguiente.  

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

Si pulsa `F5` en Windows o Mac OS o vuelve a seleccionar el botón verde **reproducir** , Visual Studio Code inicia Microsoft Edge \ (EdgeHTML \) y podrá depurar cualquier proyecto web que se ejecute en el puerto `8080` directamente desde Visual Studio Code.  

### Microsoft Edge (Chromium)  

Si deseas iniciar Microsoft Edge \ (cromo \), el nuevo Microsoft Edge, en lugar de Microsoft Edge \ (EdgeHTML \), simplemente agrega un `version` atributo a la configuración existente con la versión de Microsoft Edge \ (cromo \) que deseas iniciar \ ( `dev` , `beta` o `canary` \).  La siguiente configuración inicia la versión Canarias de Microsoft Edge \ (cromo \).  

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

## Adjuntar a Microsoft Edge  

Adjunte código de Visual Studio a Microsoft Edge \ (cromo \).  Desde el terminal, ejecute el siguiente comando.  

```shell
start msedge --remote-debugging-port=9222
```  

Agregue la configuración que se muestra a continuación al `launch.json` archivo.   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

Si ahora ejecuta esta configuración, Visual Studio Code se conecta a Microsoft Edge \ (cromo \) y comienza a depurar.  

## Ponerse en contacto con los elementos del equipo de extensión de código de Microsoft Edge Visual Studio    

Envíe sus comentarios [archivando un problema][GithubMicrosoftVscodeEdgeDebug2NewIssue] en el [repositorio de github][GithubMicrosoftVscodeEdgeDebug2] de la extensión.  Incluya el archivo de registro del adaptador de depuración, que se crea para cada ejecución en el `%temp%` directorio con el nombre `vscode-edge-debug2.txt` .  Arrastre este archivo a un Comentario de problema para cargarlo en GitHub.  

Para ayudar a que los elementos de la extensión de código Microsoft Edge Visual Studio sean mejores, tus contribuciones son bienvenidos.  Encuentre todo lo que necesita para empezar a trabajar en el [repositorio de github][GithubMicrosoftVscodeEdgeDebug2] de la extensión.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "depurador para la extensión de código perimetral de Visual Studio en acción"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Código de Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Código de Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Nuevo problema-Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Marketplace de Visual Studio"  

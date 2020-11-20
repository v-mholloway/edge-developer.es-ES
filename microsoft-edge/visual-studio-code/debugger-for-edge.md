---
description: Cómo depurar Microsoft Edge (cromo) y Microsoft Edge (EdgeHTML) desde el código de VS
title: Depurar Microsoft Edge (cromo) del código VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, depurador
ms.openlocfilehash: d9f33a17db7083a6a7cbb013dbf9886755f92c5e
ms.sourcegitcommit: 56cb5821d1b8e96f55bfa14a4ce87a3845b009c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182304"
---
# Depurador para la extensión de código de Microsoft Edge VS  

Con el [depurador para la extensión de código de Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] vs, depura el código de JavaScript front-end por línea y consulta las `console.log()` instrucciones directamente desde [Visual Studio Code][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Depurador para la extensión de código perimetral de VS en el trabajo":::
   Depurador para la extensión de código perimetral de VS en el trabajo  
:::image-end:::

<!--![Debugger for Edge VS Code extension at work][ImageGifDebuggerEdge]  -->  

## Iniciar Microsoft Edge  

Vaya a la vista de depuración \ ( `Ctrl` + `Shift` + `D` en Windows o `Command` + `Shift` + `D` en MacOS \) en la **barra de actividades**.  Si no tiene ninguna configuración en VS Code, pulse `F5` en Windows o MacOS o seleccione el botón verde de **reproducción** .  Seleccione **borde** en la lista desplegable.  Debería ver un `launch.json` archivo con la configuración siguiente.  

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

Si pulsa `F5` en Windows o MacOS o selecciona el botón verde **reproducir** , el código de vs inicia Microsoft Edge \ (EdgeHTML \) y podrá depurar cualquier proyecto web que se ejecute en el puerto `8080` directamente desde el código de vs.  

### Microsoft Edge (Chromium)  

Si deseas iniciar Microsoft Edge \ (cromo \), la siguiente versión de Microsoft Edge, en lugar de Microsoft Edge \ (EdgeHTML \), simplemente agrega un `version` atributo a la configuración existente con la versión de Microsoft Edge \ (cromo \) que deseas iniciar \ ( `stable` , `dev` , `beta` o `canary` \). La siguiente configuración inicia la versión Canarias de Microsoft Edge \ (cromo \).  

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

Adjunta código de VS a Microsoft Edge \ (cromo \).  Desde el terminal, ejecute el siguiente comando.  

```console
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

Si ahora ejecuta esta configuración, VS Code se conecta a Microsoft Edge \ (cromo \) y comienza a depurar.  

## Ponerse en contacto con los elementos del equipo de extensión de código de Microsoft Edge VS    

Envíe sus comentarios [archivando un problema][GithubMicrosoftVscodeEdgeDebug2NewIssue] en el [repositorio de github][GithubMicrosoftVscodeEdgeDebug2] de la extensión.  Incluya el archivo de registro del adaptador de depuración, que se crea para cada ejecución en el `%temp%` directorio con el nombre `vscode-edge-debug2.txt` .  Arrastre este archivo a un Comentario de problema para cargarlo en GitHub.  

Para que los elementos de la extensión de código de Microsoft Edge VS sean mejores, tus contribuciones son bienvenidos.  Encuentre todo lo que necesita para empezar a trabajar en el [repositorio de github][GithubMicrosoftVscodeEdgeDebug2] de la extensión.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge VS Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "Debugger for Edge VS extension de código en acción"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Código de Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Código de Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Nuevo problema-Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Marketplace de Visual Studio"  

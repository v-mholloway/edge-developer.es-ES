---
description: Cómo depurar Microsoft Edge (cromo) y Microsoft Edge (EdgeHTML) desde el código de VS
title: Depurar Microsoft Edge (cromo) del código VS
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/10/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, depurador
ms.openlocfilehash: 7d8d2f87500b3e81866b49de32db91c0a525baf2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574871"
---
# Depurador para la extensión de código de Microsoft Edge VS

Con el [depurador de la extensión de código de Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs, puedes depurar la línea de código de JavaScript front-end por línea y ver `console.log()` todas las instrucciones directamente desde [Visual Studio Code](https://code.visualstudio.com/)!

![GIF de la extensión de depurador para Edge VS en el trabajo](./media/debugger-for-edge.gif)

## Iniciar Microsoft Edge

Vaya a la vista de depuración ( `Ctrl`  +  `Shift`  +  `D` en Windows o `Command`  +  `Shift`  +  `D` en Mac) en la **barra de actividades**. Si no tiene ninguna configuración en VS Code, pulse `F5` en Windows o Mac, o haga clic en el botón verde de **reproducción** . Seleccione "borde" en la lista desplegable. Ahora verá un archivo **Launch. JSON** con la siguiente configuración:

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

Si ahora pulsa `F5` en Windows o Mac o vuelve a hacer clic en el botón verde **reproducir** , el código de vs iniciará Microsoft Edge (EdgeHTML) y podrá depurar cualquier proyecto web que se ejecute en el puerto **8080** directamente desde vs Code.

### Microsoft Edge (Chromium)

Si desea iniciar Microsoft Edge (cromo), la siguiente versión de Microsoft Edge, en lugar de Microsoft Edge (EdgeHTML), simplemente agregue un `version` atributo a la configuración existente con la versión de Microsoft Edge (cromo) que desea iniciar ( `dev` , `beta` , o `canary` ). La configuración siguiente iniciará la versión Canarias de Microsoft Edge (cromo):

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

También puedes adjuntar código de VS a Microsoft Edge (cromo). Desde el terminal, ejecute el siguiente comando:

`start msedge --remote-debugging-port=9222`

Agregue la siguiente configuración al archivo **Launch. JSON** :

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```

Si ahora ejecuta esta configuración, el código de VS se adjuntará a Microsoft Edge (cromo) y podrá iniciar la depuración.

## Comentarios

Envíenos sus comentarios [archivando un problema](https://github.com/Microsoft/vscode-edge-debug2/issues/new) en el repositorio de [GitHub](https://github.com/Microsoft/vscode-edge-debug2)de esta extensión. Incluya el archivo de registro del adaptador de depuración, que se crea para cada ejecución en el directorio% Temp% con el nombre `vscode-edge-debug2.txt` . Puede arrastrar este archivo a un Comentario de problema para cargarlo en GitHub.

Si desea ayudarnos a mejorar esta extensión, le damos la bienvenida a sus contribuciones. Puedes encontrar todo lo que necesitas para comenzar a usar [nuestro repositorio de github](https://github.com/Microsoft/vscode-edge-debug2).
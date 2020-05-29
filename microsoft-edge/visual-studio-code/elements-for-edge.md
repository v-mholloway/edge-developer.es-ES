---
description: Cómo usar los elementos de Microsoft Edge (cromo) del código VS
title: Elementos de Microsoft Edge (cromo) del código VS
author: erdraud
ms.author: erdraud
ms.date: 08/08/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, elementos
ms.openlocfilehash: 4875a4665fe1561ecf587a050bbd44e116d9ce5e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574875"
---
# Elementos de la extensión de código de Microsoft Edge VS

Al agregar los [elementos de la extensión de código de Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs, puedes usar la herramienta elementos del explorador desde el [código de Visual Studio](https://code.visualstudio.com/). Al iniciar o adjuntar, la herramienta elementos se conectará a una instancia de Microsoft Edge, mostrará la estructura HTML en tiempo de ejecución y le permitirá modificar el diseño o corregir problemas de estilo.

![GIF de los elementos de la extensión de código perimetral de VS en el trabajo](./media/elements-for-edge.gif)

## Iniciar Microsoft Edge desde la extensión de elementos 

Vaya a los elementos de la **barra de actividades**. Junto a donde dice "elementos de Microsoft Edge: destinos", hay un signo más que abrirá el explorador de la aplicación. Si seleccionó la opción *acerca de: en blanco* , tendrá que desplazarse a su aplicación web en el explorador para que aparezca en el panel elementos en vs Code.

## Iniciar Microsoft Edge desde la vista de depuración

Si está acostumbrado a usar la vista de depuración en Visual Studio Code, puede obtener acceso a los elementos de esa herramienta. Vaya a la vista de depuración ( `Ctrl`  +  `Shift`  +  `D` en Windows o `Command`  +  `Shift`  +  `D` en Mac). 

Si no tiene ninguna configuración en VS Code, pulse `F5` en Windows o Mac, o haga clic en el botón verde de **reproducción** . Seleccione "borde" en la lista desplegable. Ahora verá un archivo **Launch. JSON** con la siguiente configuración:

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

Ahora que ha cargado la configuración correcta, pulse `F5` en Windows o Mac, o haga clic en el botón verde de **reproducción** . La herramienta elementos que ya conoce del explorador Microsoft Edge se iniciará en VS Code, lo que le permitirá acceder a un screencast de su explorador y examinar los componentes de la página.

## Adjuntar a Microsoft Edge
Si desea adjuntar código de VS a una instancia de Microsoft Edge (cromo), debe iniciar el explorador ejecutando el siguiente comando desde su Teminal:

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

Seleccione "adjuntar a Microsoft Edge y abrir la herramienta elementos" en el menú desplegable del depurador. A continuación, presione `F5` en Windows o Mac, o haga clic en el botón verde de **reproducción** . El código de VS inicia la herramienta elementos, lo que permite acceder a un screencast del explorador, inspeccionar el DOM y el estilo de los componentes de la página.

## Comentarios
Envíenos sus comentarios [archivando un problema](https://github.com/microsoft/vscode-edge-devtools/issues/new) en el repositorio de [GitHub](https://github.com/microsoft/vscode-edge-devtools)de esta extensión. 

Si desea ayudarnos a mejorar esta extensión, le damos la bienvenida a sus contribuciones. Puedes encontrar todo lo que necesitas para comenzar a usar [nuestro repositorio de github](https://github.com/microsoft/vscode-edge-devtools).
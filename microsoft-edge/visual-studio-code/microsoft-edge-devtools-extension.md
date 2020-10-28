---
description: Cómo usar los elementos de Microsoft Edge (cromo) del código de Visual Studio
title: Elementos de Microsoft Edge (cromo) del código de Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, código de vs, código de Visual Studio, elementos
ms.openlocfilehash: 81488c08a76a16b80a415cbd17cd0617df916f54
ms.sourcegitcommit: 1cfcf2c8970a6c2221cfbf09a23d36b08bd60690
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/27/2020
ms.locfileid: "11135508"
---
# Extensión de código de Microsoft Edge DevTools para Visual Studio  

Usar <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] -->Esta extensión para acceder a Microsoft Edge DevTools dentro de [Visual Studio Code][VisualstudioCode].  Tiene acceso a los **elementos** y las herramientas de **red** en Microsoft Edge DevTools.  Puede iniciar o adjuntar a una instancia de Microsoft Edge.  Después de la conexión, puede mostrar la estructura HTML en tiempo de ejecución, modificar el diseño, corregir problemas de estilo e inspeccionar el tráfico de red.  

## Herramienta elementos  

De forma predeterminada, la extensión inicia una instancia de explorador en una ventana única y proporciona la funcionalidad de **elementos** de Microsoft Edge DevTools.  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Código de Microsoft Edge DevTools para Visual Studio que se ejecuta en una ventana de explorador completa" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   Código de Microsoft Edge DevTools para Visual Studio que se ejecuta en una ventana de explorador completa  
:::image-end:::  

En la configuración de extensión, puede habilitar más funciones, como la **red**y el **modo sin encabezado** .  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Código de Microsoft Edge DevTools para Visual Studio que se ejecuta en una ventana de explorador completa" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   Habilitar \ (o deshabilitar \) el modo desatendido y la inspección de red en la configuración de la extensión  
:::image-end:::  

## Modo sin periféricos  

En el modo sin encabezado, esta extensión no inicia una instancia de explorador completa para depurar.  Se ejecuta una instancia en segundo plano.  Es posible que tenga que permanecer dentro del editor e interactuar con el explorador integrado.  No se muestra un icono de explorador adicional en la barra de tareas.  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Código de Microsoft Edge DevTools para Visual Studio que se ejecuta en una ventana de explorador completa" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   Código de Microsoft Edge DevTools para Visual Studio ejecutándose con un explorador sin periféricos  
:::image-end:::  

> [!NOTE]
> En macOS, debe activar el modo sin encabezado como modo preferido.  El uso del modo desatendido debería resolver un problema en el que, si la ventana no está visible, la ventana del explorador informa que es `Not Active` .  

## Herramienta red  

Si también desea inspeccionar el tráfico de red de la aplicación, abra la configuración y active la pestaña **red** .  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Código de Microsoft Edge DevTools para Visual Studio que se ejecuta en una ventana de explorador completa" lightbox="./media/edge-devtools-for-vscode-network.png":::
    Inspección de red en Microsoft Edge DevTools para Visual Studio Code  
:::image-end:::  

## Iniciando Microsoft Edge desde la extensión  

Vaya a herramientas de Microsoft Edge en la **barra de actividades**.  Junto a donde dice **herramientas de Microsoft Edge: destinos,** hay un signo más que abre el explorador de la aplicación.  Si elige la opción **acerca de: en blanco** , debe ir a la aplicación web en el explorador para que aparezca en el panel **elementos** en Visual Studio Code.  

## Iniciar Microsoft Edge desde la vista de depuración  

Si estás acostumbrado a usar la vista de depuración en Visual Studio Code, accede a Microsoft Edge DevTools desde ella.  

1.  En Visual Studio Code, navegue a la vista de depuración 
    *   Seleccione `Ctrl` + `Shift` + `D` on Windows/Linux \ ( `Command` + `Shift` + `D` en MacOS \).  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  Si no tienes ninguna configuración en Visual Studio Code, completa una de las siguientes acciones.  
>     *   Seleccione `F5` .  
>     *   Elija el botón **reproducir** \ (verde \).  
> 1.  En la lista desplegable, elija **borde** en la lista desplegable.  
> 1.  `launch.json`Debe mostrarse un archivo que contenga la configuración siguiente.  
>     
>     ```json
>     {
>       "version": "0.2.0",
>       "configurations": [
>         {
>           "name": "Launch Microsoft Edge and open the Edge DevTools",
>           "request": "launch",
>           "type": "vscode-edge-devtools.debug",
>           "url": "http://localhost:8080"
>         }
>       ]
>     }
>     ```  
>     
> Después de cargar la configuración correcta, complete la siguiente acción.  

1.  Para iniciar la herramienta **elementos** desde código de Visual Studio, realice una de las siguientes acciones. 
    *   Seleccione `F5` .  
    *   Elija el botón **reproducir** \ (verde \).  
         
Ahora, puede realizar las siguientes acciones.  

*   Obtener acceso al screencast de su explorador.  
*   Inspeccione el DOM y el estilo de los componentes de la página.  

## Adjuntar a Microsoft Edge  

Siga los pasos que se indican a continuación para abrir un explorador y adjuntar la instancia al código de Visual Studio. 

1.  Para abrir una instancia de Microsoft Edge \ (cromo \), copie y ejecute el siguiente comando.  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  Una vez iniciada la instancia, copie y pegue el siguiente fragmento de código en el `launch.json` archivo.  
    
    ```json
    {
        "type": "vscode-edge-devtools.debug",
        "request": "attach",
        "name": "Attach to Microsoft Edge and open the developer tools",
        "url": "http://localhost:3000/",
        "webRoot": "${workspaceFolder}/out",
        "port": 9222
    }
    ```  
    
1.  En Visual Studio Code, abre el menú desplegable **Debugger** y elige **adjuntar a Microsoft Edge y abrir las herramientas para desarrolladores**.  
1.  Para iniciar la herramienta **elementos** desde código de Visual Studio, realice una de las siguientes acciones. 
    *   Seleccione `F5` .  
    *   Elija el botón **reproducir** \ (verde \).  
         
Ahora, puede realizar las siguientes acciones.  

*   Obtener acceso al screencast de su explorador.  
*   Inspeccione el DOM y el estilo de los componentes de la página.  
    
## Ponerse en contacto con el equipo de extensión de código de Microsoft Edge DevTools para Visual Studio  

Envíe sus comentarios [archivando un problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] con el [repositorio de github][GithubMicrosoftVscodeEdgeDevtools] de la extensión.  

Si desea ayudar a que <!--the Microsoft Edge DevTools for Visual Studio Code -->Esta ampliación mejora, tus contribuciones son bienvenidos.  Encuentra todo lo que necesitas para empezar a trabajar en el [repositorio de github][GithubMicrosoftVscodeEdgeDevtools] de la extensión.  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Código de Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Código de Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-DevTools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Nuevo problema-Microsoft/vscode-Edge-DevTools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para código de VS"  

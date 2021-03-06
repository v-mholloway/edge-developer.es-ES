---
description: Cómo usar elementos para Microsoft Edge (Chromium) desde Visual Studio código
title: Elementos para Microsoft Edge (Chromium) de Visual Studio código
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, vs code, visual studio code, elements
ms.openlocfilehash: 83bac187fa2a9b1766a52f3f2cd176f171846e02
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398458"
---
# <a name="microsoft-edge-devtools-for-visual-studio-code-extension"></a>Microsoft Edge DevTools para la Visual Studio de código  

Usar <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] -->esta extensión para tener acceso en Microsoft Edge DevTools dentro de [Microsoft Visual Studio Code][VisualstudioCode].  Tiene acceso a las herramientas **Elements** y **Network** en Microsoft Edge DevTools.  Puede iniciar o adjuntar a una instancia de Microsoft Edge.  Después de conectarse, puede mostrar la estructura HTML en tiempo de ejecución, modificar el diseño, solucionar problemas de estilo e inspeccionar el tráfico de red.  

## <a name="elements-tool"></a>Herramienta Elementos  

De forma predeterminada, la extensión inicia una instancia del explorador en una ventana única y le proporciona la funcionalidad **Elements** de Microsoft Edge DevTools.  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools para Visual Studio código que se ejecuta con una ventana completa del explorador" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   Microsoft Edge DevTools para Visual Studio código que se ejecuta con una ventana completa del explorador  
:::image-end:::  

En la configuración de extensión, puede habilitar más funciones como **Modo sin cabeza** y **Red**.  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Habilitar (o deshabilitar) el modo sin cabeza y la inspección de red en la configuración de extensión" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   Habilitar el modo sin cabeza \(o deshabilitar\) y la inspección de red en la configuración de extensión  
:::image-end:::  

## <a name="headless-mode"></a>Modo sin cabeza  

En modo sin cabeza, esta extensión no inicia una instancia completa del explorador para depurar.  Ejecuta una instancia en segundo plano.  Es posible que tenga que permanecer dentro del editor e interactuar con el explorador incrustado.  No se muestra un icono de explorador adicional en la barra de tareas.  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools para Visual Studio código que se ejecuta con un headless" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   Microsoft Edge DevTools para Visual Studio código que se ejecuta con un explorador sin cabeza  
:::image-end:::  

> [!NOTE]
> En macOS, debes activar el modo sin cabeza como el modo preferido.  El uso del modo sin cabeza debe resolver un problema en el que, si la ventana no está visible, la ventana del explorador informa de que es `Not Active` .  

## <a name="network-tool"></a>Herramienta Red  

Si también desea inspeccionar el tráfico de red de la aplicación, abra la configuración y active la **pestaña** Red.  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Inspección de red en Microsoft Edge DevTools para Visual Studio código" lightbox="./media/edge-devtools-for-vscode-network.png":::
    Inspección de red en Microsoft Edge DevTools para Visual Studio código  
:::image-end:::  

## <a name="launching-microsoft-edge-from-the-extension"></a>Iniciar Microsoft Edge desde la extensión  

Vaya a Herramientas de Microsoft Edge en la **barra de actividades**.  Junto a donde dice **Herramientas de Microsoft Edge: Destinos,** hay un signo más que abre el explorador de la aplicación.  Si eliges la opción **about:blank,** debes navegar a la aplicación web en el explorador para que aparezca en el **panel** Elementos de Visual Studio Código.  

## <a name="launching-microsoft-edge-from-the-debug-view"></a>Iniciar Microsoft Edge desde la vista Depurar  

Si está acostumbrado a usar la vista Depurar en Visual Studio, acceda a Microsoft Edge DevTools desde ella.  

1.  En Visual Studio, vaya a la vista Depurar 
    *   Seleccione `Ctrl` + `Shift` + `D` en Windows/Linux \( `Command` + `Shift` + `D` en macOS\).  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  Si no tiene ninguna configuración en Visual Studio Code, complete una de las siguientes acciones.  
>     *   Seleccione `F5` .  
>     *   Elija el **botón Reproducir** \(verde\).  
> 1.  En el desplegable, elija **Edge** en el desplegable.  
> 1.  Se `launch.json` debe mostrar un archivo que contenga la siguiente configuración.  
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
> Después de cargar la configuración correcta, realice la siguiente acción.  

1.  Para iniciar la **herramienta Elementos** desde Visual Studio code, realice una de las siguientes acciones. 
    *   Seleccione `F5` .  
    *   Elija el **botón Reproducir** \(verde\).  
         
Ahora, puede realizar las siguientes acciones.  

*   Obtenga acceso a una difusión en pantalla del explorador.  
*   Inspeccione el DOM y el estilo de los componentes de la página.  

## <a name="attaching-to-microsoft-edge"></a>Adjuntar a Microsoft Edge  

Para abrir un explorador y adjuntar la instancia a Visual Studio Code, siga estos pasos. 

1.  Para abrir una instancia de Microsoft Edge \(Chromium\), copie y ejecute el siguiente comando.  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  Después de iniciar la instancia, copie y pegue el siguiente fragmento de código en el `launch.json` archivo.  
    
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
    
1.  En Visual Studio, abra el **** menú desplegable Depurador y elija Adjuntar a **Microsoft Edge y abra las herramientas para desarrolladores.**  
1.  Para iniciar la **herramienta Elementos** desde Visual Studio code, realice una de las siguientes acciones. 
    *   Seleccione `F5` .  
    *   Elija el **botón Reproducir** \(verde\).  
         
Ahora, puede realizar las siguientes acciones.  

*   Obtenga acceso a una difusión en pantalla del explorador.  
*   Inspeccione el DOM y el estilo de los componentes de la página.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-for-visual-studio-code-extension-team"></a>Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team  

Envíe sus comentarios mediante [la presentación de un problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] en el repositorio de [GitHub][GithubMicrosoftVscodeEdgeDevtools] de la extensión.  

Si desea ayudar a hacer <!--the Microsoft Edge DevTools for Visual Studio Code -->esta extensión es mejor, sus contribuciones son bienvenidas.  Encuentre todo lo que necesita para empezar en el repositorio [de GitHub][GithubMicrosoftVscodeEdgeDevtools] de la extensión.  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio código"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentación | Visual Studio código"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Nuevo problema: microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code"  

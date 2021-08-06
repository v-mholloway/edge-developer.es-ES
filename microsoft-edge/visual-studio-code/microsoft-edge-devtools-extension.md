---
description: Cómo usar Microsoft Edge Developer Tools para Visual Studio Code extensión
title: Microsoft Edge Herramientas de desarrollador para Visual Studio Code extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/30/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, vs code, visual studio code, microsoft edge developer tools, microsoft edge developer tools extension
ms.openlocfilehash: 223e13ab943e6c9344c8d72bd08115d93c13254ad70fed07f7b09bf8286e1485
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11805928"
---
# <a name="microsoft-edge-developer-tools-for-visual-studio-code-extension"></a>Microsoft Edge Herramientas de desarrollador para Visual Studio Code extensión  

La Microsoft Edge Developer Tools para Visual Studio Code permite usar la herramienta Elementos y red del explorador desde el editor. Sin salir Visual Studio Code, use Microsoft Edge Developer Tools (DevTools) para conectarse a una instancia de Microsoft Edge con la siguiente funcionalidad.
* Ver la estructura HTML en tiempo de ejecución.
* Cambiar el diseño.
* Cambiar estilos (CSS).
* Leer mensajes de consola.
* Ver solicitudes de red. 

> [!NOTE]
> Esta extensión solo funciona con Microsoft Edge (versiones 80.0.361.48 y posteriores).

Hay dos maneras de abrir Microsoft Edge Developer Tools.
* Desde la barra de actividades de Visual Studio Code.
* Desde el depurador de JavaScript en Visual Studio Code.

En este artículo se describe Microsoft Edge Developer Tools for Visual Studio Code extension. Puede [descargar la extensión][downloadExtension] y [comprobar el código fuente][checkSourceCode].

## <a name="opening-microsoft-edge-developer-tools-with-visual-studio-code"></a>Abrir Microsoft Edge Developer Tools con Visual Studio Code  

Para abrir el panel de herramientas, elija el icono Microsoft Edge herramientas de la barra actividad.

La Microsoft Edge Developer Tools para Visual Studio Code permite iniciar una instancia de Edge o generar un archivo para automatizar el flujo `launch.json` de trabajo de depuración. 

:::image type="complex" source="./media/edge-devtools-for-vscode-extension-icon.png" alt-text="Microsoft Edge DevTools para Visual Studio Code extensión" lightbox="./media/edge-devtools-for-vscode-extension-icon.png":::
   Microsoft Edge DevTools para Visual Studio Code extensión  
:::image-end:::

Al seleccionar **Iniciar instancia,** se abre una ventana del explorador y las herramientas para desarrolladores perimetrales en Visual Studio Code.   

:::image type="complex" source="./media/edge-devtools-for-vscode-launch-instance.png" alt-text="Seleccione Iniciar instancia para abrir el explorador en Visual Studio Code" lightbox="./media/edge-devtools-for-vscode-launch-instance.png":::
   Seleccione Iniciar instancia para abrir el explorador en Visual Studio Code  
:::image-end:::

Use la extensión Developer Tools en VS Code para inspeccionar un elemento HTML en Microsoft Edge. Por ejemplo, seleccione **Success!** En el explorador y observe que la herramienta Elementos se abre con el HTML resaltado. 

:::image type="complex" source="./media/edge-devtools-for-vscode-elements.png" alt-text="Herramienta Elementos abierta con HTML resaltado" lightbox="./media/edge-devtools-for-vscode-elements.png":::
   Herramientas de elementos abiertas con HTML resaltado  
:::image-end:::

## <a name="using-microsoft-edge-developer-tools-in-visual-studio-code"></a>Usar Microsoft Edge Developer Tools en Visual Studio Code  

Puede usar esta extensión en uno de los tres modos:
* Inicie Microsoft Edge en una nueva ventana y vaya a la aplicación web.
* Adjuntar a una instancia en ejecución de Microsoft Edge.
* Abra una nueva instancia de Microsoft Edge dentro de Visual Studio Code. 

Cada modo requiere que se sirva la aplicación web desde un servidor web local, que se inicia desde una Visual Studio Code o desde la línea de comandos. Use el parámetro URL dentro del `launch.json` archivo para Visual Studio Code dirección URL que se va a abrir.

### <a name="open-a-new-browser-instance"></a>Abrir una nueva instancia del explorador

Siga estos pasos para abrir una instancia del explorador desde Visual Studio Code. 

1. En la barra de actividades, **elija Microsoft Edge herramientas para** abrir el panel Microsoft Edge: Destinos.

1. En el panel Herramientas Microsoft Edge: destinos, elija **Iniciar instancia**. Microsoft Edge se abre mostrando una página predeterminada con instrucciones para obtener más información. Además, el panel DevTools se abre en Visual Studio Code.
  
    :::image type="complex" source="./media/edge-devtools-for-vscode-targets-launch.png" alt-text="Microsoft Edge panel DevTools y devTools se abren en Visual Studio Code" lightbox="./media/edge-devtools-for-vscode-targets-launch.png":::
       Microsoft Edge panel DevTools y devTools se abren en Visual Studio Code :::image-end:::

1. En la Microsoft Edge de direcciones, vaya a la dirección URL del proyecto que desea depurar.

### <a name="change-the-default-page-to-your-project-website"></a>Cambiar la página predeterminada al sitio web del proyecto
Para depurar el proyecto, es posible que desee cambiar la página predeterminada que se abre en Microsoft Edge en Visual Studio Code. Para cambiar la página predeterminada al sitio web del proyecto, siga estos pasos. 
1. En Visual Studio Code, elija **Archivo**  >  **Nueva ventana**. Observe que no hay ninguna carpeta abierta. 
1. En la barra de actividades, **elija Microsoft Edge Developer Tools**.
1. En el panel Microsoft Edge: Destinos, elija el vínculo **abrir una** carpeta. 
1. Seleccione la carpeta del proyecto con la nueva página predeterminada que se mostrará al comenzar la depuración en Visual Studio Code.

    La primera vez que abra una carpeta, debe confirmar que confía en los autores de los archivos de esta carpeta. También puede elegir la casilla Confiar en los autores de todos los archivos de la carpeta primaria.

    :::image type="complex" source="./media/edge-devtools-for-vscode-trust.png" alt-text="¿Confía en los autores en los archivos de esta carpeta?" lightbox="./media/edge-devtools-for-vscode-trust.png":::
       ¿Confía en los autores en los archivos de esta carpeta?  
    :::image-end:::

    La primera vez que complete este proceso, también debe seleccionar Microsoft Edge **Developer Tools de** nuevo.

    El panel herramientas Microsoft Edge: destinos ahora muestra dos botones: **Iniciar** instancia y **Generar launch.jsen**.

    :::image type="complex" source="./media/edge-devtools-for-vscode-targets-buttons.png" alt-text="Microsoft Edge Herramientas: el panel Destinos muestra iniciar instancia y generar launch.jsbotones" lightbox="./media/edge-devtools-for-vscode-targets-buttons.png":::
       Microsoft Edge Herramientas: el panel Destinos muestra iniciar instancia y generar launch.jsbotones  
    :::image-end:::

1. Elija **Generar launch.jspara** crear una en el `launch.json` proyecto.
1. En `launch.json` , agregue la dirección URL del proyecto. Si deja la dirección URL vacía, se muestra la página predeterminada. 
1. Guardar `launch.json` .
1. Elija **Iniciar Project** para comprobar que Microsoft Edge se abre y muestra la dirección URL que escribió. Además, DevTools se abre en Visual Studio Code.

## <a name="change-the-extension-settings"></a>Cambiar la configuración de extensión

En la versión 1.1.6 o posterior, puede personalizar DevTools en la Visual Studio Code extensión. Para personalizar la configuración, en el panel Herramientas Microsoft Edge: destinos, elija **...** y, a continuación, elija **Abrir Configuración**.

También puede revisar los cambios realizados en la extensión. Para ver el registro de cambios, en el panel Herramientas Microsoft Edge: Destinos, elija **...** y, a continuación, elija **Ver registro de cambios**.

### <a name="change-to-headless-mode"></a>Cambiar al modo sin cabeza

De forma predeterminada, la extensión Microsoft Edge en una nueva ventana, que muestra otro icono del explorador en la barra de tareas.

Elija **Alternar difusión** en pantalla para mostrar el explorador dentro del editor u ocultar el explorador si ya se muestra. 

:::image type="complex" source="./media/edge-devtools-for-vscode-toggle-screencast.png" alt-text="Alternar la difusión por pantalla para ver el explorador dentro del editor" lightbox="./media/edge-devtools-for-vscode-toggle-screencast.png":::
   Alternar la difusión por pantalla para ver el explorador dentro del editor
:::image-end:::

También puede elegir el **Configuración**sin cabeza para usar solo el explorador de difusión en  >  **** pantalla dentro de Visual Studio Code.

:::image type="complex" source="./media/edge-devtools-for-vscode-settings-headless.png" alt-text="Elija Configuración > Headless para usar solo el explorador de difusión en pantalla dentro de Visual Studio Code" lightbox="./media/edge-devtools-for-vscode-settings-headless.png":::
   Elija Configuración > Headless para usar solo el explorador de difusión en pantalla dentro de Visual Studio Code  
:::image-end:::

## <a name="opening-source-files-from-the-elements-tool"></a>Abrir archivos de origen desde la herramienta Elementos
Una de las características de la herramienta Elements es que muestra el archivo de origen que aplicó estilos y controladores de eventos a un nodo seleccionado en el árbol DOM. Los archivos de origen aparecen en forma de vínculos a una dirección URL. Al seleccionar un vínculo, se abre ese archivo en el editor de Visual Studio Code.

:::image type="complex" source="./media/edge-devtools-for-vscode-elements-files.png" alt-text="Archivos de código abierto de la herramienta Elements" lightbox="./media/edge-devtools-for-vscode-elements-files.png":::
   Archivos de código abierto de la herramienta Elements  
:::image-end:::

## <a name="setting-up-your-project-to-show-live-changes-in-the-extension"></a>Configurar el proyecto para mostrar cambios en directo en la extensión
De forma predeterminada, la extensión no realiza un seguimiento de los cambios en directo en el código mientras escribe. Si desea que el explorador se actualice automáticamente al cambiar un archivo, configure un entorno de recarga activa. Esto requiere [Node.js][NodeJS] y [NPM][NPM] en el equipo.
En el siguiente ejemplo se muestra una carpeta de archivos de producción en el disco duro llamado `my-project` . Cambie los nombres de archivo y las ubicaciones según sea necesario para su entorno.

1. Instale Node.js y el paquete NPM de recarga.
    1. Descargar e instalar [Node.js][NodeJS].
    1. Para instalar el [volver a cargar el paquete NPM][NPM], abra un símbolo del sistema y ejecute `npm install reload -g` para instalar el paquete globalmente.
1. Adjunte la extensión al proyecto de recarga en directo.
    1. Vaya a la `my-project` carpeta de la ventana de terminal y ejecute para iniciar el servidor `reload` local.
    1. En Visual Studio Code, abra la `my-project` carpeta.
    1. Vaya a la extensión e inicie una Microsoft Edge del explorador.
    1. En Microsoft Edge, navegue por la extensión a `localhost:8080/{file name you want to open}` .
    1. Todos los cambios guardados en esta carpeta ahora desencadenan una actualización del explorador.

## <a name="browser-debugging-with-microsoft-edge-developer-tools-integration-in-visual-studio-code"></a>Depuración del explorador con la Microsoft Edge Developer Tools en Visual Studio Code
La depuración de JavaScript ahora está integrada en Visual Studio Code. A partir de la versión 1.5.7 de Visual Studio Code, puedes depurar en Chrome, Microsoft Edge o Node.js sin instalar ninguna otra extensión. Si depura con Microsoft Edge, puede iniciar Microsoft Edge Developer Tools con el depurador de JavaScript.
1. Para iniciar una sesión, use cualquiera de los siguientes métodos:
    * Elija **F5**o en la barra de menús elija el **icono Depurar** y elija Ejecutar y **depurar**.
    * Abra la Visual Studio Code de comandos y elija **Depurar: Abrir vínculo**.

    :::image type="complex" source="./media/edge-devtools-for-vscode-start-session.png" alt-text="Iniciar Microsoft Edge Developer Tools con el depurador de JavaScript" lightbox="./media/edge-devtools-for-vscode-start-session.png":::
       Iniciar Microsoft Edge Developer Tools con el depurador de JavaScript  
    :::image-end:::

1. Elija **Edge**.
    En la barra de herramientas de depuración, observe el nuevo botón Inspeccionar 

    :::image type="complex" source="./media/edge-devtools-for-vscode-inspect-button.png" alt-text="Botón Inspeccionar que se muestra ahora en la barra de herramientas de depuración" lightbox="./media/edge-devtools-for-vscode-inspect-button.png":::
       Botón Inspeccionar que se muestra ahora en la barra de herramientas de depuración :::image-end:::

1. Elija **Inspeccionar** para abrir Microsoft Edge Developer Tools dentro de Visual Studio Code.
    La primera vez que elija **Inspeccionar**, el editor le pedirá que instale [Microsoft Edge Developer Tools for Visual Studio Code extension][ https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools ].

    Una vez completada la instalación, cuando elija **Inspeccionar,** se abrirá Microsoft Edge Developer Tools dentro de Visual Studio Code.

    :::image type="complex" source="./media/edge-devtools-for-vscode-tools-inside.png" alt-text="Se abre el botón Inspeccionar Microsoft Edge Herramientas de desarrollador dentro de Visual Studio Code" lightbox="./media/edge-devtools-for-vscode-tools-inside.png":::
       Se abre el botón Inspeccionar Microsoft Edge Herramientas de desarrollador dentro de Visual Studio Code :::image-end:::

    Ahora puede inspeccionar el DOM, cambiar CSS y ver solicitudes de red de su proyecto ejecutándose en el explorador sin dejar Visual Studio Code.
    
    También puede usar la Consola de depuración en el editor para interactuar con el documento en el explorador. Tiene acceso completo al objeto window y puede usar la [API de utilidades de consola][ConsoleUtilitiesAPI].

    :::image type="complex" source="./media/edge-devtools-for-vscode-debug-console.png" alt-text="La consola de depuración en el editor interactúa con el documento abierto en el explorador" lightbox="./media/edge-devtools-for-vscode-debug-console.png":::
       La consola de depuración en el editor interactúa con el documento abierto en el explorador  
    :::image-end:::

1. Para adjuntar automáticamente a Microsoft Edge e iniciar Developer Tools en Visual Studio Code, cree un `launch.json` archivo. Para obtener más información, vaya a [Iniciar configuraciones | Depuración en Visual Studio Code][launchJSON].

    Si copia el código siguiente, asegúrese de cambiar y `http://localhost:8080` asegúrese de que la variable se `{workspaceFolder}` resuelve. Si no ha instalado esta extensión, si elige el icono, se abre la pestaña VS Code extensiones y se muestra automáticamente la extensión que se va a instalar.

    Para usar esta opción, seleccione Microsoft Edge como tipo de depuración. En el `launch.json` archivo, especifique `pwa-msedge` como tipo:

    ```JSON
    {
        "version": "0.2.0",
        "configurations": [
            {
                "type": "pwa-msedge",
                "request": "launch",
                "name": "Launch Edge",
                "url": "http://localhost:8080",
                "webRoot": "${workspaceFolder}"
            }
        ]
    }
    
## Console integration
If you launch the extension from the Run and Debug workflow, the [Debug Console of Visual Studio Code][DebugConsoleVSCode] gives you all the functions of the [Microsoft Edge Developer Tools Console][EdgeDevToolsConsole]. You have direct access to the Window object of the instance of Edge and can use all the [Console Utilities][ConsoleUtilities].

:::image type="complex" source="./media/edge-devtools-for-vscode-console-integration.png" alt-text="Microsoft Edge Developer Tools Console available when extension launched from Run and Debug workflow" lightbox="./media/edge-devtools-for-vscode-console-integration.png":::
   Microsoft Edge Developer Tools Console available when extension launched from Run and Debug workflow  
:::image-end:::

## Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team  

Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] on the [microsoft/vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.  

If you want to help make <!--the Microsoft Edge DevTools for Visual Studio Code -->this extension better, your contributions are welcome.  Find everything you need to get started in the [microsoft/vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension. 

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "New Issue - microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code"  

[ConsoleUtilitiesAPI]: /microsoft-edge/devtools-guide-chromium/console/utilities "Console Utilities API reference | Microsoft Docs"

[downloadExtension]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for VS Code | Visual Studio Marketplace"

[checkSourceCode]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | github"

[launchJSON]: https://code.visualstudio.com/Docs/editor/debugging#_launch-configurations "Launch Configurations | Debugging in Visual Studio Code"

[DebugConsoleVSCode]: https://code.visualstudio.com/Docs/editor/debugging "Debugging in Visual Studio Code"

[EdgeDevToolsConsole]: /microsoft-edge/devtools-guide-chromium/console/ "Use the Console | Microsoft Docs"

[ConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Console Utilities API reference | Microsoft Docs"

[NodeJS]: https://www.nodejs.org "Node.js"

[NPM]: https://www.npmjs.com/package/reload?activeTab=readme "reload - npm"

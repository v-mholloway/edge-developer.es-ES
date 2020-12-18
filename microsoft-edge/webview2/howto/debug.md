---
description: Más información sobre cómo depurar controles WebView2.
title: Introducción a la depuración de aplicaciones de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 4f94fe880f66f8aeb387d2db4a8bfaab20699466
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230701"
---
# Introducción a la depuración de aplicaciones de WebView2  

El objetivo del control Microsoft Edge WebView2 es combinar lo mejor de las características y herramientas de desarrollo de aplicaciones nativas y Web.  Al desarrollar su aplicación de WebView2, debe depurar la aplicación.  En este artículo se describen las distintas herramientas que se usan para depurar el código web y nativo de la aplicación WebView2.  

## [Microsoft Edge DevTools](#tab/devtools)  

Use [las herramientas de desarrollador de Microsoft Edge (cromo)][DevtoolsGuideChromiumMain] para depurar contenido web que se muestra en controles WebView2, de la misma manera que puede depurar para otra página web que se muestra en Microsoft Edge.  Para abrir la DevTools, establezca el foco en el control WebView y, a continuación, use una de las siguientes acciones.  

*   Seleccione `F12` .  
*   Seleccione `Ctrl` + `Shift` + `I` .  
*   Abra el menú contextual \ (haga clic con el botón derecho \) y elija `Inspect` .  
    
Para obtener más información, consulte [información general de DevTools][DevtoolsGuideChromiumMain].  

:::image type="complex" source="./media/f12.png" alt-text="Depuración DevTools" lightbox="./media/f12.png":::
   Depuración DevTools  
:::image-end:::  

## [Visual Studio](#tab/visualstudio)  

Visual Studio proporciona varias herramientas de depuración para el código nativo y Web en aplicaciones de WebView2.  En la sección de Visual Studio, el foco principal es la depuración de controles de WebView, pero los otros métodos de depuración en Visual Studio están disponibles de la forma habitual.  Use el siguiente proceso para depurar código nativo y web solo en aplicaciones Win32 o complementos de Office.  

> [!IMPORTANT]
> Cuando depure la aplicación en Visual Studio con el depurador nativo adjunto, seleccionar `F12` puede desencadenar el depurador nativo en lugar de las herramientas de desarrollo.  Seleccione `Ctrl` + `Shift` + `I` o use el menú contextual \ (haga clic con el botón derecho \) para evitar la situación.  

Antes de empezar, asegúrese de que se cumplan los siguientes requisitos.  

*   Para depurar scripts, la aplicación debe iniciarse desde Visual Studio.  
*   No puede adjuntar un depurador a un proceso de WebView2 en ejecución.  
*   Instale Visual Studio 2019 versión 16,4 Preview 2 o posterior.  
    
Instale y configure las herramientas de depurador de scripts en Visual Studio.  

1.  Complete las acciones siguientes para instalar el componente de **diagnóstico de JavaScript** en el **desarrollo de escritorio con C++**.  
    
    1.  En la barra del explorador de Windows, escriba `Visual Studio Installer` .  
    1.  Elija **instalador de Visual Studio** para abrirlo.  
    1.  En el instalador de Visual Studio, en la versión instalada, haga clic en el botón **más** y, a continuación, elija **modificar**.  
    1.  En Visual Studio, en **cargas de trabajo**, elija la opción **desarrollo de escritorio en C++** .  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Pantalla modificando cargas de trabajo de Visual Studio" lightbox="./media/workloads.png":::
            Pantalla modificando cargas de trabajo de Visual Studio
        :::image-end:::  
        
    1.  Elija **componentes individuales**.  
    1.  En el cuadro de búsqueda, escriba `JavaScript diagnostics` .  
    1.  Elija la configuración de **diagnóstico de JavaScript** .  
    1.  Elija **modificar**. 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Ficha modificar componentes individuales de Visual Studio" lightbox="./media/indivcomp.png":::
           Ficha modificar componentes individuales de Visual Studio  
        :::image-end:::  
        
1.  Habilite la depuración de scripts para aplicaciones de WebView2.  
    1.  En el proyecto WebView2, abra el menú contextual \ (haga clic con el botón derecho \) y elija **propiedades**.  
    1.  En las **propiedades de configuración**, elija **depuración**.  
    1.  En el **tipo de depuración**, elija **JavaScript (WebView2)**.  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Propiedad de configuración de depuración de Visual Studio" lightbox="./media/enbjs.png":::
           Propiedad de configuración de **depuración** de Visual Studio  
        :::image-end:::  
        
Complete las acciones siguientes para depurar su aplicación de WebView2.  

1.  Para establecer un punto de interrupción en el código fuente, coloque el puntero a la izquierda del número de línea y elija establecer un punto de interrupción.  El adaptador de depuración JS/TS no realiza asignaciones de ruta de origen.  Debe abrir exactamente la misma ruta asociada con su WebView2.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Agregar punto de interrupción en Visual Studio" lightbox="./media/breakpoint.png"::: 
       Agregar punto de interrupción en Visual Studio  
    :::image-end:::  
    
1.  Para ejecutar el depurador, elija el tamaño de bit de la plataforma y, a continuación, elija el botón verde reproducir junto al **depurador local de Windows**.  La aplicación se ejecuta y el depurador se conecta al primer proceso WebView2 que se crea.  
    
    :::image type="complex" source="./media/run.png" alt-text=" Depurador local de Windows de Visual Studio" lightbox="./media/run.png"::: 
       **Depurador local de Windows** de Visual Studio  
    :::image-end:::  
    
1.  En la **consola de depuración**, busque la salida del depurador.  
    
    :::image type="complex" source="./media/console.png" alt-text=" Consola de depuración de Visual Studio" lightbox="./media/console.png"::: 
       Consola de **depuración** de Visual Studio  
    :::image-end:::  
    
## [Visual Studio Code](#tab/visualstudiocode)  

Use código de Microsoft Visual Studio para depurar scripts que se ejecutan en controles WebView2.  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

En Visual Studio Code, completa las siguientes acciones para depurar el código. 

1.  Es necesario que el proyecto tenga un `launch.json` archivo.  Si el proyecto no tiene un `launch.json` archivo, copie el siguiente fragmento de código y cree un `launch.json` archivo nuevo.  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",
        "env": {
            // Customize for your application location if needed
            "Path": "%path%;e:/path/to/your/application/location; "
        },
        "useWebView": true,
    ```  
    
1.  Para establecer un punto de interrupción en el código fuente, desplace el puntero sobre la línea y seleccione `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="El punto de interrupción se establece en código de Visual Studio" lightbox="./media/breakpointvs.png":::
       El punto de interrupción se establece en código de Visual Studio  
    :::image-end:::
    
    > [!NOTE]
    > Dado que el código de Visual Studio no realiza la asignación de origen, asegúrate de establecer puntos de interrupción en el mismo archivo que use WebView2.  Si las rutas no coinciden, el código de Visual Studio no detiene el código en ejecución en el punto de interrupción.  
    
1.  Ejecute el código.  
    1.  En la pestaña **Ejecutar** , elija la configuración de inicio en el menú desplegable.  
    1.  Para iniciar la depuración de la aplicación, elija iniciar depuración, que es el triángulo verde junto a la lista desplegable iniciar configuración.  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Pestaña ejecución de código de Visual Studio" lightbox="./media/runvs.png":::
           Pestaña ejecución de código de Visual Studio  
        :::image-end:::  
        
1.  Abra la **consola de depuración** para ver los errores y resultados de la depuración.  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Consola de depuración de código de Visual Studio" lightbox="./media/resultsvs.png":::
       Consola de depuración de código de Visual Studio  
    :::image-end:::  
    
**Configuración avanzada**:  

*   Depuración de WebView dirigida. 
    
    En algunas aplicaciones WebView2, puedes usar más de un control de WebView2. Para seleccionar el control WebView2 para depurar en esta situación, puede usar la depuración de WebView2 de destino 
    
    Abra `launch.json` y complete las siguientes acciones para usar la depuración de WebView dirigida.  
    
    1.  Confirme que el `useWebview` parámetro está establecido en `true` .  
    1.  Agregue el `urlFilter` parámetro.  Cuando el control WebView2 navega a una dirección URL, el `urlFilter` valor del parámetro se usa para comparar cadenas que aparecen en la dirección URL.  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    Al depurar la aplicación, es posible que tenga que recorrer el código desde el principio del proceso de representación. Si está representando páginas web en sitios y no tiene acceso al código fuente, puede usar la `?=value`  opción, porque las páginas web omiten los parámetros no reconocidos.   
    
    > [!IMPORTANT]
    > Después de que se encuentre la primera coincidencia en la dirección URL, el depurador se detendrá.  No se pueden depurar dos controles de WebView2 al mismo tiempo porque el puerto CDP está compartido por todos los controles de WebView2 y usa un único número de puerto.  
    
*   Depurar procesos en ejecución  
    
    Es posible que necesite adjuntar el depurador para ejecutar procesos de WebView2. Para hacerlo, en `launch.json` , actualice el `request` parámetro a `attach` .
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    El control WebView2 debe abrir el puerto CDP para permitir la depuración del control WebView2.  Para asegurarte de que solo un control de WebView2 tiene abierto un puerto de protocolo de desarrollador de cromo (CDP) antes de iniciar el depurador, debes compilar el código.  
    
*   Depurar opciones de seguimiento  
    
    Agregue el `trace` parámetro a launch.jsactivado para habilitar el seguimiento de depuración.  
    
    1.  Agregar `trace` parámetro.  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Guarde el resultado de depuración en un archivo de registro." lightbox="./media/tracelog.png":::
                 Guardar el resultado de la depuración en un archivo de registro  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Resultado detallado" lightbox="./media/verbose.png":::
                 Salida de depuración de código de Visual Studio con seguimiento detallado activado  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   Depure complementos de Office.
    
    Si depura complementos de Office, abra el código fuente del complemento en una instancia independiente de código de Visual Studio.  Abra launch.jsen la aplicación WebView2 y agregue el siguiente fragmento de código para adjuntar el depurador al complemento de Office.
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   Solución de problemas del depurador  
    
    Puede encontrarse con los siguientes escenarios al utilizar el depurador.  
    
    *   El depurador no se detiene en el punto de interrupción y tiene un resultado de depuración.  Para solucionar el problema, confirme que el archivo con el punto de interrupción es el mismo archivo utilizado por el control WebView2.  El depurador no realiza la asignación de la ruta de origen.  
    *   No puede adjuntar a un proceso en ejecución y recibe un error de tiempo de espera.  Para solucionar el problema, confirme que el control WebView2 abrió el puerto CDP.  Asegúrese de  `additionalBrowserArguments`  que su valor en el registro es correcto o de que las opciones son correctas.  Para obtener más información, consulte [additionalBrowserArguments para dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] y [additionalBrowserArguments para Win32][Webview2ReferenceWin32Webview2IdlParameters].  
    
* * *  

## Consulte también  

*   Para comenzar a usar WebView2, consulte [WebView2 guías de introducción][Webview2MainGettingStarted].  
*   Para obtener un ejemplo completo de las capacidades de WebView2, consulta el repositorio de [WebView2Samples][GithubMicrosoftedgeWebview2samples] en github.
*   Para obtener información más detallada sobre las API de WebView2, consulta referencia de la [API][Webview2ApiReference].
*   Para obtener más información sobre WebView2, consulte [recursos WebView2][Webview2MainNextSteps].
    
## Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "Propiedad CoreWebView2EnvironmentOptions. AdditionalBrowserArguments (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment-Globals | Microsoft docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Referencia de la API de Microsoft Edge WebView2 | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "¿Qué novedades hay? -Depurador de JavaScript para Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicaciones de WebView de Microsoft Edge (cromo): depurador de código de Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  

---
description: Obtenga información sobre cómo depurar controles WebView2.
title: Introducción a la depuración de aplicaciones webView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral
ms.openlocfilehash: 01cd67897f7041bca0cedcee2cc3242f3ebcc962
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536180"
---
# <a name="get-started-debugging-webview2-apps"></a>Introducción a la depuración de aplicaciones webView2  

El objetivo del control WebView2 de Microsoft Edge es combinar lo mejor de las características y herramientas de desarrollo de aplicaciones nativas y web.  Al desarrollar la aplicación WebView2, debes depurar la aplicación.  En este artículo se describen las distintas herramientas que se deben usar para depurar el código web y nativo de la aplicación WebView2.  

## [<a name="microsoft-edge-devtools"></a>Microsoft Edge DevTools](#tab/devtools)  

Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] para depurar el contenido web que se muestra en los controles WebView2, del mismo modo que puede depurar para otra página web mostrada en Microsoft Edge.  Para abrir DevTools, establezca el foco en el control WebView y, a continuación, use una de las siguientes acciones.  

*   Seleccione `F12` .  
*   Seleccione `Ctrl` + `Shift` + `I` .  
*   Abra el menú contextual \(hacer clic con el botón secundario\) y elija `Inspect` .  
    
Para obtener más información, vaya [a DevTools overview][DevtoolsGuideChromiumMain].  

:::image type="complex" source="./media/f12.png" alt-text="Depuración de DevTools" lightbox="./media/f12.png":::
   Depuración de DevTools  
:::image-end:::    

## [<a name="visual-studio"></a>Visual Studio](#tab/visualstudio)  

Visual Studio proporciona varias herramientas de depuración para código web y nativo en aplicaciones webView2.  En la Visual Studio, el foco principal es la depuración de controles WebView, pero los demás métodos de depuración de Visual Studio están disponibles como de costumbre.  Use el siguiente proceso para depurar código web y nativo solo en aplicaciones de Win32 o complementos de Office.  

> [!IMPORTANT]
> Al depurar la aplicación en Visual Studio con el depurador nativo adjunto, seleccionar puede desencadenar el depurador nativo `F12` en lugar de Herramientas de desarrollador.  Seleccione `Ctrl` + `Shift` + `I` o use el menú contextual \(hacer clic con el botón secundario\) para evitar la situación.  

Antes de comenzar, asegúrese de que se cumplen los siguientes requisitos.  

*   Para depurar scripts, la aplicación debe iniciarse desde dentro de Visual Studio.  
*   No puede adjuntar un depurador a un proceso webView2 en ejecución.  
*   Instale Visual Studio versión 16.4 preview 2 o posterior de 2019.  
    
Instale y configure las herramientas del depurador de scripts en Visual Studio.  

1.  Complete las siguientes acciones para instalar el componente **de diagnóstico de JavaScript** en **el desarrollo de escritorio con C++**.  
    1.  En la barra del Explorador de Windows, escriba `Visual Studio Installer` .  
    1.  Elija **Visual Studio installer para** abrirlo.  
    1.  En el instalador Visual Studio, en la versión instalada, elija el botón **Más** y, a continuación, **elija Modificar**.  
    1.  En Visual Studio, en **Cargas de trabajo,** elija la configuración **Desarrollo de escritorio en C++.**  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Visual Studio pantalla Modificar cargas de trabajo" lightbox="./media/workloads.png":::
            Visual Studio pantalla Modificar cargas de trabajo
        :::image-end:::  
        
    1.  Elija **Componentes individuales**.  
    1.  En el cuadro de búsqueda, escriba `JavaScript diagnostics` .  
    1.  Elija la configuración **de diagnóstico de JavaScript.**  
    1.  Elija **Modificar**. 
        
        :::image type="complex" source="./media/indiv-comp.png" alt-text="Visual Studio modificar componentes individuales ficha" lightbox="./media/indiv-comp.png":::
           Visual Studio modificar componentes individuales ficha  
        :::image-end:::  
        
1.  Habilitar la depuración de scripts para aplicaciones webView2.  
    1.  En el proyecto WebView2, abra el menú contextual \(haga clic con el botón secundario\) y elija **Propiedades**.  
    1.  En Propiedades **de configuración,** elija **Depuración**.  
    1.  En Tipo **de depurador,** elija **JavaScript (WebView2).**  
        
        :::image type="complex" source="./media/enb-js.png" alt-text="Visual Studio de depuración de propiedades de configuración" lightbox="./media/enb-js.png":::
           Visual Studio de **depuración de** propiedades de configuración  
        :::image-end:::  
        
Complete las siguientes acciones para depurar la aplicación WebView2.  

1.  Para establecer un punto de interrupción en el código fuente, mantenga el mouse a la izquierda del número de línea y elija establecer un punto de interrupción.  El adaptador de depuración JS/TS no realiza la asignación de ruta de acceso de origen.  Debe abrir exactamente la misma ruta de acceso asociada a su WebView2.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio agregar punto de interrupción" lightbox="./media/breakpoint.png"::: 
       Visual Studio agregar punto de interrupción  
    :::image-end:::  
    
1.  Para ejecutar el depurador, elija el tamaño de bits de la plataforma y, a continuación, elija el botón de reproducción verde junto a **Depurador local de Windows**.  La aplicación se ejecuta y el depurador se conecta al primer proceso de WebView2 que se crea.  
    
    :::image type="complex" source="./media/run.png" alt-text=" Visual Studio depurador local de Windows" lightbox="./media/run.png"::: 
       Visual Studio depurador **local de Windows**  
    :::image-end:::  
    
1.  En la **Consola de depuración,** busque el resultado del depurador.  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio de depuración" lightbox="./media/console.png"::: 
       Visual Studio de **depuración**  
    :::image-end:::  
    
## [<a name="visual-studio-code"></a>Visual Studio Code](#tab/visualstudiocode)  

Use Microsoft Visual Studio Code para depurar scripts que se ejecutan en controles WebView2.  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

En Visual Studio code, realice las siguientes acciones para depurar el código. 

1.  Es necesario que el proyecto tenga un `launch.json` archivo.  Si el proyecto no tiene un archivo, copie el siguiente fragmento de código `launch.json` y cree un nuevo `launch.json` archivo.  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",
        "env": {
            // Customize for your app location if needed
            "Path": "%path%;e:/path/to/your/app/location; "
        },
        "useWebView": true,
        // The following two lines setup source path mapping, where `url` is the start page of your app, and `webRoot` is the top level directory with all your code files.
        "url": "file:///${workspaceFolder}/path/to/your/toplevel/foo.html",
        "webRoot": "${workspaceFolder}/path/to/your/assets"
    ```  
    
    > [!NOTE]
    > Visual Studio asignación de ruta de origen de código ahora requiere la dirección URL, por lo que la aplicación ahora recibe un parámetro de línea de comandos cuando se inicia.  Puede omitir el parámetro `url` de forma segura si es necesario.  
    
1.  Para establecer un punto de interrupción en el código fuente, mantenga el mouse en la línea y seleccione `F9`
    
    :::image type="complex" source="./media/breakpoint-vs.png" alt-text="El punto de interrupción se establece en Visual Studio código" lightbox="./media/breakpoint-vs.png":::
       El punto de interrupción se establece en Visual Studio código  
    :::image-end:::
    
1.  Ejecute el código.  
    1.  En la **pestaña Ejecutar,** elija la configuración de inicio en el menú desplegable.  
    1.  Para empezar a depurar la aplicación, elija Iniciar depuración, que es el triángulo verde junto a la lista desplegable de configuración de inicio.  
        
        :::image type="complex" source="./media/run-vs.png" alt-text=" Visual Studio ejecutar código" lightbox="./media/run-vs.png":::
           Visual Studio ejecutar código  
        :::image-end:::  
        
1.  Abra **la Consola de depuración** para ver el resultado de depuración y los errores.  
    
    :::image type="complex" source="./media/results-vs.png" alt-text=" Visual Studio de depuración de código" lightbox="./media/results-vs.png":::
       Visual Studio de depuración de código  
    :::image-end:::  
    
**Configuración avanzada**:  

*   Depuración de vista web dirigida. 
    
    En algunas aplicaciones webView2, puede usar más de un control WebView2. Para elegir el control WebView2 para depurar en esta situación, puede usar la depuración de webview2 dirigida 
    
    Abra y complete las siguientes acciones para usar la depuración `launch.json` de Webview dirigida.  
    
    1.  Confirme que el `useWebview` parámetro está establecido en `true` .  
    1.  Agregue el `urlFilter` parámetro.  Cuando el control WebView2 navega a una dirección URL, el valor del parámetro se usa para comparar las cadenas que `urlFilter` aparecen en la dirección URL.  
        
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    Al depurar la aplicación, es posible que deba pasar por el código desde el principio del proceso de representación. Si está representando páginas web en sitios y no tiene acceso al código fuente, puede usar la opción, ya que las páginas web omiten parámetros no `?=value`  reconocidos.   
    
    > [!IMPORTANT]
    > Después de encontrar la primera coincidencia en la dirección URL, el depurador se detiene.  No puede depurar dos controles WebView2 al mismo tiempo porque todos los controles WebView2 comparten el puerto CDP y usan un único número de puerto.  
    
*   Depurar procesos en ejecución  
    
    Es posible que deba adjuntar el depurador a los procesos de WebView2 en ejecución. Para ello, en `launch.json` , actualice el parámetro a `request` `attach` .
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    El control WebView2 debe abrir el puerto CDP para permitir la depuración del control WebView2.  El código debe crearse para asegurarse de que solo un control WebView2 tiene abierto un puerto de Protocolo para desarrolladores de Chrome (CDP), antes de iniciar el depurador.  
    
*   Opciones de seguimiento de depuración  
    
    Agregue el `trace` parámetro para launch.jspara habilitar el seguimiento de depuración.  
    
    1.  Parámetro `trace` Add.  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/trace-log.png" alt-text=" Guarde el resultado de depuración en un archivo de registro." lightbox="./media/trace-log.png":::
                 Guardar resultados de depuración en un archivo de registro  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Salida detallada" lightbox="./media/verbose.png":::
                 Visual Studio salida de depuración de código con seguimiento detallado activado  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   Depurar complementos de Office.  
    
    Si va a depurar complementos de Office, abra el código fuente del complemento en una instancia independiente de Visual Studio Code.  Abra launch.jsen la aplicación WebView2 y agregue el siguiente fragmento de código para adjuntar el depurador al complemento de Office.
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   Solución de problemas del depurador  
    
    Es posible que encuentre los siguientes escenarios al usar el depurador.  
    
    *   El depurador no se detiene en el punto de interrupción y tiene resultados de depuración.  Para solucionar el problema, confirme que el archivo con el punto de interrupción es el mismo archivo que usa el control WebView2.  El depurador no realiza la asignación de ruta de acceso de origen.  
    *   No se puede adjuntar a un proceso en ejecución y se produce un error de tiempo de espera.  Para solucionar el problema, confirme que el control WebView2 abrió el puerto CDP.  Asegúrese de  `additionalBrowserArguments`  que el valor del Registro es correcto o de que las opciones son correctas.  Para obtener más información, vaya a [additionalBrowserArguments para dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] y [additionalBrowserArguments para Win32][Webview2ReferenceWin32Webview2IdlParameters].  
        
* * *  

## <a name="see-also"></a>Consulte también  

*   Para empezar a usar WebView2, vaya a [WebView2 Get Started Guides][Webview2MainGetStarted].  
*   Para obtener un ejemplo completo de las capacidades de WebView2, vaya al repositorio [WebView2Samples][GithubMicrosoftedgeWebview2samples] en GitHub.
*   Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][Webview2ApiReference].
*   Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2MainNextSteps].
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Getting in touch with the Microsoft Edge WebView team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "Propiedad CoreWebView2EnvironmentOptions.AdditionalBrowserArguments (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment: global | Microsoft Docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Referencia de api de Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webview2MainGetStarted]: ../index.md#get-started "Introducción: introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

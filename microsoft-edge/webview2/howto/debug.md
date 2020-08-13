---
description: Más información sobre cómo depurar controles WebView2.
title: Depurar WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 6b2cc65e5cb368c29efec2eb3638f0c1772000d9
ms.sourcegitcommit: 4bc904c5d54347185f275bd76441975be471c320
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/12/2020
ms.locfileid: "10926480"
---
# Cómo depurar con WebView2  

El objetivo del control Microsoft Edge WebView2 es combinar lo mejor de las características de desarrollo de aplicaciones nativas y Web y las herramientas de desarrollador.  En la siguiente página se describen las distintas herramientas que se deben usar al desarrollar con controles WebView2.  

## Microsoft Edge DevTools  

Use [las herramientas de desarrollador de Microsoft Edge (cromo)][DevtoolsGuideChromiumMain] para depurar contenido web que se muestra en los controles de WebView2, de la misma manera que usa Microsoft Edge.  Para abrir la DevTools, establezca el foco en la ventana WebView y, a continuación, use cualquiera de las siguientes acciones.  
*   Seleccione `F12` .  
*   Seleccione `Ctrl` + `Shift` + `I` .  
*   Abra el menú contextual \ (haga clic con el botón derecho \) > seleccione `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   Microsoft Edge DevTools  
:::image-end:::  

> [!NOTE]
> Cuando depure la aplicación en Visual Studio con el depurador nativo adjunto, presionar `F12` podría desencadenar el depurador nativo en lugar de las herramientas de desarrollo.  Presione `Ctrl` + `Shift` + `I` o use el menú contextual \ (haga clic con el botón derecho \) para evitar la situación.  

> [!NOTE]
> Puede usar el `--auto-open-devtools-for-tabs` argumento de la línea de comandos para abrir una nueva ventana de DevTools al crear por primera vez una vista en WebView.  <!--See `CreateCoreWebView2Controller` documentation for how to provide additional command-line arguments to the browser process.  See `LoaderOverride` registry key to examine different builds of WebView2 without modifying your application in the `CreateCoreWebView2Controller` documentation.  -->  

## Visual Studio  

Use el depurador de scripts en Visual Studio 2019 versión 16,4 Preview 2 o una versión posterior para depurar el script en Visual Studio.  Compruebe que el componente **diagnóstico de JavaScript** en **desarrollo de escritorio con** la carga de trabajo de C++ está instalado.  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Diagnósticos de JavaScript de Visual Studio":::
   Diagnósticos de JavaScript de Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Para habilitar la depuración de scripts WebView2, abra el menú contextual \ (haga clic con el botón derecho \) en el proyecto > seleccione **propiedades**.  

*   En **propiedades de configuración**, seleccione **depuración**.  
*   En la propiedad **tipo de depurador** , seleccione **JavaScript (WebView2)** en la lista de opciones. 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Depurador de JavaScript de Visual Studio":::
   Depurador de JavaScript de Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Ya está todo configurado y listo para depurar.  

Para depurar, complete las siguientes acciones.  

1.  Establecer puntos de interrupción  
    *   Abra el archivo de script y establezca el punto de interrupción en el lugar que desee.  
        
        > [!NOTE]
        > El adaptador de depuración JS/TS no realiza la asignación de ruta de origen.Debe abrir exactamente la misma ruta asociada con su WebView2.  
        
1.  Ejecutar código  
    *   Seleccione el tipo de compilación y el entorno de tiempo de ejecución que corresponda y, a continuación, inicie el depurador local de Windows.  
1.  Ver consola de depuración  
    *   La aplicación se ejecuta y el depurador se conecta después de que se crea el primer webview2.Se muestra el resultado pendiente de depuración.  
        
        > [!NOTE]
        > Este método de depuración está actualmente restringido a las aplicaciones Win32 y los complementos de Office.  
        
## Visual Studio Code  

Puede usar código de Visual Studio para depurar scripts que se ejecutan en controles WebView2.  Para obtener más información, consulte [aplicaciones de WebView de Microsoft Edge (cromo)][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].  

<!--todo:  add See also heading  -->  

## Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!--## Debugging  

Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`. You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView. See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process. Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.  -->  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicaciones de WebView de Microsoft Edge (cromo)-VS depurador de código para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  

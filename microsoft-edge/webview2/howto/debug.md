---
description: Más información sobre cómo depurar controles WebView2.
title: Depurar WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 232104abc360cfa660d567ffb66535213fcb3ae0
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888589"
---
# Cómo depurar con WebView2  

El objetivo del control Microsoft Edge WebView2 es combinar lo mejor de las características de desarrollo de aplicaciones nativas y Web y las herramientas de desarrollador.  En la siguiente página se describen las distintas herramientas que se deben usar al desarrollar con controles WebView2.  

## Microsoft Edge DevTools  

Use [las herramientas de desarrollador de Microsoft Edge (cromo)][DevtoolsMain] para depurar contenido web que se muestra en controles WebView2, de la misma manera que si estuviera usando Microsoft Edge.  Para abrir la DevTools, establezca el foco en la ventana WebView y, a continuación, use cualquiera de las siguientes acciones.  

*   Seleccione `F12` .  
*   Seleccione `Ctrl` + `Shift` + `I` .  
*   Abra el menú contextual \ (haga clic con el botón derecho \) y seleccione `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   Microsoft Edge DevTools  
:::image-end:::  

> [!IMPORTANT]
> Cuando depure la aplicación en Visual Studio con el depurador nativo adjunto, seleccionar `F12` puede desencadenar el depurador nativo en lugar de las herramientas de desarrollo.  Use `Ctrl` + `Shift` + `I` o use el menú contextual \ (haga clic con el botón derecho \) para evitar la situación.  

## Visual Studio  

Puede usar Visual Studio para desarrollar el código de la aplicación y las secuencias de comandos de depuración al mismo tiempo.  

Ten en cuenta lo siguiente.  

*   Visual Studio solo admite scripts de depuración cuando la aplicación se inicia desde Visual Studio.  \ (No se admite adjuntar un proceso en ejecución para la depuración. \)  
*   El escenario de depuración de WebView objetivo no es compatible.  

Use el depurador de scripts en Visual Studio 2019 versión 16,4 Preview 2 o una versión posterior para depurar el script en Visual Studio.  

Configurar el depurador.  

*   Compruebe que el componente **diagnóstico de JavaScript** en **desarrollo de escritorio con** la carga de trabajo de C++ está instalado.  
    
    1.  Vaya a la configuración de **aplicaciones & características** en Windows.  Búsquelo con la barra de tareas de Windows.  
    1.  Elija **modificar**.  
    1.  Compruebe que están seleccionadas las casillas de verificación **diagnósticos de JavaScript** y **desarrollo de escritorio de C++** .  
        
        :::image type="complex" source="../media/appsandfeatures.png" alt-text="Aplicaciones y características" lightbox="../media/appsandfeatures.png":::
           Aplicaciones y características  
        :::image-end:::  
        
*   Habilite la depuración de script WebView2.  
    1.  Mantenga el puntero sobre el proyecto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **propiedades**.  
    1.  En **propiedades de configuración**, seleccione **depuración**.  
    1.  En la propiedad **tipo de depurador** , busque en la lista de opciones y seleccione **JavaScript (WebView2)**.  
        
        :::image type="complex" source="../media/enbjs.png" alt-text="Depurador de JavaScript de Visual Studio" lightbox="../media/enbjs.png":::
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

Puede usar código de Visual Studio para depurar scripts que se ejecutan en controles WebView2.  Para obtener más información, consulte [aplicaciones de WebView de Microsoft Edge (cromo)][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].  

<!--todo:  add See also heading  -->  

## Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge  

Ayuda a crear una experiencia WebView2 más rica compartiendo tus comentarios.  Visita el [repositorio de comentarios][GithubMicrosoftedgeWebviewfeedback] para enviar solicitudes de características o informes de errores.  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicaciones de WebView de Microsoft Edge (cromo)-VS depurador de código para Microsoft Edge | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

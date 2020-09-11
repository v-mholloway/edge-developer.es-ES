---
description: Más información sobre cómo depurar controles WebView2.
title: Introducción a la depuración de aplicaciones de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/13/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 15171147b847b1d41cd603efed1b8ee42185dc29
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010701"
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

Visual Studio proporciona varias herramientas de depuración para el código nativo y Web en aplicaciones de WebView2.  En la sección de Visual Studio, el foco principalmente es la depuración de controles de WebView, pero los otros métodos de depuración en Visual Studio están disponibles de la forma habitual.  Use el siguiente proceso para depurar código nativo y web solo en aplicaciones Win32 o complementos de Office.  

> [!IMPORTANT]
> Cuando depure la aplicación en Visual Studio con el depurador nativo adjunto, seleccionar `F12` puede desencadenar el depurador nativo en lugar de las herramientas de desarrollo.  Seleccione `Ctrl` + `Shift` + `I` o use el menú contextual \ (haga clic con el botón derecho \) para evitar la situación.  

Antes de empezar, asegúrese de que se cumplan los siguientes requisitos.  

*   Para depurar scripts, la aplicación debe iniciarse desde Visual Studio.  
*   No puede adjuntar un depurador a un proceso de WebView2 en ejecución.  
*   Instale Visual Studio 2019 versión 16,4 Preview 2 o posterior.  

Instale y configure las herramientas de depurador de scripts en Visual Studio.  

1.  Complete las acciones siguientes para instalar el componente de **diagnóstico de JavaScript** en el **desarrollo de escritorio con C++**.  

    1. En la barra del explorador de Windows, escriba `Visual Studio Installer` .  
    1. Elija **instalador de Visual Studio** para abrirlo.  
    1. En el instalador de Visual Studio, en la versión instalada, haga clic en el botón **más** y, a continuación, elija **modificar**.  
    1. En Visual Studio, en **cargas de trabajo**, elija la opción **desarrollo de escritorio en C++** .  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Pantalla modificando cargas de trabajo de Visual Studio" lightbox="./media/workloads.png":::
            Pantalla modificando cargas de trabajo de Visual Studio :::image-end:::  
        
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
    
* * *  

## Consulte también  

*   Para comenzar a usar WebView2, consulte [WebView2 guías de introducción][Webview2MainGettingStarted].  
*   Para obtener un ejemplo completo de las capacidades de WebView2, consulta el repositorio de [WebView2Samples][GithubMicrosoftedgeWebview2samples] en github.
*   Para obtener información más detallada sobre las API de WebView2, consulta referencia de la [API][Webview2ApiReference].
*   Para obtener más información sobre WebView2, consulte [recursos WebView2][Webview2MainNextSteps].

## Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions clase | Microsoft docs"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-Globals | Microsoft docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Referencia de la API de Microsoft Edge WebView2 | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "¿Qué novedades hay? -Depurador de JavaScript para Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicaciones de WebView de Microsoft Edge (cromo): depurador de código de Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  

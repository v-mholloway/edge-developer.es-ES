---
description: Obtenga información sobre cómo vincular estáticamente la biblioteca del cargador de WebView2.
title: Cómo vincular estáticamente la biblioteca del cargador de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/15/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 880e9ed809dc268ee0b30b6ee3b5996711f54300
ms.sourcegitcommit: 0ded671914aae231493f418dd7645a04361dca1b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "11120127"
---
# Vincular estáticamente la biblioteca del cargador de WebView2  

Es posible que desee distribuir su aplicación con un único archivo ejecutable, en lugar de un paquete de muchos archivos. Para crear un único archivo ejecutable o reducir el tamaño del paquete, debe vincular estáticamente los archivos de WebView2Loader. El SDK de WebView2 contiene un archivo de encabezado, `WebView2Loader.dll` y el `IDL` archivo. `WebView2Loader.dll` es un pequeño componente que ayuda a que las aplicaciones encuentren el tiempo de ejecución de WebView2 o los canales no estables de Microsoft Edge en el dispositivo.  

Para las aplicaciones que no deseen enviar un `WebView2Loader.dll` , complete los siguientes pasos.  

1.  Abra el `.vcxproj` archivo de proyecto de la aplicación en un editor de texto, como código de Visual Studio.  
    
    > [!NOTE]
    > El `.vcproj` archivo de proyecto puede ser un archivo oculto, lo que significa que no se muestra en Visual Studio.  Use la línea de comandos para buscar archivos ocultos.  
    
1.  Busca la sección en el código en la que incluyes los archivos de destino del paquete NuGet de WebView2.  La ubicación en el código se resalta en la siguiente ilustración.  

    :::image type="complex" source="./media/inserthere.png" alt-text="Fragmentos de código de archivos de proyecto" lightbox="./media/inserthere.png":::
       Fragmentos de código de archivos de proyecto   
    :::image-end:::  
  
1.  Copie el siguiente fragmento de código y péguelo donde `Microsoft.Web.WebView2.targets` esté incluido.  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Fragmentos de código de archivos de proyecto" lightbox="./media/staticlib.png":::
       Fragmento de código insertado  
    :::image-end:::  
    
1.  Edite las dependencias adicionales de la configuración de compilación de la aplicación.  Para empezar, busque todas las `<AdditionalDependencies>` etiquetas. Para cada uno, agregue `version.lib` como una dependencia adicional a cada configuración de compilación distinta del `.vcxproj` archivo.  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Fragmentos de código de archivos de proyecto" lightbox="./media/versionlib.png":::
       Agregar `version.lib` a `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > El equipo WebView2 tiene como objetivo automatizar la adición de la dependencia adicional en versiones futuras.  
    
1. Compila y ejecuta la aplicación.

### Ponerse en contacto con el equipo de WebView2  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### Consulte también  

*   Para comenzar a usar WebView2, vaya a [WebView2 guías de introducción][Webview2MainGettingStarted].  
*   Para obtener un ejemplo completo de las capacidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samples] en github.
*   Para obtener información más detallada sobre las API de WebView2, vaya a referencia de la [API][Webview2ApiReference].
*   Para obtener más información sobre WebView2, vaya a [recursos WebView2][Webview2MainNextSteps].

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Referencia de la API de Microsoft Edge WebView2 | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "¿Qué novedades hay? -Depurador de JavaScript para Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicaciones de WebView de Microsoft Edge (cromo): depurador de código de Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  

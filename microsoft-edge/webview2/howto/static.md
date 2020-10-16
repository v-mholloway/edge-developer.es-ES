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
ms.openlocfilehash: a25bd85c8a6b17bdf8712c954eb7b7cc28738eb2
ms.sourcegitcommit: 442de63da52d00c6dc27fa08ccdb736534127566
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "11120077"
---
# Cómo vincular estáticamente la biblioteca del cargador de WebView2  

## Contexto  

¿Qué es el WebView2Loader.dll?  

*   El SDK de WebView2 contiene un archivo de encabezado, `WebView2Loader.dll.` y el `IDL` archivo. `WebView2Loader.dll` es un pequeño componente que ayuda a que las aplicaciones encuentren el tiempo de ejecución de WebView2 (o canales de Microsoft Edge no estables) en el dispositivo.  

Para las aplicaciones que tienen un único tiempo de ejecución y no desean enviar un `WebView2Loader.dll` , complete los siguientes pasos de **procedimiento** .  

## Procedimiento  

1.  Abra el `.vcxproj` archivo de proyecto de la aplicación en un editor de texto, como código de Visual Studio.  
    
    > [!NOTE]
    > El `.vcproj` archivo de proyecto puede ser un archivo oculto, lo que significa que no se muestra en Visual Studio.  Use la línea de comandos para buscar un archivo oculto.  
    
1.  Busca la sección en el código en la que incluyes los archivos de destino del paquete NuGet de WebView2.  La ubicación en el código se resalta en la siguiente ilustración.  
    
    :::image type="complex" source="./media/inserthere.png" alt-text="Fragmentos de código de archivos de proyecto" lightbox="./media/inserthere.png"::: 
       Fragmentos de código de archivos de proyecto  
    :::image-end:::  
    
1.  Copie el siguiente fragmento de código y péguelo donde `Microsoft.Web.WebView2.targets` esté incluido.  

    > [!NOTE]
    > Por ejemplo, lo incluye después del bloque de código siguiente.  
    > 
    > ```csharp
    > <Import Project="..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets" Condition="Exists('..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets')" />
    > ```  
    
    ```csharp
    <PropertyGroup> <WebView2LoaderPreference>Static</WebView2LoaderPreference> </PropertyGroup>
    ```
    
    :::image type="complex" source="./media/staticlib.png" alt-text="Fragmentos de código de archivos de proyecto" lightbox="./media/staticlib.png"::: 
       Fragmento de código insertado  
    :::image-end:::  
    
1.  Edite las dependencias adicionales de la configuración de compilación de la aplicación.  Para empezar, busque todas las `<AdditionalDependencies>` etiquetas.  
1.  Agregue `version.lib` como una dependencia adicional a cada configuración de compilación distinta en el `.vcxproj` archivo de la aplicación.  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Fragmentos de código de archivos de proyecto" lightbox="./media/versionlib.png"::: 
       Agregar `version.lib` a `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > El equipo de WebView2 se propone automatizar el paso de dependencia adicional en futuras versiones.  
    
Compile e implemente la aplicación.  Intentos.  

## Consulte también  

*   Para comenzar a usar WebView2, vaya a [WebView2 guías de introducción][Webview2MainGettingStarted].  
*   Para obtener un ejemplo completo de las capacidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samples] en github.
*   Para obtener información más detallada sobre las API de WebView2, vaya a referencia de la [API][Webview2ApiReference].
*   Para obtener más información sobre WebView2, vaya a [recursos WebView2][Webview2MainNextSteps].

## Ponerse en contacto con el equipo de WebView2  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Referencia de la API de Microsoft Edge WebView2 | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "¿Qué novedades hay? -Depurador de JavaScript para Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicaciones de WebView de Microsoft Edge (cromo): depurador de código de Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  

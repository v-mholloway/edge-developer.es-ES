---
description: Obtenga información sobre cómo vincular estáticamente la biblioteca de cargadores de WebView2.
title: Cómo vincular estáticamente la biblioteca de cargadores de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral
ms.openlocfilehash: 91a09823a60fbe60e9eb23d938e8a173366dbf98
ms.sourcegitcommit: 66a8e3db5b63b0532ca2f4003fa37bde6bd225b0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2021
ms.locfileid: "11934089"
---
# <a name="statically-link-the-webview2-loader-library"></a>Vincular estáticamente la biblioteca de cargadores de WebView2  

Es posible que desee distribuir la aplicación con un único archivo ejecutable, en lugar de un paquete de muchos archivos. Para crear un único archivo ejecutable o reducir el tamaño del paquete, debe vincular estáticamente los archivos WebView2Loader. El SDK de WebView2 contiene un archivo de encabezado `WebView2Loader.dll` y el `IDL` archivo. `WebView2Loader.dll` es un componente pequeño que ayuda a las aplicaciones a localizar webView2 Runtime o Microsoft Edge de vista previa en el dispositivo.  

Para las aplicaciones que no desean enviar un `WebView2Loader.dll` , siga estos pasos.  

1.  Abra el `.vcxproj` archivo de proyecto de la aplicación en un editor de texto, como Visual Studio Code.  
    
    > [!NOTE]
    > El `.vcproj` archivo de proyecto puede ser un archivo oculto, lo que significa que no se muestra en Visual Studio.  Use la línea de comandos para buscar archivos ocultos.  
    
1.  Busque la sección en el código donde se incluyen los archivos de destino de NuGet webView2.  La ubicación del código se resalta en la siguiente figura.  
    
    :::image type="complex" source="./media/insert-here.png" alt-text="Project Fragmento de código de archivos" lightbox="./media/insert-here.png":::
       Project Fragmento de código de archivos   
    :::image-end:::  
    
1.  Copie el siguiente fragmento de código y péguelo donde `Microsoft.Web.WebView2.targets` esté incluido.  
    
    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```  
    
    :::image type="complex" source="./media/static-lib.png" alt-text="Fragmento de código insertado" lightbox="./media/static-lib.png":::
       Fragmento de código insertado  
    :::image-end:::  
    
1.  Edite las dependencias adicionales de la configuración de compilación para la aplicación.  Para empezar, busque todas las `<AdditionalDependencies>` etiquetas. Para cada uno, agregue `version.lib` como dependencia adicional a cada configuración de compilación diferente en el `.vcxproj` archivo.  
    
    :::image type="complex" source="./media/version-lib.png" alt-text="Adición de version.lib a ItemDefinitionGroups" lightbox="./media/version-lib.png":::
       Agregar `version.lib` a `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > El equipo de WebView2 tiene como objetivo automatizar la adición de la dependencia adicional en futuras versiones.  
    
1.  Compila y ejecuta la aplicación.  
    
## <a name="getting-in-touch-with-the-webview2-team"></a>Getting in touch with the WebView2 team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

## <a name="see-also"></a>Consulta también  

*   Para empezar a usar WebView2, vaya a [WebView2 Introducción Guías][Webview2MainGetStarted].  
*   Para obtener un ejemplo completo de las funcionalidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samples] en GitHub.
*   Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][Webview2ApiReference].
*   Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2MainNextSteps].
    
<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2 API Reference | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2MainGetStarted]: ../index.md#get-started "Introducción: introducción a Microsoft Edge WebView2 | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "¿Cuáles son las novedades? - Depurador de JavaScript para Visual Studio Code: microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge webview (Chromium) - Visual Studio Code - Depurador para Microsoft Edge - microsoft/vscode-edge-debug2 | GitHub"  

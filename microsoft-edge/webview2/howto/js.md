---
description: Obtenga información sobre cómo usar JavaScript en escenarios complejos en aplicaciones webView2
title: Usar JavaScript en aplicaciones webView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral
ms.openlocfilehash: da04d1e24b95dfa7ea477bbd228fd46b64727ec3
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536740"
---
# <a name="use-javascript-in-webview-for-extended-scenarios"></a>Usar JavaScript en WebView para escenarios extendidos  

El uso de JavaScript en controles WebView2 te permite personalizar aplicaciones nativas para satisfacer tus requisitos.  En este artículo se explora cómo usar JavaScript en WebView2 y se analiza cómo desarrollar mediante funciones y características avanzadas de WebView2.  

## <a name="before-you-begin"></a>Antes de comenzar  

En este artículo se supone que ya tiene un proyecto en funcionamiento.  Si no tiene un proyecto y desea seguirlo, vaya a la Guía de introducción a [WebView2][Webview2GettingstartedWpf].  

## <a name="basic-webview2-functions"></a>Funciones básicas de WebView2  

Usa las siguientes funciones para empezar a insertar JavaScript en la aplicación WebView.  

| API  | Descripción  |
|:--- |:--- |  
| [ExecuteScriptAsync][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | Ejecute JavaScript en un control WebView. Para obtener más información, vaya al tutorial Introducción. |
| [OnDocumentCreatedAsync][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | Se ejecuta cuando se crea el modelo de objetos de documento \(DOM\). |
      
## <a name="scenario--running-a-dedicated-script-file"></a>Escenario: ejecución de un archivo de script dedicado  

En esta sección, acceda a un archivo JavaScript dedicado desde el control WebView2.  

> [!NOTE]
> Aunque escribir JavaScript en línea puede ser eficaz para comandos rápidos de JavaScript, se pierden los temas de color de JavaScript y el formato de línea que dificulta la escritura de grandes secciones de código en Visual Studio.  

Para solucionar el problema, cree un archivo JavaScript independiente con el código y, a continuación, pase una referencia a ese archivo mediante los `ExecuteScriptAsync` parámetros.  

1.  Cree un archivo en el proyecto y agregue el código `.js` JavaScript que desea ejecutar.  Por ejemplo, cree un archivo denominado `script.js` .  
1.  Convertir el archivo JavaScript en una cadena que se pasa a `ExecuteScriptAsync` .  
    1.  Para convertir el archivo JavaScript en una cadena, copie el siguiente fragmento de código.  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  Pegue el código en `MainWindow.xaml.cs` .  
1.  Pase la variable de texto mediante `ExecuteScriptAsync` .  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## <a name="scenario--remove-drag-and-drop-functionality"></a>Escenario: quitar la funcionalidad de arrastrar y colocar  

En esta sección, use JavaScript para quitar la funcionalidad de arrastrar y colocar del control WebView2.  

Para empezar, explore la funcionalidad actual de arrastrar y colocar.  

1.  Cree un `.txt` archivo para arrastrar y colocar.  Por ejemplo, cree un archivo denominado `contoso.txt` y agréle texto.  
1.  Ejecute el proyecto.  
1.  Arrastre y coloque el archivo `contoso.txt` en el control WebView.  Se abre una nueva ventana, que es el resultado del código del proyecto de ejemplo.  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Resultado de arrastrar y colocar contoso.txt" lightbox="./media/dragtext.png":::
       Resultado de arrastrar y colocar contoso.txt  
    :::image-end:::  

Ahora, agregue código para quitar la funcionalidad de arrastrar y colocar del control WebView2.  

1.  Copie y pegue el siguiente fragmento de código `InitializeAsync()` en `MainWindow.xaml.cs` .   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  Ejecute el proyecto.  
1.  Intente arrastrar y colocar `contoso.txt` .  Confirme que no puede arrastrar y colocar.  

## <a name="scenario--removing-the-context-menu"></a>Escenario: quitar el menú contextual  

En esta sección, quite el menú contextual predeterminado del control WebView2.  

Para empezar, explore la funcionalidad del menú contextual actual.  

1.  Ejecute el proyecto.  
1.  Mantenga el mouse en cualquier lugar del control WebView2 y abra el menú contextual \(hacer clic con el botón secundario\).  El menú contextual muestra las opciones predeterminadas.  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Menú contextual que muestra las opciones predeterminadas" lightbox="./media/contextmenu.png":::
       Menú contextual que muestra las opciones predeterminadas  
    :::image-end:::  
    
Ahora agregue código para quitar la funcionalidad del menú contextual del control WebView2.  

1.  Copie y pegue el siguiente fragmento de código `InitializeAsync()` en `MainWindow.xaml.cs` .    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  Vuelva a ejecutar el código.  Confirme que no puede abrir un menú contextual \(hacer clic con el botón secundario\).  
   
## <a name="see-also"></a>Consulta también  

*   Para obtener más información sobre cómo empezar a usar WebView2, vaya a [WebView2 Getting Started Guides][Webview2MainGettingStarted].  
*   Para obtener un ejemplo completo de las funcionalidades de WebView2, vaya al repositorio [WebView2Samples][GithubMicrosoftedgeWebview2samples] en GitHub.  
*   Para obtener información detallada sobre las API de WebView2, vaya a [Referencia de api][Webview2ApiReference].  
*   Para obtener más información sobre WebView2, vaya a [Recursos de WebView2][Webview2MainNextSteps].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Getting in touch with the Microsoft Edge WebView team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  


[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2 API Reference | Microsoft Docs"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Introducción a WebView2 en WPF (versión preliminar) | Microsoft Docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated - 0.9.579 - interfaz ICoreWebView2 | Microsoft Docs"  
[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

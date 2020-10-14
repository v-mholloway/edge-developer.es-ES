---
description: Más información sobre cómo usar JavaScript en escenarios complejos en aplicaciones de WebView2
title: Usar JavaScript en aplicaciones de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/12/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 5312cf6209e81a1bbcfa33f324e9b8e7ef099cec
ms.sourcegitcommit: aec8d3482465dfb9a4f5f61c5eded1ff6f66d71d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "11117714"
---
# Usar JavaScript en vista previa para escenarios extendidos  

El uso de JavaScript en WebView2 permite personalizar aplicaciones nativas para satisfacer sus necesidades.  En este artículo se explica cómo usar JavaScript en WebView2 y se revisa cómo desarrollar con las características y funcionalidades avanzadas de WebView2.  

## Antes de comenzar  

En este artículo se da por supuesto que ya tiene un proyecto en curso.  Si no tiene un proyecto y quiere seguirlo, vaya a la [Guía de introducción de WebView2][Webview2GettingstartedWpf].  

## Funciones de WebView2 básicas  

Use las siguientes funciones para empezar a incrustar JavaScript en la aplicación WebView.  

| API  | Descripción  |
|:--- |:--- |  
| [ExecuteScriptAsync][Webview2ReferenceWpf09515MicrosoftWebExecutescriptasync] | Ejecutar JavaScript en un control WebView. Para obtener más información, vaya al tutorial Introducción. |
| [OnDocumentCreatedAsync][Webview2ReferenceWin3209538Icorewebview2Addscripttoexecuteondocumentcreated] | Se ejecuta cuando se crea el modelo de objetos de documento \ (DOM \). |
      
## Escenario: ejecutar un archivo de script dedicado  

En esta sección, accede a un archivo de JavaScript dedicado desde el control WebView2.  

> [!NOTE]
> Aunque escribir JavaScript en línea puede ser eficaz para los comandos rápidos de JavaScript, pierde los temas de color y el formato de las líneas de JavaScript que dificulta escribir grandes secciones de código en Visual Studio.  

Para resolver el problema, cree un archivo JavaScript independiente con el código y, a continuación, pase una referencia a ese archivo usando los `ExecuteScriptAsync` parámetros.  

1.  Cree un `.js` archivo en el proyecto y agregue el código JavaScript que desea ejecutar.  Por ejemplo, cree un archivo denominado `script.js` .  
1.  Convierte el archivo JavaScript en una cadena que se pasa a `ExecuteScriptAsync` .  
    1.  Para convertir el archivo de JavaScript en una cadena, copie el siguiente fragmento de código.  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  Pega el código en `MainWindow.xaml.cs` .  
1.  Pase la variable de texto con `ExecuteScriptAsync` .  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## Escenario: quitar la funcionalidad de arrastrar y colocar  

En esta sección, use JavaScript para quitar la funcionalidad de arrastrar y colocar de su control WebView2.  

Para empezar, explore la funcionalidad actual de arrastrar y colocar.  

1.  Cree un `.txt` archivo para arrastrar y colocar.  Por ejemplo, cree un archivo con el nombre `contoso.txt` y agréguele texto.  
1.  Ejecute el proyecto.  
1.  Arrastre el archivo y colóquelo `contoso.txt` en el control WebView.  Se abrirá una nueva ventana, que es el resultado del código de su proyecto de ejemplo.  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Resultado de arrastrar y soltar contoso.txt" lightbox="./media/dragtext.png":::
       Resultado de arrastrar y soltar contoso.txt  
    :::image-end:::  

Ahora, agregue código para quitar la funcionalidad de arrastrar y colocar del control WebView2.  

1.  Copie y pegue el siguiente fragmento de código en `InitializeAsync()` en `MainWindow.xaml.cs` .   
            
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

## Escenario: quitar el menú contextual  

En esta sección, quite el menú contextual predeterminado del control WebView2.  

Para empezar, explore la funcionalidad actual del menú contextual.  

1.  Ejecute el proyecto.  
1.  Mantenga el mouse en cualquier lugar del control WebView2 y abra el menú contextual \ (haga clic con el botón derecho \).  El menú contextual muestra las opciones predeterminadas.  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Resultado de arrastrar y soltar contoso.txt" lightbox="./media/contextmenu.png":::
       Menú contextual que muestra las opciones predeterminadas  
    :::image-end:::  
    
Ahora agregue código para quitar la funcionalidad de menú contextual del control WebView2.  

1.  Copie y pegue el siguiente fragmento de código en `InitializeAsync()` en `MainWindow.xaml.cs` .    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  Vuelva a ejecutar el código.  Confirme que no puede abrir un menú contextual \ (haga clic con el botón derecho \).  
   
## Consulte también  

*   Para obtener más información sobre cómo comenzar a usar WebView2, vaya a [WebView2 guías de introducción][Webview2MainGettingStarted].  
*   Para obtener un ejemplo completo de las capacidades de WebView2, navegue hasta el repositorio de [WebView2Samples][GithubMicrosoftedgeWebview2samples] en github.  
*   Para obtener información detallada sobre las API de WebView2, vaya a referencia de la [API][Webview2ApiReference].  
*   Para obtener más información sobre WebView2, vaya a [recursos WebView2][Webview2MainNextSteps].  

## Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  


[Webview2ApiReference]: ../webview2-api-reference.md "Referencia de la API de Microsoft Edge WebView2 | Microsoft docs"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Introducción a WebView2 en WPF (vista previa) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2ReferenceWin3209538Icorewebview2Addscripttoexecuteondocumentcreated]: ../reference/win32/0-9-538/icorewebview2.md#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated-0.9.579-interface ICoreWebView2 | Microsoft docs"  
[Webview2ReferenceWpf09515MicrosoftWebExecutescriptasync]: ../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync "ExecuteScriptAsync-Microsoft. Web. WebView2. WPF. WebView2 (clase) | Microsoft docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

---
description: Guía de introducción a WebView2 para aplicaciones WPF
title: Introducción a WebView2 para aplicaciones WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, aplicaciones wpf, wpf, edge, CoreWebView2, control de explorador, html perimetral, introducción, Introducción, .NET
ms.openlocfilehash: 969b6209b6cb84f5345f5b0e533f2e972e81fa58
ms.sourcegitcommit: 01ed086305c06b4e3a0436586524986700276148
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/14/2021
ms.locfileid: "11893872"
---
# <a name="get-started-with-webview2-in-wpf"></a>Introducción a WebView2 en WPF

En este artículo, empieza a crear tu primera aplicación WebView2 y obtén información sobre las características principales de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Para obtener más información sobre las API individuales, vaya a [Referencia de api][DotnetApiMicrosoftWebWebview2Wpf].  

## <a name="prerequisites"></a>Requisitos previos  

Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar.  

*   El tiempo de ejecución de [WebView2][Webview2Installer] o cualquier canal [Microsoft Edge Insider (versión preliminar)][MicrosoftedgeinsiderDownload] debe instalarse en un sistema operativo compatible \(actualmente Windows 10, Windows 8.1 y Windows 7\).  
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 o posterior.  
    
## <a name="step-1---create-a-single-window-app"></a>Paso 1: Crear una aplicación de una sola ventana  

Comience con un proyecto de escritorio básico que contenga una sola ventana principal.  

1.  En Visual Studio, elija **WPF .NET Core App** \(or **WPF .NET Framework App**\) > **Next**.  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-wpf-core.png" alt-text="Núcleo de WPF":::
             Núcleo de WPF :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-wpf-fw.png" alt-text="Marco WPF":::
             Marco WPF :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  Escriba valores para **Project nombre y** **Ubicación**.  Elija **.NET Framework 4.6.2** o posterior **\(o .NET Core 3.0** o posterior\).  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-create-core.png" alt-text="Crear núcleo":::
             Crear núcleo :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-create-fw.png" alt-text="Crear marco":::
             Crear marco :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  Para crear el proyecto, elija **Crear**.  
    
## <a name="step-2---install-webview2-sdk"></a>Paso 2: Instalar WebView2 SDK  

Use NuGet para agregar el SDK de WebView2 al proyecto.  

1.  Mantenga el mouse en el proyecto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Administrar NuGet paquetes...**.  
    
    :::image type="complex" source="./media/wpf-getting-started-mng-nuget.png" alt-text="Administrar paquetes NuGet" lightbox="./media/wpf-getting-started-mng-nuget.png":::
       Administrar paquetes NuGet
    :::image-end:::
    
1.  En la barra de búsqueda, `Microsoft.Web.WebView2` escriba > **elija Microsoft.Web.WebView2**.  
    
    :::image type="complex" source="./media/install-nuget.png" alt-text="NuGet" lightbox="./media/install-nuget.png":::
       NuGet  
    :::image-end:::
    
    Listo para empezar a desarrollar aplicaciones con la API de WebView2.  Para compilar y ejecutar el proyecto, seleccione `F5` .  El proyecto en ejecución muestra una ventana vacía.  
    
    :::image type="complex" source="./media/winforms-empty-app.png" alt-text="Aplicación vacía" lightbox="./media/winforms-empty-app.png":::
       Aplicación vacía  
    :::image-end:::  
    
## <a name="step-3---create-a-single-webview"></a>Paso 3: Crear un único WebView 

A continuación, agregue un WebView a la aplicación.  

1.  En el `MainWindow.xaml` archivo, para agregar el espacio de nombres XAML webView2, inserte la siguiente línea dentro de la `<Window/>` etiqueta.  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    Asegúrese de que el código de `MainWindow.xaml` es similar al siguiente fragmento de código.  
    
    ```xml
    <Window x:Class="WPF_Getting_Started.MainWindow"
            xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
            xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
            xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
            xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
            xmlns:local="clr-namespace:{YOUR PROJECT NAME}"
            xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
            mc:Ignorable="d"
            Title="MainWindow"
            Height="450"
            Width="800"
    >
        <Grid>
        
        </Grid>
    </Window>
    ```  
    
1.  Para agregar el control WebView2, reemplace las `<Grid>` etiquetas por el siguiente fragmento de código.  La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  Para compilar y ejecutar el proyecto, seleccione `F5`  Asegurarse de que el control WebView2 muestre [https://www.microsoft.com][|::ref1::|Main] .  
    
    :::image type="complex" source="./media/wpf-getting-started-microsoft.png" alt-text="Microsoft.com":::
       Microsoft.com
    :::image-end:::  
    
## <a name="step-4---navigation"></a>Paso 4: navegación  

Agregue la capacidad de permitir a los usuarios cambiar la dirección URL que muestra el control WebView2 agregando una barra de direcciones a la aplicación.

1.  En el archivo, agregue una barra de direcciones copiando y pegando el siguiente fragmento de código dentro del `MainWindow.xaml` `<DockPanel>` que contiene WebView.  
    
    ```xml
    <DockPanel DockPanel.Dock="Top">
        <Button x:Name="ButtonGo"
                DockPanel.Dock="Right"
                Click="ButtonGo_Click"
                Content="Go"
        />
        <TextBox Name="addressBar"/>
    </DockPanel>
    ```  
    
    Asegúrese de `<DockPanel>` que la sección del archivo coincide con el siguiente fragmento de `MainWindow.xaml` código.  
    
    ```xml
    <DockPanel>
        <DockPanel DockPanel.Dock="Top">
            <Button x:Name="ButtonGo" DockPanel.Dock="Right" Click="ButtonGo_Click" Content="Go"/>
            <TextBox Name = "addressBar"/>
        </DockPanel>
        <wv2:WebView2 Name = "webView"
                      Source = "https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  En Visual Studio, en el archivo, para agregar el espacio de nombres, inserte el siguiente fragmento de código `MainWindow.xaml.cs` `CoreWebView2` en la parte superior.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  En el archivo, copie el siguiente fragmento de código para crear el método, que navega webview a la `MainWindow.xaml.cs` dirección URL especificada en la barra de `ButtonGo_Click` direcciones.  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    Para compilar y ejecutar el proyecto, seleccione `F5` .  Escriba una nueva dirección URL en la barra de direcciones y elija **Ir**.  Por ejemplo, escribe `https://www.bing.com`.  Asegúrese de que el control WebView2 navega a la dirección URL.  
    
    > [!NOTE]
    > Asegúrese de que se ha escrito una dirección URL completa en la barra de direcciones.  Se `ArgumentException` produce un error si la dirección URL no comienza con o `http://` `https://` .  
    
    :::image type="complex" source="./media/wpf-getting-started-bing.png" alt-text="Bing":::
       bing.com
    :::image-end:::
    
## <a name="step-5---navigation-events"></a>Paso 5: eventos de navegación  

Durante la navegación por la página web, el control WebView2 genera eventos.  La aplicación que hospeda los controles WebView2 escucha los siguientes eventos.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  
    
Para obtener más información, vaya a [Eventos de navegación][Webview2ConceptsNavigationEvents].  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación":::
   Eventos de navegación
:::image-end:::  

Cuando se produce un error, se producen los siguientes eventos y pueden depender de la navegación a una página web de error.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
    
> [!NOTE]
> Si se produce un redireccionamiento HTTP, hay varios `NavigationStarting` eventos en una fila.  

Para demostrar cómo usar los eventos, registre un controlador para que cancele las solicitudes que no son `NavigationStarting` HTTPS.  

En el `MainWindow.xaml.cs` archivo, modifique el constructor para que coincida con el siguiente fragmento de código y agregue la `EnsureHttps` función.  

```csharp
public MainWindow()
{
    InitializeComponent();
    webView.NavigationStarting += EnsureHttps;
}

void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
}
```  

En el constructor, `EnsureHttps` se registra como el controlador de eventos en el evento en el control `NavigationStarting` WebView2.  

Para compilar y ejecutar el proyecto, seleccione `F5` .  Asegúrese de que al navegar a un sitio HTTP, webView permanece sin cambios.  Sin embargo, WebView navega a sitios HTTPS.  

## <a name="step-6---scripting"></a>Paso 6: Scripting  

Puede usar aplicaciones host para insertar código JavaScript en controles WebView2 en tiempo de ejecución.  Puede realizar la tarea WebView para ejecutar JavaScript arbitrario o agregar scripts de inicialización.  JavaScript inyectado se aplica a todos los nuevos documentos de nivel superior y a los fotogramas secundarios hasta que se quita JavaScript.  JavaScript inyectado se ejecuta con un tiempo específico.  

*   Ejecutarlo después de la creación del objeto global.  
*   Ejecutarlo antes de que se ejecute cualquier otro script incluido en el documento HTML.  
    
Por ejemplo, agregue scripts que envíen una alerta cuando un usuario navegue a sitios que no son HTTPS.  Modifique la `EnsureHttps` función para insertar un script en el contenido web que usa el método [ExecuteScriptAsync.](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync)  

```csharp
void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        webView.CoreWebView2.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
}
```  

Para compilar y ejecutar el proyecto, seleccione `F5` .  Asegúrate de que la aplicación muestra una alerta cuando navegas a un sitio web que no usa HTTPS.  

:::image type="complex" source="./media/wpf-getting-started-https.png" alt-text="HTTPS":::
   HTTPS
:::image-end:::  

## <a name="step-7---communication-between-host-and-web-content"></a>Paso 7: comunicación entre contenido de host y web  

El contenido de host y web puede comunicarse de las siguientes maneras mediante `postMessage` .  

*   El contenido web de un control WebView2 puede publicar un mensaje en el host mediante `window.chrome.webview.postMessage` .  El host controla el mensaje con cualquier registrado `WebMessageReceived` en el host.  
*   Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON` .  Los controladores agregados a `window.chrome.webview.addEventListener` .  
    
El mecanismo de comunicación pasa mensajes del contenido web al host mediante funcionalidades nativas.  

En el proyecto, cuando el control WebView2 navega a una dirección URL, muestra la dirección URL en la barra de direcciones y alerta al usuario de la dirección URL mostrada en el control WebView2.  

1.  En el `MainWindow.xaml.cs` archivo, actualice el constructor y cree una `InitializeAsync` función que coincida con el siguiente fragmento de código.  La `InitializeAsync` función espera [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) porque la inicialización de `CoreWebView2` es asincrónica.  
    
    ```csharp
    public MainWindow()
    {
        InitializeComponent();
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }
    
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  
    
1.  Después **de inicializar CoreWebView2,** registre un controlador de eventos para responder a `WebMessageReceived` .  In `MainWindow.xaml.cs` , update and add using the following code `InitializeAsync` `UpdateAddressBar` snippet.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
    }
    
    void UpdateAddressBar(object sender, CoreWebView2WebMessageReceivedEventArgs args)
    {
        String uri = args.TryGetWebMessageAsString();
        addressBar.Text = uri;
        webView.CoreWebView2.PostWebMessageAsString(uri);
    }
    ```  
    
1.  Para que WebView envíe y responda al mensaje web, después `CoreWebView2` de inicializarse, el host:  
    1.  Inserta un script en el contenido web que registra un controlador para imprimir el mensaje desde el host.  
    1.  Inserta un script en el contenido web que publica la dirección URL en el host.  
        
    En el `MainWindow.xaml.cs` archivo, actualice `InitializeAsync` para que coincida con el siguiente fragmento de código.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    Para compilar y ejecutar la aplicación, seleccione `F5` .  Ahora, la barra de direcciones muestra el URI en el control WebView2.  Cuando navega correctamente a un nuevo URI, el control WebView2 avisa al usuario del URI que se muestra en el control WebView2.  
    
    :::image type="complex" source="./media/wpf-getting-started-searchbar.png" alt-text="addressBar":::
       addressBar
    :::image-end:::
    
Enhorabuena, has creado tu primera aplicación WebView2.  

## <a name="next-steps"></a>Pasos siguientes  

Para seguir aprendiendo más sobre WebView2, vaya a los siguientes recursos.  

*   Para obtener más información sobre cómo crear aplicaciones webView2, vaya a Procedimientos recomendados de desarrollo [de WebView2][WV2BestPractices].  
*   Para obtener un ejemplo completo de las funcionalidades de WebView2, vaya a [WebView2Samples repo][GithubMicrosoftedgeWebview2samplesMain] en GitHub.  
*   Para obtener información más detallada acerca de la API de WebView2, vaya a [Referencia de API](/dotnet/api/microsoft.web.webview2.wpf.webview2).  
*   Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2](../index.md#next-steps).  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Ponerse en contacto con el equipo de Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  
 
[WV2BestPractices]: ../concepts/developer-guide.md "Procedimientos recomendados de desarrollo de WebView2 | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegación | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Espacio de nombres Microsoft.Web.WebView2.Wpf | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Clase WebView2 | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "Método WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 | Microsoft Edge Programador"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualStudioMain]: https://visualstudio.microsoft.com "Microsoft Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador de WebView2" 

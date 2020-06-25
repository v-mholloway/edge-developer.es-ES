---
description: Hospedar contenido web en la aplicación WPF con el control de WebView 2 de Microsoft Edge
title: Vista previa de Microsoft Edge 2 para aplicaciones de WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicaciones WPF, WPF, Edge, CoreWebView2, control de explorador, código HTML de Edge, introducción, .NET
ms.openlocfilehash: 9ecb80050d52d1d3b888027a728456a881d8c5ad
ms.sourcegitcommit: 8f2badc98ea7b7d1861dabfaf0e4dd8677e89bea
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2020
ms.locfileid: "10767019"
---
# Introducción a WebView2 en WPF (vista previa)

En este artículo, empiece a crear su primera aplicación de WebView2 y obtenga información sobre las características principales de [WebView2 (versión preliminar)](../index.md).  Para obtener más información sobre las API individuales, consulta referencia de la [API](../reference/dotnet/0-9-515-reference-webview2.md).  

## Requisitos previos  

Asegúrese de haber instalado la siguiente lista de requisitos previos antes de continuar:  

* [Canal Canarias de Microsoft Edge (cromo)](https://www.microsoftedgeinsider.com/download) instalado en Windows 10, Windows 8,1 o Windows 7.  
* [Visual Studio](https://visualstudio.microsoft.com/) 2017 o posterior.  

## Paso 1: crear una aplicación de una sola ventana  

Empiece con un proyecto de escritorio básico que contenga una única ventana principal.  

1.  Abra **Visual Studio**.  
1.  Seleccione aplicación **.net Core de WPF** o **aplicación .NET Framework de WPF**y, a continuación, seleccione **siguiente**.  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="WPF Core":::
             WPF Core :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Marco WPF":::
             Marco WPF :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  Escriba los valores para **el nombre** y la **Ubicación**del proyecto.  Seleccione .NET Framework 4.6.2 o posterior o .NET Core 3,0 o posterior.  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Crear núcleo":::
                 Crear núcleo :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Crear marco de trabajo":::
                 Crear marco de trabajo :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  Seleccione **crear** para crear el proyecto.  
    
## Paso 2: instalar el SDK de WebView2  

A continuación, agregue el SDK de WebView2 al proyecto.  Para obtener la vista previa, instala el SDK de WebView2 con Nuget.  

1.  Abra el menú contextual en el proyecto \ (haga clic con el botón derecho \) y seleccione **administrar paquetes NuGet...**.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Nuget":::
       Nuget
    :::image-end:::
    
2.  Escriba `Microsoft.Web.WebView2` en la barra de búsqueda.  Seleccione **Microsoft. Web. WebView2** en los resultados de la búsqueda.  

3. Marque la opción **incluir versión preliminar**, seleccione una versión de paquete de versión **preliminar** y, a continuación, elija **instalar**.  
  
     ![Nuget](./media/installnuget.PNG)
    
    Ya está todo listo para empezar a desarrollar aplicaciones con la API de WebView2.  Pulse `F5` para compilar y ejecutar el proyecto.  El proyecto en ejecución muestra una ventana vacía.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Aplicación vacía":::
       Aplicación vacía :::image-end:::  
    
## Paso 3: crear una sola vista previa en MainWindow. Xaml  

A continuación, agregue una vista de vista a la aplicación.  

1.  Abra `MainWindow.xaml` .  Agrega el espacio de nombres XAML WebView2 insertando la siguiente línea dentro de la `<Window/>` etiqueta.  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    Confirme que el código de `MainWindow.xaml` la es similar al siguiente fragmento de código.  
    
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
    
1.  Agregue el control WebView2 reemplazando las `<Grid>` etiquetas, con el siguiente fragmento de código.  La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  Pulse `F5` para compilar y ejecutar el proyecto.  Confirme que se muestra el control WebView2 [https://www.microsoft.com](https://www.microsoft.com) .  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       Microsoft.com
    :::image-end:::  
    
## Paso 4: navegación  

Agregue una barra de direcciones a la aplicación para permitir a los usuarios que cambien la dirección URL que muestra el control WebView2.

1.  En **MainWindow. Xaml**, agregue una barra de direcciones copiando y pegando el siguiente fragmento de código dentro de la DockPanel que contiene la vista de gráfico.  
    
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
    
    Confirme que la `DockPanel` sección de `MainWindow.xaml` aparece como el siguiente fragmento de código.  
    
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
    
1.  Abrir `MainWindow.xaml.cs` en Visual Studio.  Para agregar el `CoreWebView2` espacio de nombres, inserte el siguiente fragmento de código en la parte superior de `MainWindow.xaml.cs` .  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  En **MainWindow.Xaml.CS**, copie el siguiente fragmento de código para crear el `ButtonGo_Click` método, que navega por la vista en vista previa a la dirección URL que se escribe en la barra de direcciones.  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    Pulse `F5` para compilar y ejecutar el proyecto.  Escriba una nueva dirección URL en la barra de direcciones y seleccione **ir**.  Por ejemplo, escriba `https://www.bing.com` .  Confirme que el control WebView2 se desplaza hasta la dirección URL.  
    
    > [!NOTE]
    > Asegúrese de que se escribe una dirección URL completa en la barra de direcciones.  `ArgumentException`Se inicia una si la dirección URL no comienza con `http://` o `https://` .  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       Bing
    :::image-end:::
    
## Paso 5: eventos de navegación  

La aplicación que hospeda los controles WebView2 escucha los siguientes eventos provocados por el control WebView2 durante la navegación a páginas Web.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

Para obtener más información, vea [eventos de navegación](../reference/win32/0-9-488/icorewebview2.md#navigation-events).  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación":::
   Eventos de navegación
:::image-end:::  

Cuando se produce un error, se producen los eventos siguientes y puede que dependan de la navegación a una página de error.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

Cuando hay una redirección de HTTP, hay varios `NavigationStarting` eventos.  

Para mostrar cómo usar estos eventos, comienza registrando un controlador para `NavigationStarting` que cancele todas las solicitudes que no usen https.  

En `MainWindow.xaml.cs` , modifique el constructor como se muestra a continuación y agregue la `EnsureHttps` función.  

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

En el constructor, EnsureHttps se registra como el controlador de eventos en el `NavigationStarting` evento en el control de WebView2.  

Pulse `F5` para compilar y ejecutar el proyecto.  Confirme que, al navegar a un sitio HTTP, la WebView no sufre **cambios**.  Sin embargo, la vista Web se desplaza a sitios HTTPS.  

## Paso 6: scripting  

Puede usar aplicaciones host para inyectar código JavaScript en controles WebView2 en tiempo de ejecución.  El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a los fotogramas secundarios hasta que se quite el JavaScript.  El código JavaScript insertado se ejecuta después de la creación del objeto global y antes de que se ejecute cualquier otro script incluido en el documento HTML.  

Puede usar scripting para avisar al usuario cuando navegue a un sitio que no es HTTPS.  Modifique la `EnsureHttps` función para que inserte el script en el contenido web con el método [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) .  

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

Pulse `F5` para compilar y ejecutar el proyecto.  Confirme que la aplicación muestra una alerta cuando se desplaza a un sitio que no usa HTTPS.  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   HTTPS
:::image-end:::  

## Paso 7: comunicación entre el host y el contenido web  

El host y el contenido web pueden comunicarse entre sí mediante las `postMessage` siguientes acciones:  

*   El contenido Web de un control WebView2 puede publicar un mensaje en el host mediante `window.chrome.webview.postMessage` .  El anfitrión controla el mensaje con cualquier registro `WebMessageReceived` en el host.  
*   Los anfitriones se exponen en el contenido web en un control WebView2 mediante `CoreWebView2.PostWebMessageAsString` o `CoreWebView2.PostWebMessageAsJSON` .  Estos mensajes los detectan los controladores agregados a `window.chrome.webview.addEventListener` .  

Este mecanismo de comunicación permite que el contenido web transmita mensajes al host mediante capacidades nativas.  

En el proyecto, cuando el control WebView2 navega a una dirección URL, muestra la dirección URL en la barra de direcciones y alerta al usuario de la dirección URL que se muestra en el control de WebView2.  

1.  En **MainWindow.Xaml.CS**, actualice el constructor y cree una `InitializeAsync` función tal como se muestra en el siguiente fragmento de código.  La `InitializeAsync` función espera [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) porque la inicialización `CoreWebView2` es asincrónica.  
    
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
    
1.  Después de inicializar **CoreWebView2** , registra un controlador de eventos para responder `WebMessageReceived` .  En la actualización de **MainWindow.Xaml.CS** `InitializeAsync` y agregue `UpdateAddressBar` con el siguiente fragmento de código.  
    
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
    
1.  Para que la vista Web pueda enviar y responder al mensaje Web, después de que `CoreWebView2` se inicialice, el host:  
    
    1.  Inserta un script en el contenido web que registra un controlador para imprimir el mensaje desde el host.  
    1.  Inserta un script en el contenido web que publica la dirección URL en el host.  
    
    En `MainWindow.xaml.cs` , actualice `InitializeAsync` como se indica a continuación:  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    Pulse `F5` para compilar y ejecutar la aplicación.  Ahora la barra de direcciones muestra el URI en la vista de vista previa y, al navegar correctamente a un nuevo URI, la WebView alerta al usuario del URI que se muestra en la vista de vista en WebView.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="Direcciones":::
       Direcciones
    :::image-end:::

¡ Enhorabuena! has creado tu primera WebView2 aplicación.  

## Pasos siguientes  

*   Para obtener un ejemplo completo de las capacidades de WebView2, consulta [repositorio de WebView2Samples](https://github.com/MicrosoftEdge/WebView2Samples) en github.  
*   Para obtener información más detallada sobre las API de WebView2, consulta referencia de la [API](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md).  
*   Para obtener más información sobre WebView2, consulte [recursos WebView2](../index.md#next-steps).  

## Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge  

Ayuda a crear una experiencia WebView2 más rica compartiendo tus comentarios.  Visite el [repositorio de comentarios](https://github.com/MicrosoftEdge/WebViewFeedback) de WebView de Microsoft Edge para enviar solicitudes de características o informes de errores o buscar problemas conocidos.  

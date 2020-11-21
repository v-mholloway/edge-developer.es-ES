---
description: Guía de introducción a WebView2 para aplicaciones WinUI
title: Introducción a WebView2 para las aplicaciones WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, WinUI aplicaciones, WinUI, Edge, CoreWebView2, control del explorador, código HTML de Edge, introducción, .NET
ms.openlocfilehash: a1ccffe332f71ee9d53ff267e8cca6bdbda81703
ms.sourcegitcommit: 02c602379537ab3b9d0a355cea7fcf96fdbd8870
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2020
ms.locfileid: "11182724"
---
# Introducción a WebView2 en WinUI 3 (vista previa)  

En este artículo, aprenderá a crear su primera aplicación de WebView2 y sobre las características principales de [Introducción a Microsoft Edge WebView2 (versión preliminar)][Webview2Index].  Tu primera WebView2 aplicación usa WinUI3.  Para obtener más información sobre las API individuales, vaya a referencia de la [API][GithubMicrosoftUiXamlSpecsWebview2].  

## Requisitos previos  

Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar con el siguiente artículo.  

1.  Windows 10 versión 1803 \ (compilación 17134 \) o posterior.  Para obtener más información, vaya a [Windows Update: preguntas más frecuentes][MicrosoftSupport12373].  
1.  [Canal Canarias de Microsoft Edge (cromo)][MicrosoftedgeinsiderDownload] en Windows 10, Windows 8,1 o Windows 7.  
1.  Visual Studio 2019, versión 16,9 Preview.  Para obtener más información, vaya a la [biblioteca de interfaces de usuario de Windows 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].  
    
    Incluya las siguientes cargas de trabajo al instalar Visual Studio.  
    
    *   Desarrollo de escritorio .NET \ (el instalador también instala .NET 5 \)  
    *   Desarrollo de la plataforma universal de Windows  
        
    Para crear aplicaciones de C++, también debe incluir las siguientes cargas de trabajo.  
    
    *   Desarrollo de escritorio con C++  
    *   El componente opcional de las herramientas de la plataforma universal de Windows de C++ (v142) para la carga de trabajo de la plataforma universal de Windows.  Para obtener más información, vaya a detalles de instalación en la sección desarrollo de la plataforma universal de Windows, en el panel derecho.  
        
1.  Asegúrese de que su sistema tiene habilitado un origen de paquete NuGet para [Nuget.org][NugetHome].  Para obtener más información, vaya a [configuraciones comunes de NuGet][NugetConsumePackagesConfiguringNugetBehavior] y a [Windows Community Toolkit][WindowsCommunitytoolkit].  
1.  Descargue e instale el [paquete VSIX de la versión preliminar de WinUI 3][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].  El instalador agrega las plantillas de proyecto WinUI 3 y el paquete NuGet que contiene las bibliotecas WinUI 3 a Visual Studio 2019.  
    
    Para obtener instrucciones sobre cómo agregar el paquete VSIX a Visual Studio, vaya a [Buscar y usar las extensiones de Visual Studio][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].
    
1.  Habilite el [modo de desarrollador][WindowsUwpGetStartedEnableYourDeviceForDevelopment] para asegurarse de que tiene acceso a todas las características de Visual Studio específicas del desarrollador.  
    
## Paso 1: crear proyecto  

Empiece con un proyecto de escritorio básico que contenga una única ventana principal.  

1.  En Visual Studio, elija **crear un nuevo proyecto**.  
1.  En la lista desplegable proyecto, elija **C#**, **Windows**y **WinUI** respectivamente.  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Crear un nuevo proyecto WinUI con Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        Crear un nuevo proyecto WinUI con Visual Studio
    :::image-end:::  
    
1.  Seleccione **aplicación en blanco, empaquetada (WinUI en el escritorio)** y, a continuación, elija **siguiente**.  
1.  Escriba un nombre de proyecto, elija otras opciones según sea necesario y, a continuación, elija **crear**.  
1.  En **nuevo proyecto de plataforma universal de Windows**, elija los valores siguientes y, a continuación, elija **Aceptar**.  
    *   **Versión de destino**:  **Windows 10, versión 1903 (compilación 18362)** o posterior  
    *   **Versión mínima**:  **Windows 10, versión 1803 (compilación 17134)**  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="El nuevo cuadro de diálogo de proyecto de la plataforma universal de Windows con los valores elegidos para la versión de destino y la versión mínima." lightbox="./media/winui-gettingstarted-projecttype.png":::
       El nuevo cuadro de diálogo de proyecto de la plataforma universal de Windows con los valores elegidos para la versión de destino y la versión mínima.
    :::image-end:::  
    
1.  En el explorador de soluciones, se generan dos proyectos.  
    *   **Nombre del proyecto (escritorio)**.  Este proyecto contiene el código de la aplicación.  **App.Xaml.CS** define una `Application` clase que representa la instancia de la aplicación.  **MainWindow.Xaml.CS** define una `MainWindow` clase que representa la ventana principal que muestra la instancia de la aplicación.  Estas clases se derivan de tipos en el `Microsoft.UI.Xaml` espacio de nombres WinUI.  
    
    *   **Nombre del proyecto (paquete)**.  Este proyecto es un proyecto de empaquetado de aplicaciones para Windows que está configurado para generar la aplicación en un paquete MSIX para su implementación.  El proyecto contiene el manifiesto del paquete de la aplicación y es el proyecto de inicio de la solución de forma predeterminada.  Para obtener más información, vaya a [configurar la aplicación de escritorio para el empaquetado de MSIX en Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] y [Referencia del esquema del manifiesto de paquete para Windows 10][UwpSchemasAppxpackageUapmanifestRoot].
    
1.  En el explorador de soluciones, para mostrar el código, Abra `MainWindow.xaml` archivo.  Seleccione `F5` para ejecutar el proyecto y mostrar una ventana con un botón.  
    
## Paso 2: agregar un control WebView2 a un proyecto  

A continuación, agregue un control WebView2 al proyecto.  

1.  Abra `MainWindow.xaml` .  Agrega el espacio de nombres XAML WebView2 insertando la siguiente línea dentro de la `<Window/>` etiqueta.  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Confirme que el código `MainWindow.xaml` es similar al siguiente fragmento de código.  
    
    ```xml
    <Window
          x:Class="WinUI_Sample.MainWindow"
          xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
          xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
          xmlns:local="using:WinUI_Sample"
          xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
          xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
          mc:Ignorable="d"
          xmlns:controls="using:Microsoft.UI.Xaml.Controls"
          >
        
          <StackPanel Orientation="Horizontal" HorizontalAlignment="Center" VerticalAlignment="Center">
            <Button x:Name="myButton" Click="myButton_Click">Click Me</Button>
          </StackPanel>
    
    </Window>
    ```  
    
1.  Para agregar el control WebView2, reemplace las `<StackPanel>` etiquetas con el siguiente fragmento de código.  La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.  
    
    ```xml  
    <Grid>

        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
        
        <controls:WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  Abra `MainWindow.xaml.cs` y comente la línea siguiente.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Seleccione `F5` para compilar y ejecutar el proyecto.  Confirme que se muestra el control WebView2 [https://www.microsoft.com][|::ref1::|Main] .  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Un control WebView2 que muestra el sitio de microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       Un control WebView2 que muestra el sitio de microsoft.com.  
    :::image-end:::  
    
## Paso 3: agregar controles de navegación  

Permite a los usuarios controlar la página web que se muestra en el control WebView2 agregando una barra de direcciones a la aplicación.  

1.  En `MainWindow.xaml` , copie y pegue el siguiente fragmento de código dentro del `Grid` elemento que contiene el `WebView2` elemento.  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    Confirme que su `Grid` elemento de `MainWindow.xaml` es similar al siguiente fragmento de código.  
    
    ```xml
    <Grid>
    
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
    
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
        
        <WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  En `MainWindow.xaml.cs` , copie el siguiente fragmento de código en `myButton_Click` , que navega por el control WebView2 a la dirección URL que se escribe en la barra de direcciones.  
    
    ```csharp
    private void myButton_Click(object sender, RoutedEventArgs e)
    {
        try
        {
            Uri targetUri = new Uri(addressBar.Text);
            MyWebView.Source = targetUri;
        }
        catch (FormatException ex)
        {
            // Incorrect address entered.
        }
    }
    ```  
    
    Seleccione `F5` para compilar y ejecutar el proyecto.  Escriba una nueva dirección URL en la barra de direcciones y, después, elija **ir**.  Por ejemplo, escriba `https://www.bing.com` .  
    
    > [!NOTE]
    > Asegúrate de usar direcciones URL completas en la barra de direcciones.  `ArgumentException` las excepciones se inician si la dirección URL no comienza con `http://` o `https://` .  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       Bing.com  
    :::image-end:::  
    
## Paso 4: eventos de navegación  

Las aplicaciones que hospedan controles WebView2 escuchan los siguientes eventos provocados por los controles de WebView2 durante la navegación por la Página Web.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> Las redirecciones HTTP generan varios `NavigationStarting` eventos.  

Para obtener más información, vaya a [eventos de navegación][Webviews2ConceptsNavigationEvents].  

Cuando se producen errores, se producen los eventos siguientes y puede navegar a una página de error.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
Para obtener un ejemplo de cómo usar los eventos, registra un controlador para `NavigationStarting` que cancele cualquier solicitud que no use HTTPS.  En `MainWindow.xaml.cs` , modifique el constructor para registrarlo `EnsureHttps` y agregue la `EnsureHttps` función para que coincida con el siguiente fragmento de código.  

```csharp
public MainWindow()
{
    InitializeComponent();
    MyWebView.NavigationStarting += EnsureHttps;
}

private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

Seleccione `F5` para compilar y ejecutar el proyecto.  Confirme que la navegación está bloqueada en sitios HTTP y que se permite en sitios HTTPS.  

## Paso 5: scripting  

Las aplicaciones de host pueden inyectar código JavaScript en controles WebView2 en tiempo de ejecución.  El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a cualquier fotograma secundario hasta que se quite el JavaScript.  El JavaScript insertado se ejecuta con intervalos específicos.  

*   Ejecútelo después de crear el objeto global.  
*   Ejecútelo antes de ejecutar cualquier otro script incluido en el documento HTML.  

Como ejemplo, agregar scripts envía una alerta cuando un usuario navega a sitios que no son HTTPS.  Modifique la `EnsureHttps` función para insertar un script en el contenido web que usa [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].  

```csharp
private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        MyWebView.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

Seleccione `F5` para compilar y ejecutar el proyecto.  Confirme que su aplicación muestra una alerta cuando se desplaza a un sitio que no usa HTTPS.  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Control WebView2 que muestra un cuadro de diálogo de alerta" lightbox="./media/winui-gettingstarted-script.png":::
   Control WebView2 que muestra un cuadro de diálogo de alerta
:::image-end:::  

Enhorabuena, has creado tu primera aplicación de WebView2.  

## Pasos siguientes  

Nuestro equipo está actualmente generando más API de WebView2.  Para obtener más información sobre el estado actual de las API de WebView2, vaya a la [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2].  

> [!NOTE]
> Es posible que el objeto WinRT CoreWebView2 no esté disponible en el momento en que se envían las API de WebView2.  Para comprender las API que están disponibles para los controles de WebView2, vaya a [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] para obtener una lista de las API que están disponibles.  

Para obtener más información sobre las capacidades de WebView2, vaya a [WebView2 conceptos y guías de How-To][Webview2IndexNextSteps] y al [repositorio de ejemplos de WebView2][GithubMicrosoftedgeWebview2samplesMain].  

## Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegación | Microsoft docs"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync " MétodoWebView2.ExecuteScriptAsync (String) (Microsoft. Web. WebView2. WPF) | Microsoft docs"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Configuraciones de NuGet comunes | Microsoft docs"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Referencia del esquema del manifiesto del paquete para Windows 10 | Microsoft docs"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Instalar sin usar el cuadro de diálogo administrar extensiones: administrar extensiones para Visual Studio | Microsoft docs"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurar el entorno de desarrollo: biblioteca de interfaces de usuario de Windows 3,0 Preview 1 (mayo de 2020) | Microsoft docs"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Documentación del kit de herramientas de Windows Microsoft docs"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurar la aplicación de escritorio para el empaquetado de MSIX en Visual Studio | Microsoft docs"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Habilitar el dispositivo para el desarrollo | Microsoft docs"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 espec-Microsoft/Microsoft-UI-XAML-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Técnico"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: preguntas más frecuentes"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar los canales de Insider de Microsoft Edge"  

[NugetHome]: https://nuget.org "Inicio | Galería de NuGet"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Descargar dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Plantillas de proyecto WinUI 3 | Marketplace de Visual Studio"  

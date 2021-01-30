---
description: Guía de introducción a WebView2 para aplicaciones WinUI
title: Introducción a WebView2 para aplicaciones WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, winui apps, winui, edge, CoreWebView2, control del explorador, edge html, getting started, Getting Started, .NET
ms.openlocfilehash: 5188a735eaf635c3b3bc0eead6f4ee4f3a83f1c4
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306155"
---
# Introducción a WebView2 en WinUI 3 (versión preliminar)  

En este artículo, empieza a crear tu primera aplicación WebView2 y obtén información sobre las características principales [de WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  La primera aplicación WebView2 usa WinUI3.  Para obtener más información sobre las API individuales, vaya a [la referencia de la API.][GithubMicrosoftUiXamlSpecsWebview2]  

## Requisitos previos  

Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar.  

*   [WebView2 Runtime][Webview2Installer] o cualquier canal no estable de [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado en Windows 10 versión 1803 \(compilación 17134\) o posterior.  Para obtener más información sobre Windows 10, ve a [Windows Update: Preguntas más frecuentes.][MicrosoftSupport12373]  
    
    > [!NOTE]
    > El equipo de WebView recomienda usar el canal Canary y la versión mínima necesaria es 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2019, versión 16.9 Preview.  Para obtener más información, ve a la Biblioteca [de interfaz de usuario de Windows 3 Preview 3.][WindowsAppsWinui3ConfigureYourDevEnvironment]  
    
    *   Incluya las siguientes cargas de trabajo al instalar Visual Studio.  
        *   Desarrollo de escritorio .NET \(el instalador también instala .NET 5\)  
        *   Desarrollo de la Plataforma universal de Windows  
    *   Para crear aplicaciones de C++, también debes incluir las siguientes cargas de trabajo.  
        *   Desarrollo de escritorio con C++  
        *   El componente opcional de las herramientas de la Plataforma universal de Windows C++ \(v142\) para la carga de trabajo de la Plataforma universal de Windows.  Para obtener más información, ve a **Detalles de instalación** en la sección desarrollo de la Plataforma universal de **Windows,** en el panel derecho.  
        
## Paso 0: configuración Visual Studio configuración  

1.  Asegúrese de que el sistema tiene un origen de paquete NuGet habilitado para [nuget.org][NugetHome].  Para obtener más información, vaya a [configuraciones de NuGet comunes][NugetConsumePackagesConfiguringNugetBehavior] y [a Windows Community Toolkit.][WindowsCommunitytoolkit]  
1.  Descarga e instala el paquete [VSIX de WinUI 3 Preview 3.][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]  El instalador agrega las plantillas de proyecto WinUI 3 y el paquete NuGet que contiene las bibliotecas de WinUI 3 a Visual Studio 2019.  
    
    Para obtener instrucciones sobre cómo agregar el paquete a Visual Studio, vaya a Buscar y `VSIX` [usar Visual Studio extensiones.][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]
    
1.  Para obtener acceso a todas las características de Visual Studio específicas del desarrollador, activa el [modo de desarrollador.][WindowsUwpGetStartedEnableYourDeviceForDevelopment]  
    
## Paso 1: Crear proyecto  

Comience con un proyecto de escritorio básico que contenga una sola ventana principal.  

1.  En Visual Studio, elija **Crear un nuevo proyecto.**  
1.  En la lista desplegable del proyecto, elija **C#**, **Windows**y **WinUI** respectivamente.  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Crear un nuevo proyecto de WinUI con Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        Crear un nuevo proyecto de WinUI con Visual Studio
    :::image-end:::  
    
1.  Choose **Blank App, Packaged (WinUI in Desktop)**  >  **Next**.  
1.  Escriba un nombre de proyecto.
1.  Elija las opciones según sea necesario.  
1.  Elija **Crear**.  
1.  En **Nuevo proyecto de plataforma universal de Windows,** elija los siguientes valores y, a continuación, elija **Aceptar.**  
    *   **Versión de**destino:  **Windows 10, versión 1903 (compilación 18362)** o posterior  
    *   **Versión mínima:**  **Windows 10, versión 1803 (compilación 17134)**  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Cuadro de diálogo Nuevo proyecto de plataforma universal de Windows con los valores elegidos para la versión de destino y la versión mínima." lightbox="./media/winui-gettingstarted-projecttype.png":::
       Cuadro de diálogo Nuevo proyecto de plataforma universal de Windows con los valores elegidos para la versión de destino y la versión mínima.
    :::image-end:::  
    
1.  En el Explorador de soluciones, se generan dos proyectos.  
    *   **El nombre del proyecto (escritorio).**  El proyecto de escritorio contiene el código de la aplicación.  El `App.xaml.cs` archivo define una clase que representa la instancia de la `Application` aplicación.  El `MainWindow.xaml.cs` archivo define una clase que representa la ventana principal que muestra la instancia de la `MainWindow` aplicación.  Las clases derivan de tipos en el `Microsoft.UI.Xaml` espacio de nombres de WinUI.  
    *   **El nombre del proyecto (paquete).**  El proyecto de paquete es un proyecto de empaquetado de aplicaciones de Windows que está configurado para compilar la aplicación en un paquete MSIX para su implementación.  El proyecto contiene el manifiesto del paquete de la aplicación y es el proyecto de inicio de la solución de forma predeterminada.  Para obtener más información, ve a Configurar la aplicación de escritorio para el empaquetado [MSIX][WindowsMsixDesktopToUwpPackagingDotNet] en Visual Studio y la referencia del esquema del manifiesto del paquete [para Windows 10.][UwpSchemasAppxpackageUapmanifestRoot]  
1.  En el Explorador de soluciones, para mostrar el código, abra el `MainWindow.xaml` archivo.  Para ejecutar el proyecto y mostrar una ventana con un botón, seleccione `F5` .  
    
## Paso 2: Agregar un control WebView2 al proyecto  

Agrega un control WebView2 al proyecto.  

1.  En el `MainWindow.xaml` archivo, para agregar el espacio de nombres XAML WebView2, inserta la siguiente línea dentro de la `<Window/>` etiqueta.  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Asegúrese de que el código `MainWindow.xaml` es similar al siguiente fragmento de código.  
    
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
    
1.  Para agregar el control WebView2, reemplace las `<StackPanel>` etiquetas por el siguiente fragmento de código.  La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.  
    
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
    
1.  En el `MainWindow.xaml.cs` archivo, comente la siguiente línea.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Para compilar y ejecutar el proyecto, seleccione `F5` .  Asegúrese de que se muestra el control WebView2 [https://www.microsoft.com][|::ref1::|Main] .  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="El control WebView2 muestra microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       El control WebView2 muestra microsoft.com  
    :::image-end:::  
    
## Paso 3: Agregar controles de navegación  

Para permitir a los usuarios controlar la página web que se muestra en el control WebView2, agrega una barra de direcciones a la aplicación.  

1.  En el archivo, copie y pegue el siguiente fragmento de código `MainWindow.xaml` dentro del elemento que contiene el `<Grid>` `WebView2` elemento.  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    Asegúrese de `<Grid>` que el elemento del archivo es similar al siguiente fragmento de `MainWindow.xaml` código.  
    
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
    
1.  En el archivo, copie el siguiente fragmento de código en , que navega por el control WebView2 a la dirección URL especificada `MainWindow.xaml.cs` en la barra de `myButton_Click` direcciones.  
    
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
    
    Para compilar y ejecutar el proyecto, seleccione `F5` .  Escriba una nueva dirección URL en la barra de direcciones y, a continuación, elija **Ir**.  Por ejemplo, escriba `https://www.bing.com` .  
    
    > [!NOTE]
    > Asegúrese de escribir direcciones URL completas en la barra de direcciones.  `ArgumentException` se inician excepciones si la dirección URL no comienza con `http://` o `https://` .  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       bing.com  
    :::image-end:::  
    
## Paso 4: Eventos de navegación  

Las aplicaciones que hospedan controles WebView2 escuchan los siguientes eventos que los controles WebView2 genera durante la navegación de la página web.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> Si se produce un redireccionamiento HTTP, hay varios `NavigationStarting` eventos en una fila.  

Para obtener más información, vaya a [Eventos de navegación.][Webviews2ConceptsNavigationEvents]  

Cuando se producen errores, se producen los siguientes eventos y pueden navegar a una página web de error.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
Como ejemplo de cómo usar los eventos, registre un controlador para que cancele las solicitudes que no `NavigationStarting` son HTTPS.  In `MainWindow.xaml.cs` , modify the constructor to register , and add the function so that it matches the following `EnsureHttps` code `EnsureHttps` snippet.  

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

Para compilar y ejecutar el proyecto, seleccione `F5` .  Asegúrese de que la navegación está bloqueada en sitios HTTP y permitida para los sitios HTTPS.  

## Paso 5: Scripting  

Puedes usar aplicaciones host para insertar código JavaScript en controles WebView2 en tiempo de ejecución.  Puede hacer que WebView ejecute JavaScript arbitrario o agregue scripts de inicialización.  El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a todos los fotogramas secundarios hasta que se quite el JavaScript.  El JavaScript inyectado se ejecuta con intervalos específicos.  

*   Ejecutarlo después de la creación del objeto global.  
*   Ejecutarlo antes de ejecutar cualquier otro script incluido en el documento HTML.  

Por ejemplo, agregue scripts que envíen una alerta cuando un usuario navegue a sitios que no son HTTPS.  Modifique la `EnsureHttps` función para insertar un script en el contenido web que usa [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].  

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

Para compilar y ejecutar el proyecto, seleccione `F5` .  Asegúrate de que la aplicación muestra una alerta cuando navegas a cualquier sitio web que no sea HTTPS.  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="El control WebView2 muestra un cuadro de diálogo de alerta" lightbox="./media/winui-gettingstarted-script.png":::
   El control WebView2 muestra un cuadro de diálogo de alerta
:::image-end:::  

Enhorabuena, has creado tu primera aplicación WebView2.  

## Pasos siguientes  

Para continuar con el aprendizaje sobre WebView2, vaya a los siguientes recursos.  

### Consulte también  

*   Para obtener un ejemplo completo de las capacidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].  
    
    > [!NOTE]
    > Es posible que el objeto WinRT CoreWebView2 no esté disponible con la versión de la API de WebView2.  Para comprender qué API están disponibles para los controles WebView2, ve a [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] para obtener una lista de las API que están disponibles.  
    
*   Para obtener información detallada acerca de la API de WebView2, vaya a [la especificación de WebView2][GithubMicrosoftUiXamlSpecsWebview2].  
    
## Introducción al equipo de Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: ../index.md "Introducción a microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegación | Microsoft Docs"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Configuraciones comunes de NuGet | Microsoft Docs"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Referencia del esquema del manifiesto del paquete para Windows 10 | Microsoft Docs"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Instalar sin usar el cuadro de diálogo Administrar extensiones: administrar extensiones para Visual Studio | Microsoft Docs"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurar el entorno de desarrollo: Windows UI Library 3.0 Preview 1 (mayo de 2020) | Microsoft Docs"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Documentación del Kit de herramientas de la comunidad de Windows | Microsoft Docs"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurar la aplicación de escritorio para el empaquetado MSIX en Visual Studio | Microsoft Docs"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Habilitar el dispositivo para el desarrollo | Microsoft Docs"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "Especificación de WebView2: microsoft/microsoft-ui-xaml-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: preguntas más frecuentes"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[NugetHome]: https://nuget.org "Inicio | Galería de NuGet"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Descargar dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Plantillas de proyecto de WinUI 3 | Visual Studio Marketplace"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador de WebView2" 

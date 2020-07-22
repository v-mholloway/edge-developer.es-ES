---
description: Hospedar contenido web en la aplicación WinUI con el control de WebView 2 de Microsoft Edge
title: Microsoft Edge WebView2 para aplicaciones WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, WinUI aplicaciones, WinUI, Edge, CoreWebView2, control del explorador, código HTML de Edge, introducción, .NET
ms.openlocfilehash: 76bf2e7dc0ef54da4203f186ce0356cfbcbc130d
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888634"
---
# <span data-ttu-id="b441e-104">Introducción a WebView2 en WinUI3 (vista previa)</span><span class="sxs-lookup"><span data-stu-id="b441e-104">Getting started with WebView2 in WinUI3 (Preview)</span></span>  

<span data-ttu-id="b441e-105">En este artículo, empiece a crear su primera aplicación de WebView2 con WinUI3 y obtenga información sobre las características principales de [Introducción a Microsoft Edge WebView2 (versión preliminar)][Webview2Index].</span><span class="sxs-lookup"><span data-stu-id="b441e-105">In this article, get started creating your first WebView2 app with WinUI3 and learn about the main features of [Introduction to Microsoft Edge WebView2 (Preview)][Webview2Index].</span></span>  <span data-ttu-id="b441e-106">Para obtener más información sobre las API individuales, consulta referencia de la [API][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="b441e-106">For more information on individual APIs, see [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="b441e-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b441e-107">Prerequisites</span></span>  

<span data-ttu-id="b441e-108">Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar con el siguiente artículo.</span><span class="sxs-lookup"><span data-stu-id="b441e-108">Ensure you install the following list of pre-requisites before proceeding with the following article.</span></span>  

*   <span data-ttu-id="b441e-109">Windows 10 versión 1803 \ (compilación 17134 \) o posterior.</span><span class="sxs-lookup"><span data-stu-id="b441e-109">Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="b441e-110">Para obtener más información, consulte [Windows Update: preguntas más frecuentes][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="b441e-110">For more information, see [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
*   <span data-ttu-id="b441e-111">[Canal Canarias de Microsoft Edge (cromo)][MicrosoftedgeinsiderDownload] en Windows 10, Windows 8,1 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b441e-111">[Microsoft Edge (Chromium) Canary channel][MicrosoftedgeinsiderDownload] on Windows 10, Windows 8.1, or Windows 7.</span></span>  
*   <span data-ttu-id="b441e-112">Visual Studio 2019, versión 16,7 Preview 1.</span><span class="sxs-lookup"><span data-stu-id="b441e-112">Visual Studio 2019, version 16.7 Preview 1.</span></span>  <span data-ttu-id="b441e-113">Para obtener más información, consulte [biblioteca de interfaces de usuario de Windows 3 Preview 2 (2020 de julio)][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="b441e-113">For more information, see [Windows UI Library 3 Preview 2 (July 2020)][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
*   <span data-ttu-id="b441e-114">Ambas versiones, [x64][WindowsDotnetcliBlobCoreSdk50100Preview4202681X86] y [x86][WindowsDotnetcliBlobCoreSdk50100Preview4202681X64] , de .net 5 Preview 4.</span><span class="sxs-lookup"><span data-stu-id="b441e-114">Both the [x64][WindowsDotnetcliBlobCoreSdk50100Preview4202681X86] and [x86][WindowsDotnetcliBlobCoreSdk50100Preview4202681X64] versions of .NET 5 Preview 4.</span></span>  
*   <span data-ttu-id="b441e-115">Extensión de [plantillas de proyecto WinUI 3][VisualstudioMarketplaceWinUiprojecttemplates] para Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="b441e-115">[WinUI 3 Project Templates][VisualstudioMarketplaceWinUiprojecttemplates] extension for Visual Studio 2019.</span></span>  
<span data-ttu-id="b441e-116">Asegúrate de [Habilitar el modo de desarrollador][WindowsUwpGetStartedEnableYourDeviceForDevelopment] para asegurarte de tener acceso a todas las características de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b441e-116">Ensure you [Enable Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment] to ensure you have access to all Visual Studio features.</span></span>  

## <span data-ttu-id="b441e-117">Paso 1: crear proyecto</span><span class="sxs-lookup"><span data-stu-id="b441e-117">Step 1 - Create Project</span></span>  

<span data-ttu-id="b441e-118">Empiece con un proyecto de escritorio básico que contenga una única ventana principal.</span><span class="sxs-lookup"><span data-stu-id="b441e-118">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="b441e-119">En Visual Studio, seleccione **crear un nuevo proyecto**.</span><span class="sxs-lookup"><span data-stu-id="b441e-119">In Visual Studio, select **Create a new project**.</span></span>  
1.  <span data-ttu-id="b441e-120">En la lista desplegable proyecto, seleccione **C#**, **Windows**y **WinUI** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b441e-120">In the project drop-down, select **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Cuadro de diálogo de creación de proyectos de Visual Studio para WinUI" lightbox="./media/winui-gettingstarted-selections.png":::
       <span data-ttu-id="b441e-122">Cuadro de diálogo de creación de proyectos de Visual Studio para WinUI</span><span class="sxs-lookup"><span data-stu-id="b441e-122">Visual studio project creation dialog for WinUI</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b441e-123">Seleccione **aplicación en blanco, empaquetada (WinUI en el escritorio)** y, a continuación, elija **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b441e-123">Choose **Blank App, Packaged (WinUI in Desktop)**, and then choose **Next**.</span></span>  
1.  <span data-ttu-id="b441e-124">Escriba un nombre de proyecto, elija otras opciones según sea necesario y, a continuación, seleccione **crear**.</span><span class="sxs-lookup"><span data-stu-id="b441e-124">Enter a project name, choose other options as needed, and then select **Create**.</span></span>  
1.  <span data-ttu-id="b441e-125">En **nuevo proyecto de plataforma universal de Windows**, seleccione los valores siguientes y, a continuación, elija **Aceptar**:</span><span class="sxs-lookup"><span data-stu-id="b441e-125">In **New Universal Windows Platform Project**, select the following values, and then choose **OK**:</span></span>  
    *   <span data-ttu-id="b441e-126">Versión de destino: **Windows 10, versión 1903 (compilación 18362)** o posterior.</span><span class="sxs-lookup"><span data-stu-id="b441e-126">Target version: **Windows 10, version 1903 (build 18362)** or later.</span></span>  
    *   <span data-ttu-id="b441e-127">Versión mínima: **Windows 10, versión 1803 (compilación 17134)**.</span><span class="sxs-lookup"><span data-stu-id="b441e-127">Minimum version: **Windows 10, version 1803 (build 17134)**.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="El nuevo cuadro de diálogo de proyecto de la plataforma universal de Windows con valores seleccionados para la versión de destino y la versión mínima." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="b441e-129">El nuevo cuadro de diálogo de proyecto de la plataforma universal de Windows con valores seleccionados para la versión de destino y la versión mínima.</span><span class="sxs-lookup"><span data-stu-id="b441e-129">The New Universal Windows Platform Project dialog with selected values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="b441e-130">En el explorador de soluciones, se generan dos proyectos.</span><span class="sxs-lookup"><span data-stu-id="b441e-130">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="b441e-131">**Nombre del proyecto (escritorio)**.</span><span class="sxs-lookup"><span data-stu-id="b441e-131">**Your project name(Desktop)**.</span></span> <span data-ttu-id="b441e-132">Este proyecto contiene el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b441e-132">This project contains the code for your app.</span></span>  <span data-ttu-id="b441e-133">**App.Xaml.CS** define una `Application` clase que representa la instancia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b441e-133">**App.xaml.cs** defines an`Application`class that represents your app instance.</span></span> <span data-ttu-id="b441e-134">**MainWindow.Xaml.CS** define una `MainWindow` clase que representa la ventana principal que muestra la instancia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b441e-134">**MainWindow.xaml.cs** defines a`MainWindow`class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="b441e-135">Estas clases se derivan de tipos en el `Microsoft.UI.Xaml` espacio de nombres WinUI.</span><span class="sxs-lookup"><span data-stu-id="b441e-135">These classes derive from types in the`Microsoft.UI.Xaml`namespace of WinUI.</span></span>  
    
    *   <span data-ttu-id="b441e-136">**Nombre del proyecto (paquete)**.</span><span class="sxs-lookup"><span data-stu-id="b441e-136">**Your project name(Package)**.</span></span>  <span data-ttu-id="b441e-137">Este proyecto es aWindows Projectthat de empaquetado de aplicaciones está configurado para generar la aplicación en un paquete de MSIX para la implementación.</span><span class="sxs-lookup"><span data-stu-id="b441e-137">This project is aWindows Application Packaging Projectthat is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="b441e-138">El proyecto contiene el paquete manifestfor la aplicación y es el proyecto de inicio de la solución de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b441e-138">The project contains thepackage manifestfor your app, and it is the startup project for your solution by default.</span></span> <span data-ttu-id="b441e-139">Para obtener más información, vea [configurar la aplicación de escritorio para el empaquetado de MSIX en Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] y [Referencia del esquema del manifiesto de paquete para Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="b441e-139">For more information, see [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>
    
1.  <span data-ttu-id="b441e-140">En el explorador de soluciones, Abra **MainWindow. Xaml** para mostrar el código.</span><span class="sxs-lookup"><span data-stu-id="b441e-140">In the Solution Explorer, open **MainWindow.xaml** to display the code.</span></span>  <span data-ttu-id="b441e-141">Seleccione `F5` para ejecutar el proyecto y mostrar una ventana con un botón.</span><span class="sxs-lookup"><span data-stu-id="b441e-141">Select `F5` to run your project and show a window with a button.</span></span>  
    
## <span data-ttu-id="b441e-142">Paso 2: agregar un control WebView2 a un proyecto</span><span class="sxs-lookup"><span data-stu-id="b441e-142">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="b441e-143">A continuación, agregue un control WebView2 al proyecto.</span><span class="sxs-lookup"><span data-stu-id="b441e-143">Next add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="b441e-144">Abra `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="b441e-144">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="b441e-145">Agrega el espacio de nombres XAML WebView2 insertando la siguiente línea dentro de la `<Window/>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="b441e-145">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="b441e-146">Confirme que el código `MainWindow.xaml` es similar al siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="b441e-146">Confirm that your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="b441e-147">Para agregar el control WebView2, reemplace las `<StackPanel>` etiquetas con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="b441e-147">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="b441e-148">La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="b441e-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="b441e-149">Abra `MainWindow.xaml.cs` y comente la línea siguiente.</span><span class="sxs-lookup"><span data-stu-id="b441e-149">Open `MainWindow.xaml.cs` and comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="b441e-150">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="b441e-150">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="b441e-151">Confirme que se muestra el control WebView2 [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="b441e-151">Confirm that your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Un control WebView2 que muestra el sitio de microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="b441e-153">Un control WebView2 que muestra el sitio de microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="b441e-153">A WebView2 control displaying the microsoft.com site.</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b441e-154">Paso 3: agregar controles de navegación</span><span class="sxs-lookup"><span data-stu-id="b441e-154">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="b441e-155">Permite a los usuarios controlar la página web que se muestra en el control WebView2 agregando una barra de direcciones a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b441e-155">Allow users to control the web page that is displayed in your WebView2 control by adding an address bar to your app.</span></span> 

1.  <span data-ttu-id="b441e-156">En **MainWindow. Xaml**, copie y pegue el siguiente fragmento de código dentro del `Grid` elemento que contiene el `WebView2` elemento.</span><span class="sxs-lookup"><span data-stu-id="b441e-156">In **MainWindow.xaml**, copy and paste the following code snippet inside the `Grid` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="b441e-157">Confirme que su `Grid` elemento de `MainWindow.xaml` es similar al siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="b441e-157">Confirm that your `Grid` element of `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="b441e-158">En **MainWindow.Xaml.CS**, copie el siguiente fragmento de código en `myButton_Click` , que navega por el control WebView2 a la dirección URL escrita en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="b441e-158">In **MainWindow.xaml.cs**, copy the following code snippet to `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="b441e-159">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="b441e-159">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="b441e-160">Escriba una nueva dirección URL en la barra de direcciones y, después, seleccione **ir**.</span><span class="sxs-lookup"><span data-stu-id="b441e-160">Enter a new URL in the address bar, and then select **Go**.</span></span>  <span data-ttu-id="b441e-161">Por ejemplo, escriba `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="b441e-161">For example, enter `https://www.bing.com`.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="b441e-162">Asegúrate de usar direcciones URL completas en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="b441e-162">Ensure you use complete URLs in the address bar.</span></span> `ArgumentException` <span data-ttu-id="b441e-163">las excepciones se inician si la dirección URL no comienza con `http://` o `https://` .</span><span class="sxs-lookup"><span data-stu-id="b441e-163">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="b441e-165">Bing.com</span><span class="sxs-lookup"><span data-stu-id="b441e-165">Bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b441e-166">Paso 4: eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="b441e-166">Step 4 - Navigation events</span></span>  

<span data-ttu-id="b441e-167">Las aplicaciones que hospedan controles WebView2 escuchan los siguientes eventos provocados por los controles de WebView2 durante la navegación por la Página Web.</span><span class="sxs-lookup"><span data-stu-id="b441e-167">Applications that host WebView2 controls listen for the following events that are raised by WebView2 controls during web page navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  
> [!NOTE]
> <span data-ttu-id="b441e-168">Las redirecciones HTTP generan varios `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="b441e-168">HTTP redirects raise multiple `NavigationStarting` events.</span></span>  
<span data-ttu-id="b441e-169">Para obtener más información, vea [eventos de navegación][Webviews2ReferenceWin3209488Icorewebview2NavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="b441e-169">For more information, see [Navigation Events][Webviews2ReferenceWin3209488Icorewebview2NavigationEvents].</span></span>  

<span data-ttu-id="b441e-170">Cuando se producen errores, se producen los eventos siguientes y puede navegar a una página de error.</span><span class="sxs-lookup"><span data-stu-id="b441e-170">When errors occur, the following events are raised and may navigate to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
    

<span data-ttu-id="b441e-171">Para obtener un ejemplo de cómo usar los eventos, registra un controlador para `NavigationStarting` que cancele todas las solicitudes que no usen https.</span><span class="sxs-lookup"><span data-stu-id="b441e-171">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span> <span data-ttu-id="b441e-172">En `MainWindow.xaml.cs` , modifique el constructor para registrarlo `EnsureHttps` y agregue la `EnsureHttps` función para que coincida con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="b441e-172">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  


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

<span data-ttu-id="b441e-173">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="b441e-173">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="b441e-174">Confirme que la navegación está bloqueada en sitios HTTP y que se permite en sitios HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b441e-174">Confirm that navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="b441e-175">Paso 5: scripting</span><span class="sxs-lookup"><span data-stu-id="b441e-175">Step 5 - Scripting</span></span>  

<span data-ttu-id="b441e-176">Las aplicaciones de host pueden inyectar código JavaScript en controles WebView2 en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b441e-176">Host applications may inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="b441e-177">El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a los fotogramas secundarios hasta que se quite el JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b441e-177">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="b441e-178">El código JavaScript insertado se ejecuta después de la creación del objeto global y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="b441e-178">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="b441e-179">Como ejemplo, agregar scripts envía una alerta cuando un usuario navega a sitios que no son HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b441e-179">As an example, add scripts send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="b441e-180">Modifique la `EnsureHttps` función para insertar un script en el contenido web con [ExecuteScriptAsync][Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="b441e-180">Modify the `EnsureHttps` function to inject a script into the web content using [ExecuteScriptAsync][Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="b441e-181">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="b441e-181">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="b441e-182">Confirme que su aplicación muestra una alerta cuando se desplaza a un sitio que no usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b441e-182">Confirm that your application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Control WebView2 que muestra un cuadro de diálogo de alerta" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="b441e-184">Control WebView2 que muestra un cuadro de diálogo de alerta</span><span class="sxs-lookup"><span data-stu-id="b441e-184">WebView2 control showing an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="b441e-185">Enhorabuena, has creado tu primera aplicación de WebView2.</span><span class="sxs-lookup"><span data-stu-id="b441e-185">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="b441e-186">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="b441e-186">Next Steps</span></span>  

<span data-ttu-id="b441e-187">Nuestro equipo está actualmente generando más API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="b441e-187">Our team is currently building more WebView2 APIs.</span></span>  <span data-ttu-id="b441e-188">Para obtener más información sobre el estado actual de las API de WebView2, consulte la [especificación WebView2][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="b441e-188">For more information on the current state of WebView2 APIs, see the [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

> [!NOTE]
> <span data-ttu-id="b441e-189">Es posible que el objeto WinRT CoreWebView2 no esté disponible en el momento en que se envían las API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="b441e-189">The WinRT CoreWebView2 object may not be available at the time the WebView2 APIs ship.</span></span> <span data-ttu-id="b441e-190">Para conocer las API que están disponibles para los controles de WebView2, consulta la [especificación de WebView2][GithubMicrosoftUiXamlSpecsWebview2] para obtener una lista de las API que están disponibles.</span><span class="sxs-lookup"><span data-stu-id="b441e-190">To understand which APIs are available to WebView2 controls, see [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span> 

<span data-ttu-id="b441e-191">Para obtener más información sobre las capacidades de WebView2, consulte [WebView2 conceptos y guías de procedimientos][Webview2IndexNextSteps], y el [repositorio de ejemplos de WebView2][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="b441e-191">For more information about WebView2 capabilities, see [WebView2 Concepts and How-To guides][Webview2IndexNextSteps], and the [WebView2 samples repo][GithubMicrosoftedgeWebview2samplesMain].</span></span>  

## <span data-ttu-id="b441e-192">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b441e-192">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="b441e-193">Ayuda a crear una experiencia WebView2 más rica compartiendo tus comentarios.</span><span class="sxs-lookup"><span data-stu-id="b441e-193">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="b441e-194">Visite el [repositorio de comentarios][GithubMicrosoftedgeWebviewfeedback] de Microsoft Edge WebView para enviar solicitudes de características o informes de errores, o para buscar problemas conocidos.</span><span class="sxs-lookup"><span data-stu-id="b441e-194">Visit the Microsoft Edge WebView [feedback repo][GithubMicrosoftedgeWebviewfeedback] to submit feature requests or bug reports, or to search for known issues.</span></span>  

<!-- links -->  

[Webview2Index]: ../index.md "Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webviews2ReferenceWin3209488Icorewebview2NavigationEvents]: ../reference/win32/0-9-488/icorewebview2.md#navigation-events "Eventos de navegación-interfaz ICoreWebView2 | Microsoft docs"  
[Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync]: ../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync "ExecuteScriptAsync-Microsoft. Web. WebView2. WPF. WebView2 (clase) | Microsoft docs"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Referencia del esquema del manifiesto del paquete para Windows 10 | Microsoft docs"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurar el entorno de desarrollo: biblioteca de interfaces de usuario de Windows 3,0 Preview 1 (mayo de 2020) | Microsoft docs"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurar la aplicación de escritorio para el empaquetado de MSIX en Visual Studio | Microsoft docs"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Habilitar el dispositivo para el desarrollo | Microsoft docs"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 espec-Microsoft/Microsoft-UI-XAML-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Técnico"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: preguntas más frecuentes"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar los canales de Insider de Microsoft Edge"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Descargar dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe "dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceWinUiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Plantillas de proyecto WinUI 3"  

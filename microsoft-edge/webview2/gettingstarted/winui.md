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
# <span data-ttu-id="03768-104">Introducción a WebView2 en WinUI 3 (vista previa)</span><span class="sxs-lookup"><span data-stu-id="03768-104">Getting started with WebView2 in WinUI 3 (Preview)</span></span>  

<span data-ttu-id="03768-105">En este artículo, aprenderá a crear su primera aplicación de WebView2 y sobre las características principales de [Introducción a Microsoft Edge WebView2 (versión preliminar)][Webview2Index].</span><span class="sxs-lookup"><span data-stu-id="03768-105">In this article, learn how to create your first WebView2 app and about the main features of [Introduction to Microsoft Edge WebView2 (Preview)][Webview2Index].</span></span>  <span data-ttu-id="03768-106">Tu primera WebView2 aplicación usa WinUI3.</span><span class="sxs-lookup"><span data-stu-id="03768-106">Your first WebView2 app uses WinUI3.</span></span>  <span data-ttu-id="03768-107">Para obtener más información sobre las API individuales, vaya a referencia de la [API][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="03768-107">For more information on individual APIs, navigate to [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="03768-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03768-108">Prerequisites</span></span>  

<span data-ttu-id="03768-109">Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar con el siguiente artículo.</span><span class="sxs-lookup"><span data-stu-id="03768-109">Ensure you install the following list of pre-requisites before proceeding with the following article.</span></span>  

1.  <span data-ttu-id="03768-110">Windows 10 versión 1803 \ (compilación 17134 \) o posterior.</span><span class="sxs-lookup"><span data-stu-id="03768-110">Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="03768-111">Para obtener más información, vaya a [Windows Update: preguntas más frecuentes][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="03768-111">For more information, navigate to [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
1.  <span data-ttu-id="03768-112">[Canal Canarias de Microsoft Edge (cromo)][MicrosoftedgeinsiderDownload] en Windows 10, Windows 8,1 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="03768-112">[Microsoft Edge (Chromium) Canary channel][MicrosoftedgeinsiderDownload] on Windows 10, Windows 8.1, or Windows 7.</span></span>  
1.  <span data-ttu-id="03768-113">Visual Studio 2019, versión 16,9 Preview.</span><span class="sxs-lookup"><span data-stu-id="03768-113">Visual Studio 2019, version 16.9 Preview.</span></span>  <span data-ttu-id="03768-114">Para obtener más información, vaya a la [biblioteca de interfaces de usuario de Windows 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="03768-114">For more information, navigate to [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
    
    <span data-ttu-id="03768-115">Incluya las siguientes cargas de trabajo al instalar Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="03768-115">Include the following workloads when you install Visual Studio.</span></span>  
    
    *   <span data-ttu-id="03768-116">Desarrollo de escritorio .NET \ (el instalador también instala .NET 5 \)</span><span class="sxs-lookup"><span data-stu-id="03768-116">.NET Desktop Development \(the installer also installs .NET 5\)</span></span>  
    *   <span data-ttu-id="03768-117">Desarrollo de la plataforma universal de Windows</span><span class="sxs-lookup"><span data-stu-id="03768-117">Universal Windows Platform development</span></span>  
        
    <span data-ttu-id="03768-118">Para crear aplicaciones de C++, también debe incluir las siguientes cargas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="03768-118">To build C++ apps, you must also include the following workloads.</span></span>  
    
    *   <span data-ttu-id="03768-119">Desarrollo de escritorio con C++</span><span class="sxs-lookup"><span data-stu-id="03768-119">Desktop development with C++</span></span>  
    *   <span data-ttu-id="03768-120">El componente opcional de las herramientas de la plataforma universal de Windows de C++ (v142) para la carga de trabajo de la plataforma universal de Windows.</span><span class="sxs-lookup"><span data-stu-id="03768-120">The C++ (v142) Universal Windows Platform tools optional component for the Universal Windows Platform workload.</span></span>  <span data-ttu-id="03768-121">Para obtener más información, vaya a detalles de instalación en la sección desarrollo de la plataforma universal de Windows, en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="03768-121">For more information,  navigate to Installation Details under the Universal Windows Platform development section, on the right pane.</span></span>  
        
1.  <span data-ttu-id="03768-122">Asegúrese de que su sistema tiene habilitado un origen de paquete NuGet para [Nuget.org][NugetHome].  Para obtener más información, vaya a [configuraciones comunes de NuGet][NugetConsumePackagesConfiguringNugetBehavior] y a [Windows Community Toolkit][WindowsCommunitytoolkit].</span><span class="sxs-lookup"><span data-stu-id="03768-122">Make sure your system has a NuGet package source enabled for [nuget.org][NugetHome].  For more information, navigate to [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span></span>  
1.  <span data-ttu-id="03768-123">Descargue e instale el [paquete VSIX de la versión preliminar de WinUI 3][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span><span class="sxs-lookup"><span data-stu-id="03768-123">Download and install the [WinUI 3 Preview 3 VSIX package][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span></span>  <span data-ttu-id="03768-124">El instalador agrega las plantillas de proyecto WinUI 3 y el paquete NuGet que contiene las bibliotecas WinUI 3 a Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="03768-124">The installer adds both the WinUI 3 project templates and the NuGet package containing the WinUI 3 libraries to Visual Studio 2019.</span></span>  
    
    <span data-ttu-id="03768-125">Para obtener instrucciones sobre cómo agregar el paquete VSIX a Visual Studio, vaya a [Buscar y usar las extensiones de Visual Studio][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span><span class="sxs-lookup"><span data-stu-id="03768-125">For instructions on how to add the VSIX package to Visual Studio, navigate to [Finding and Using Visual Studio Extensions][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span></span>
    
1.  <span data-ttu-id="03768-126">Habilite el [modo de desarrollador][WindowsUwpGetStartedEnableYourDeviceForDevelopment] para asegurarse de que tiene acceso a todas las características de Visual Studio específicas del desarrollador.</span><span class="sxs-lookup"><span data-stu-id="03768-126">Enable [Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment] to ensure you have access to all developer-specific Visual Studio features.</span></span>  
    
## <span data-ttu-id="03768-127">Paso 1: crear proyecto</span><span class="sxs-lookup"><span data-stu-id="03768-127">Step 1 - Create Project</span></span>  

<span data-ttu-id="03768-128">Empiece con un proyecto de escritorio básico que contenga una única ventana principal.</span><span class="sxs-lookup"><span data-stu-id="03768-128">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="03768-129">En Visual Studio, elija **crear un nuevo proyecto**.</span><span class="sxs-lookup"><span data-stu-id="03768-129">In Visual Studio, choose **Create a new project**.</span></span>  
1.  <span data-ttu-id="03768-130">En la lista desplegable proyecto, elija **C#**, **Windows**y **WinUI** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="03768-130">In the project drop-down, choose **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Crear un nuevo proyecto WinUI con Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        <span data-ttu-id="03768-132">Crear un nuevo proyecto WinUI con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="03768-132">Create a new WinUI project using Visual Studio</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="03768-133">Seleccione **aplicación en blanco, empaquetada (WinUI en el escritorio)** y, a continuación, elija **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="03768-133">Choose **Blank App, Packaged (WinUI in Desktop)**, and then choose **Next**.</span></span>  
1.  <span data-ttu-id="03768-134">Escriba un nombre de proyecto, elija otras opciones según sea necesario y, a continuación, elija **crear**.</span><span class="sxs-lookup"><span data-stu-id="03768-134">Enter a project name, choose other options as needed, and then choose **Create**.</span></span>  
1.  <span data-ttu-id="03768-135">En **nuevo proyecto de plataforma universal de Windows**, elija los valores siguientes y, a continuación, elija **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="03768-135">In **New Universal Windows Platform Project**, choose the following values, and then choose **OK**.</span></span>  
    *   <span data-ttu-id="03768-136">**Versión de destino**:  **Windows 10, versión 1903 (compilación 18362)** o posterior</span><span class="sxs-lookup"><span data-stu-id="03768-136">**Target version**:  **Windows 10, version 1903 (build 18362)** or later</span></span>  
    *   <span data-ttu-id="03768-137">**Versión mínima**:  **Windows 10, versión 1803 (compilación 17134)**</span><span class="sxs-lookup"><span data-stu-id="03768-137">**Minimum version**:  **Windows 10, version 1803 (build 17134)**</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="El nuevo cuadro de diálogo de proyecto de la plataforma universal de Windows con los valores elegidos para la versión de destino y la versión mínima." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="03768-139">El nuevo cuadro de diálogo de proyecto de la plataforma universal de Windows con los valores elegidos para la versión de destino y la versión mínima.</span><span class="sxs-lookup"><span data-stu-id="03768-139">The New Universal Windows Platform Project dialog with chosen values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="03768-140">En el explorador de soluciones, se generan dos proyectos.</span><span class="sxs-lookup"><span data-stu-id="03768-140">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="03768-141">**Nombre del proyecto (escritorio)**.</span><span class="sxs-lookup"><span data-stu-id="03768-141">**Your project name (Desktop)**.</span></span>  <span data-ttu-id="03768-142">Este proyecto contiene el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="03768-142">This project contains the code for your app.</span></span>  <span data-ttu-id="03768-143">**App.Xaml.CS** define una `Application` clase que representa la instancia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="03768-143">**App.xaml.cs** defines an `Application` class that represents your app instance.</span></span>  <span data-ttu-id="03768-144">**MainWindow.Xaml.CS** define una `MainWindow` clase que representa la ventana principal que muestra la instancia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="03768-144">**MainWindow.xaml.cs** defines a `MainWindow` class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="03768-145">Estas clases se derivan de tipos en el `Microsoft.UI.Xaml` espacio de nombres WinUI.</span><span class="sxs-lookup"><span data-stu-id="03768-145">These classes derive from types in the `Microsoft.UI.Xaml` namespace of WinUI.</span></span>  
    
    *   <span data-ttu-id="03768-146">**Nombre del proyecto (paquete)**.</span><span class="sxs-lookup"><span data-stu-id="03768-146">**Your project name (Package)**.</span></span>  <span data-ttu-id="03768-147">Este proyecto es un proyecto de empaquetado de aplicaciones para Windows que está configurado para generar la aplicación en un paquete MSIX para su implementación.</span><span class="sxs-lookup"><span data-stu-id="03768-147">This project is a Windows Application Packaging Project that is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="03768-148">El proyecto contiene el manifiesto del paquete de la aplicación y es el proyecto de inicio de la solución de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="03768-148">The project contains the package manifest for your app, and it is the startup project for your solution by default.</span></span>  <span data-ttu-id="03768-149">Para obtener más información, vaya a [configurar la aplicación de escritorio para el empaquetado de MSIX en Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] y [Referencia del esquema del manifiesto de paquete para Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="03768-149">For more information, navigate to [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>
    
1.  <span data-ttu-id="03768-150">En el explorador de soluciones, para mostrar el código, Abra `MainWindow.xaml` archivo.</span><span class="sxs-lookup"><span data-stu-id="03768-150">In the Solution Explorer, to display the code, open `MainWindow.xaml` file.</span></span>  <span data-ttu-id="03768-151">Seleccione `F5` para ejecutar el proyecto y mostrar una ventana con un botón.</span><span class="sxs-lookup"><span data-stu-id="03768-151">Select `F5` to run your project and show a window with a button.</span></span>  
    
## <span data-ttu-id="03768-152">Paso 2: agregar un control WebView2 a un proyecto</span><span class="sxs-lookup"><span data-stu-id="03768-152">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="03768-153">A continuación, agregue un control WebView2 al proyecto.</span><span class="sxs-lookup"><span data-stu-id="03768-153">Next add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="03768-154">Abra `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="03768-154">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="03768-155">Agrega el espacio de nombres XAML WebView2 insertando la siguiente línea dentro de la `<Window/>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="03768-155">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="03768-156">Confirme que el código `MainWindow.xaml` es similar al siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="03768-156">Confirm that your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="03768-157">Para agregar el control WebView2, reemplace las `<StackPanel>` etiquetas con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="03768-157">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="03768-158">La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="03768-158">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="03768-159">Abra `MainWindow.xaml.cs` y comente la línea siguiente.</span><span class="sxs-lookup"><span data-stu-id="03768-159">Open `MainWindow.xaml.cs` and comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="03768-160">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="03768-160">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="03768-161">Confirme que se muestra el control WebView2 [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="03768-161">Confirm that your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Un control WebView2 que muestra el sitio de microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="03768-163">Un control WebView2 que muestra el sitio de microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="03768-163">A WebView2 control displaying the microsoft.com site.</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="03768-164">Paso 3: agregar controles de navegación</span><span class="sxs-lookup"><span data-stu-id="03768-164">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="03768-165">Permite a los usuarios controlar la página web que se muestra en el control WebView2 agregando una barra de direcciones a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="03768-165">Allow users to control the web page that is displayed in your WebView2 control by adding an address bar to your app.</span></span>  

1.  <span data-ttu-id="03768-166">En `MainWindow.xaml` , copie y pegue el siguiente fragmento de código dentro del `Grid` elemento que contiene el `WebView2` elemento.</span><span class="sxs-lookup"><span data-stu-id="03768-166">In `MainWindow.xaml`, copy and paste the following code snippet inside the `Grid` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="03768-167">Confirme que su `Grid` elemento de `MainWindow.xaml` es similar al siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="03768-167">Confirm that your `Grid` element of `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="03768-168">En `MainWindow.xaml.cs` , copie el siguiente fragmento de código en `myButton_Click` , que navega por el control WebView2 a la dirección URL que se escribe en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="03768-168">In `MainWindow.xaml.cs`, copy the following code snippet to `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="03768-169">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="03768-169">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="03768-170">Escriba una nueva dirección URL en la barra de direcciones y, después, elija **ir**.</span><span class="sxs-lookup"><span data-stu-id="03768-170">Enter a new URL in the address bar, and then choose **Go**.</span></span>  <span data-ttu-id="03768-171">Por ejemplo, escriba `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="03768-171">For example, enter `https://www.bing.com`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="03768-172">Asegúrate de usar direcciones URL completas en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="03768-172">Ensure you use complete URLs in the address bar.</span></span>  `ArgumentException` <span data-ttu-id="03768-173">las excepciones se inician si la dirección URL no comienza con `http://` o `https://` .</span><span class="sxs-lookup"><span data-stu-id="03768-173">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="03768-175">Bing.com</span><span class="sxs-lookup"><span data-stu-id="03768-175">Bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="03768-176">Paso 4: eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="03768-176">Step 4 - Navigation events</span></span>  

<span data-ttu-id="03768-177">Las aplicaciones que hospedan controles WebView2 escuchan los siguientes eventos provocados por los controles de WebView2 durante la navegación por la Página Web.</span><span class="sxs-lookup"><span data-stu-id="03768-177">Applications that host WebView2 controls listen for the following events that are raised by WebView2 controls during web page navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="03768-178">Las redirecciones HTTP generan varios `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="03768-178">HTTP redirects raise multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="03768-179">Para obtener más información, vaya a [eventos de navegación][Webviews2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="03768-179">For more information, navigate to [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="03768-180">Cuando se producen errores, se producen los eventos siguientes y puede navegar a una página de error.</span><span class="sxs-lookup"><span data-stu-id="03768-180">When errors occur, the following events are raised and may navigate to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="03768-181">Para obtener un ejemplo de cómo usar los eventos, registra un controlador para `NavigationStarting` que cancele cualquier solicitud que no use HTTPS.</span><span class="sxs-lookup"><span data-stu-id="03768-181">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any request that does not use HTTPS.</span></span>  <span data-ttu-id="03768-182">En `MainWindow.xaml.cs` , modifique el constructor para registrarlo `EnsureHttps` y agregue la `EnsureHttps` función para que coincida con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="03768-182">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="03768-183">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="03768-183">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="03768-184">Confirme que la navegación está bloqueada en sitios HTTP y que se permite en sitios HTTPS.</span><span class="sxs-lookup"><span data-stu-id="03768-184">Confirm that navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="03768-185">Paso 5: scripting</span><span class="sxs-lookup"><span data-stu-id="03768-185">Step 5 - Scripting</span></span>  

<span data-ttu-id="03768-186">Las aplicaciones de host pueden inyectar código JavaScript en controles WebView2 en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="03768-186">Host applications may inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="03768-187">El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a cualquier fotograma secundario hasta que se quite el JavaScript.</span><span class="sxs-lookup"><span data-stu-id="03768-187">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="03768-188">El JavaScript insertado se ejecuta con intervalos específicos.</span><span class="sxs-lookup"><span data-stu-id="03768-188">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="03768-189">Ejecútelo después de crear el objeto global.</span><span class="sxs-lookup"><span data-stu-id="03768-189">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="03768-190">Ejecútelo antes de ejecutar cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="03768-190">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="03768-191">Como ejemplo, agregar scripts envía una alerta cuando un usuario navega a sitios que no son HTTPS.</span><span class="sxs-lookup"><span data-stu-id="03768-191">As an example, add scripts send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="03768-192">Modifique la `EnsureHttps` función para insertar un script en el contenido web que usa [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="03768-192">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="03768-193">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="03768-193">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="03768-194">Confirme que su aplicación muestra una alerta cuando se desplaza a un sitio que no usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="03768-194">Confirm that your application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Control WebView2 que muestra un cuadro de diálogo de alerta" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="03768-196">Control WebView2 que muestra un cuadro de diálogo de alerta</span><span class="sxs-lookup"><span data-stu-id="03768-196">WebView2 control showing an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="03768-197">Enhorabuena, has creado tu primera aplicación de WebView2.</span><span class="sxs-lookup"><span data-stu-id="03768-197">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="03768-198">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="03768-198">Next Steps</span></span>  

<span data-ttu-id="03768-199">Nuestro equipo está actualmente generando más API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="03768-199">Our team is currently building more WebView2 APIs.</span></span>  <span data-ttu-id="03768-200">Para obtener más información sobre el estado actual de las API de WebView2, vaya a la [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="03768-200">For more information on the current state of WebView2 APIs, navigate to the [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

> [!NOTE]
> <span data-ttu-id="03768-201">Es posible que el objeto WinRT CoreWebView2 no esté disponible en el momento en que se envían las API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="03768-201">The WinRT CoreWebView2 object may not be available at the time the WebView2 APIs ship.</span></span>  <span data-ttu-id="03768-202">Para comprender las API que están disponibles para los controles de WebView2, vaya a [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] para obtener una lista de las API que están disponibles.</span><span class="sxs-lookup"><span data-stu-id="03768-202">To understand which APIs are available to WebView2 controls, navigate to [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span>  

<span data-ttu-id="03768-203">Para obtener más información sobre las capacidades de WebView2, vaya a [WebView2 conceptos y guías de How-To][Webview2IndexNextSteps] y al [repositorio de ejemplos de WebView2][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="03768-203">For more information about WebView2 capabilities, navigate to [WebView2 Concepts and How-To guides][Webview2IndexNextSteps] and the [WebView2 samples repo][GithubMicrosoftedgeWebview2samplesMain].</span></span>  

## <span data-ttu-id="03768-204">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="03768-204">Getting in touch with the Microsoft Edge WebView team</span></span>  

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

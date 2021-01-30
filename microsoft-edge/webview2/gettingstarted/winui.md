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
# <span data-ttu-id="f9ed4-104">Introducción a WebView2 en WinUI 3 (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="f9ed4-104">Getting started with WebView2 in WinUI 3 (Preview)</span></span>  

<span data-ttu-id="f9ed4-105">En este artículo, empieza a crear tu primera aplicación WebView2 y obtén información sobre las características principales [de WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="f9ed4-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="f9ed4-106">La primera aplicación WebView2 usa WinUI3.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-106">Your first WebView2 app uses WinUI3.</span></span>  <span data-ttu-id="f9ed4-107">Para obtener más información sobre las API individuales, vaya a [la referencia de la API.][GithubMicrosoftUiXamlSpecsWebview2]</span><span class="sxs-lookup"><span data-stu-id="f9ed4-107">For more information on individual APIs, navigate to [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="f9ed4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f9ed4-108">Prerequisites</span></span>  

<span data-ttu-id="f9ed4-109">Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-109">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="f9ed4-110">[WebView2 Runtime][Webview2Installer] o cualquier canal no estable de [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado en Windows 10 versión 1803 \(compilación 17134\) o posterior.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-110">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="f9ed4-111">Para obtener más información sobre Windows 10, ve a [Windows Update: Preguntas más frecuentes.][MicrosoftSupport12373]</span><span class="sxs-lookup"><span data-stu-id="f9ed4-111">For more information about Windows 10, navigate to [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f9ed4-112">El equipo de WebView recomienda usar el canal Canary y la versión mínima necesaria es 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-112">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="f9ed4-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, versión 16.9 Preview.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, version 16.9 Preview.</span></span>  <span data-ttu-id="f9ed4-114">Para obtener más información, ve a la Biblioteca [de interfaz de usuario de Windows 3 Preview 3.][WindowsAppsWinui3ConfigureYourDevEnvironment]</span><span class="sxs-lookup"><span data-stu-id="f9ed4-114">For more information, navigate to [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
    
    *   <span data-ttu-id="f9ed4-115">Incluya las siguientes cargas de trabajo al instalar Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-115">Include the following workloads when you install Visual Studio.</span></span>  
        *   <span data-ttu-id="f9ed4-116">Desarrollo de escritorio .NET \(el instalador también instala .NET 5\)</span><span class="sxs-lookup"><span data-stu-id="f9ed4-116">.NET Desktop Development \(the installer also installs .NET 5\)</span></span>  
        *   <span data-ttu-id="f9ed4-117">Desarrollo de la Plataforma universal de Windows</span><span class="sxs-lookup"><span data-stu-id="f9ed4-117">Universal Windows Platform development</span></span>  
    *   <span data-ttu-id="f9ed4-118">Para crear aplicaciones de C++, también debes incluir las siguientes cargas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-118">To build C++ apps, you must also include the following workloads.</span></span>  
        *   <span data-ttu-id="f9ed4-119">Desarrollo de escritorio con C++</span><span class="sxs-lookup"><span data-stu-id="f9ed4-119">Desktop development with C++</span></span>  
        *   <span data-ttu-id="f9ed4-120">El componente opcional de las herramientas de la Plataforma universal de Windows C++ \(v142\) para la carga de trabajo de la Plataforma universal de Windows.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-120">The C++ \(v142\) Universal Windows Platform tools optional component for the Universal Windows Platform workload.</span></span>  <span data-ttu-id="f9ed4-121">Para obtener más información, ve a **Detalles de instalación** en la sección desarrollo de la Plataforma universal de **Windows,** en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-121">For more information,  navigate to **Installation Details** under the **Universal Windows Platform development** section, on the right pane.</span></span>  
        
## <span data-ttu-id="f9ed4-122">Paso 0: configuración Visual Studio configuración</span><span class="sxs-lookup"><span data-stu-id="f9ed4-122">Step 0 - Visual Studio settings</span></span>  

1.  <span data-ttu-id="f9ed4-123">Asegúrese de que el sistema tiene un origen de paquete NuGet habilitado para [nuget.org][NugetHome].  Para obtener más información, vaya a [configuraciones de NuGet comunes][NugetConsumePackagesConfiguringNugetBehavior] y [a Windows Community Toolkit.][WindowsCommunitytoolkit]</span><span class="sxs-lookup"><span data-stu-id="f9ed4-123">Ensure your system has a NuGet package source enabled for [nuget.org][NugetHome].  For more information, navigate to [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span></span>  
1.  <span data-ttu-id="f9ed4-124">Descarga e instala el paquete [VSIX de WinUI 3 Preview 3.][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]</span><span class="sxs-lookup"><span data-stu-id="f9ed4-124">Download and install the [WinUI 3 Preview 3 VSIX package][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span></span>  <span data-ttu-id="f9ed4-125">El instalador agrega las plantillas de proyecto WinUI 3 y el paquete NuGet que contiene las bibliotecas de WinUI 3 a Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-125">The installer adds both the WinUI 3 project templates and the NuGet package containing the WinUI 3 libraries to Visual Studio 2019.</span></span>  
    
    <span data-ttu-id="f9ed4-126">Para obtener instrucciones sobre cómo agregar el paquete a Visual Studio, vaya a Buscar y `VSIX` [usar Visual Studio extensiones.][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]</span><span class="sxs-lookup"><span data-stu-id="f9ed4-126">For instructions on how to add the `VSIX` package to Visual Studio, navigate to [Finding and Using Visual Studio Extensions][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span></span>
    
1.  <span data-ttu-id="f9ed4-127">Para obtener acceso a todas las características de Visual Studio específicas del desarrollador, activa el [modo de desarrollador.][WindowsUwpGetStartedEnableYourDeviceForDevelopment]</span><span class="sxs-lookup"><span data-stu-id="f9ed4-127">To access all developer-specific Visual Studio features, turn on [Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment].</span></span>  
    
## <span data-ttu-id="f9ed4-128">Paso 1: Crear proyecto</span><span class="sxs-lookup"><span data-stu-id="f9ed4-128">Step 1 - Create Project</span></span>  

<span data-ttu-id="f9ed4-129">Comience con un proyecto de escritorio básico que contenga una sola ventana principal.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-129">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="f9ed4-130">En Visual Studio, elija **Crear un nuevo proyecto.**</span><span class="sxs-lookup"><span data-stu-id="f9ed4-130">In Visual Studio, choose **Create a new project**.</span></span>  
1.  <span data-ttu-id="f9ed4-131">En la lista desplegable del proyecto, elija **C#**, **Windows**y **WinUI** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-131">In the project drop-down, choose **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Crear un nuevo proyecto de WinUI con Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        <span data-ttu-id="f9ed4-133">Crear un nuevo proyecto de WinUI con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f9ed4-133">Create a new WinUI project using Visual Studio</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="f9ed4-134">Choose **Blank App, Packaged (WinUI in Desktop)**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-134">Choose **Blank App, Packaged (WinUI in Desktop)** > **Next**.</span></span>  
1.  <span data-ttu-id="f9ed4-135">Escriba un nombre de proyecto.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-135">Enter a project name.</span></span>
1.  <span data-ttu-id="f9ed4-136">Elija las opciones según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-136">Choose options as needed.</span></span>  
1.  <span data-ttu-id="f9ed4-137">Elija **Crear**.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-137">Choose **Create**.</span></span>  
1.  <span data-ttu-id="f9ed4-138">En **Nuevo proyecto de plataforma universal de Windows,** elija los siguientes valores y, a continuación, elija **Aceptar.**</span><span class="sxs-lookup"><span data-stu-id="f9ed4-138">In **New Universal Windows Platform Project**, choose the following values, and then choose **OK**.</span></span>  
    *   <span data-ttu-id="f9ed4-139">**Versión de**destino:  **Windows 10, versión 1903 (compilación 18362)** o posterior</span><span class="sxs-lookup"><span data-stu-id="f9ed4-139">**Target version**:  **Windows 10, version 1903 (build 18362)** or later</span></span>  
    *   <span data-ttu-id="f9ed4-140">**Versión mínima:**  **Windows 10, versión 1803 (compilación 17134)**</span><span class="sxs-lookup"><span data-stu-id="f9ed4-140">**Minimum version**:  **Windows 10, version 1803 (build 17134)**</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Cuadro de diálogo Nuevo proyecto de plataforma universal de Windows con los valores elegidos para la versión de destino y la versión mínima." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="f9ed4-142">Cuadro de diálogo Nuevo proyecto de plataforma universal de Windows con los valores elegidos para la versión de destino y la versión mínima.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-142">The New Universal Windows Platform Project dialog with chosen values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="f9ed4-143">En el Explorador de soluciones, se generan dos proyectos.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-143">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="f9ed4-144">**El nombre del proyecto (escritorio).**</span><span class="sxs-lookup"><span data-stu-id="f9ed4-144">**Your project name (Desktop)**.</span></span>  <span data-ttu-id="f9ed4-145">El proyecto de escritorio contiene el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-145">The Desktop project contains the code for your app.</span></span>  <span data-ttu-id="f9ed4-146">El `App.xaml.cs` archivo define una clase que representa la instancia de la `Application` aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-146">The `App.xaml.cs` file defines an `Application` class that represents your app instance.</span></span>  <span data-ttu-id="f9ed4-147">El `MainWindow.xaml.cs` archivo define una clase que representa la ventana principal que muestra la instancia de la `MainWindow` aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-147">The `MainWindow.xaml.cs` file defines a `MainWindow` class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="f9ed4-148">Las clases derivan de tipos en el `Microsoft.UI.Xaml` espacio de nombres de WinUI.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-148">The classes derive from types in the `Microsoft.UI.Xaml` namespace of WinUI.</span></span>  
    *   <span data-ttu-id="f9ed4-149">**El nombre del proyecto (paquete).**</span><span class="sxs-lookup"><span data-stu-id="f9ed4-149">**Your project name (Package)**.</span></span>  <span data-ttu-id="f9ed4-150">El proyecto de paquete es un proyecto de empaquetado de aplicaciones de Windows que está configurado para compilar la aplicación en un paquete MSIX para su implementación.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-150">The Package project is a Windows Application Packaging Project that is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="f9ed4-151">El proyecto contiene el manifiesto del paquete de la aplicación y es el proyecto de inicio de la solución de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-151">The project contains the package manifest for your app, and is the startup project for your solution by default.</span></span>  <span data-ttu-id="f9ed4-152">Para obtener más información, ve a Configurar la aplicación de escritorio para el empaquetado [MSIX][WindowsMsixDesktopToUwpPackagingDotNet] en Visual Studio y la referencia del esquema del manifiesto del paquete [para Windows 10.][UwpSchemasAppxpackageUapmanifestRoot]</span><span class="sxs-lookup"><span data-stu-id="f9ed4-152">For more information, navigate to [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>  
1.  <span data-ttu-id="f9ed4-153">En el Explorador de soluciones, para mostrar el código, abra el `MainWindow.xaml` archivo.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-153">In the Solution Explorer, to display the code, open the `MainWindow.xaml` file.</span></span>  <span data-ttu-id="f9ed4-154">Para ejecutar el proyecto y mostrar una ventana con un botón, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="f9ed4-154">To run your project and display a window with a button, select `F5`.</span></span>  
    
## <span data-ttu-id="f9ed4-155">Paso 2: Agregar un control WebView2 al proyecto</span><span class="sxs-lookup"><span data-stu-id="f9ed4-155">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="f9ed4-156">Agrega un control WebView2 al proyecto.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-156">Add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="f9ed4-157">En el `MainWindow.xaml` archivo, para agregar el espacio de nombres XAML WebView2, inserta la siguiente línea dentro de la `<Window/>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-157">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="f9ed4-158">Asegúrese de que el código `MainWindow.xaml` es similar al siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-158">Ensure your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="f9ed4-159">Para agregar el control WebView2, reemplace las `<StackPanel>` etiquetas por el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-159">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="f9ed4-160">La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-160">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="f9ed4-161">En el `MainWindow.xaml.cs` archivo, comente la siguiente línea.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-161">In the `MainWindow.xaml.cs` file, comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="f9ed4-162">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="f9ed4-162">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="f9ed4-163">Asegúrese de que se muestra el control WebView2 [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="f9ed4-163">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="El control WebView2 muestra microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="f9ed4-165">El control WebView2 muestra microsoft.com</span><span class="sxs-lookup"><span data-stu-id="f9ed4-165">WebView2 control displays microsoft.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f9ed4-166">Paso 3: Agregar controles de navegación</span><span class="sxs-lookup"><span data-stu-id="f9ed4-166">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="f9ed4-167">Para permitir a los usuarios controlar la página web que se muestra en el control WebView2, agrega una barra de direcciones a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-167">To allow users to control the webpage that is displayed in your WebView2 control, add an address bar to your app.</span></span>  

1.  <span data-ttu-id="f9ed4-168">En el archivo, copie y pegue el siguiente fragmento de código `MainWindow.xaml` dentro del elemento que contiene el `<Grid>` `WebView2` elemento.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-168">In the `MainWindow.xaml` file, copy and paste the following code snippet inside the `<Grid>` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="f9ed4-169">Asegúrese de `<Grid>` que el elemento del archivo es similar al siguiente fragmento de `MainWindow.xaml` código.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-169">Ensure your `<Grid>` element in the `MainWindow.xaml` file is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="f9ed4-170">En el archivo, copie el siguiente fragmento de código en , que navega por el control WebView2 a la dirección URL especificada `MainWindow.xaml.cs` en la barra de `myButton_Click` direcciones.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-170">In the `MainWindow.xaml.cs` file, copy the following code snippet into `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="f9ed4-171">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="f9ed4-171">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="f9ed4-172">Escriba una nueva dirección URL en la barra de direcciones y, a continuación, elija **Ir**.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-172">Enter a new URL in the address bar, and then choose **Go**.</span></span>  <span data-ttu-id="f9ed4-173">Por ejemplo, escriba `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="f9ed4-173">For example, enter `https://www.bing.com`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f9ed4-174">Asegúrese de escribir direcciones URL completas en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-174">Ensure you enter complete URLs in the address bar.</span></span>  `ArgumentException` <span data-ttu-id="f9ed4-175">se inician excepciones si la dirección URL no comienza con `http://` o `https://` .</span><span class="sxs-lookup"><span data-stu-id="f9ed4-175">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="f9ed4-177">bing.com</span><span class="sxs-lookup"><span data-stu-id="f9ed4-177">bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f9ed4-178">Paso 4: Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="f9ed4-178">Step 4 - Navigation events</span></span>  

<span data-ttu-id="f9ed4-179">Las aplicaciones que hospedan controles WebView2 escuchan los siguientes eventos que los controles WebView2 genera durante la navegación de la página web.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-179">Apps that host WebView2 controls listen for the following events that are raised by WebView2 controls during webpage navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="f9ed4-180">Si se produce un redireccionamiento HTTP, hay varios `NavigationStarting` eventos en una fila.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-180">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="f9ed4-181">Para obtener más información, vaya a [Eventos de navegación.][Webviews2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="f9ed4-181">For more information, navigate to [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="f9ed4-182">Cuando se producen errores, se producen los siguientes eventos y pueden navegar a una página web de error.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-182">When errors occur, the following events are raised and may navigate to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="f9ed4-183">Como ejemplo de cómo usar los eventos, registre un controlador para que cancele las solicitudes que no `NavigationStarting` son HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-183">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  <span data-ttu-id="f9ed4-184">In `MainWindow.xaml.cs` , modify the constructor to register , and add the function so that it matches the following `EnsureHttps` code `EnsureHttps` snippet.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-184">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="f9ed4-185">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="f9ed4-185">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="f9ed4-186">Asegúrese de que la navegación está bloqueada en sitios HTTP y permitida para los sitios HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-186">Ensure navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="f9ed4-187">Paso 5: Scripting</span><span class="sxs-lookup"><span data-stu-id="f9ed4-187">Step 5 - Scripting</span></span>  

<span data-ttu-id="f9ed4-188">Puedes usar aplicaciones host para insertar código JavaScript en controles WebView2 en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-188">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="f9ed4-189">Puede hacer que WebView ejecute JavaScript arbitrario o agregue scripts de inicialización.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-189">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="f9ed4-190">El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a todos los fotogramas secundarios hasta que se quite el JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-190">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="f9ed4-191">El JavaScript inyectado se ejecuta con intervalos específicos.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-191">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="f9ed4-192">Ejecutarlo después de la creación del objeto global.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-192">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="f9ed4-193">Ejecutarlo antes de ejecutar cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-193">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="f9ed4-194">Por ejemplo, agregue scripts que envíen una alerta cuando un usuario navegue a sitios que no son HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-194">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="f9ed4-195">Modifique la `EnsureHttps` función para insertar un script en el contenido web que usa [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="f9ed4-195">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="f9ed4-196">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="f9ed4-196">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="f9ed4-197">Asegúrate de que la aplicación muestra una alerta cuando navegas a cualquier sitio web que no sea HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-197">Ensure your app displays an alert when you navigate to any non-HTTPS websites.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="El control WebView2 muestra un cuadro de diálogo de alerta" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="f9ed4-199">El control WebView2 muestra un cuadro de diálogo de alerta</span><span class="sxs-lookup"><span data-stu-id="f9ed4-199">WebView2 control displays an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="f9ed4-200">Enhorabuena, has creado tu primera aplicación WebView2.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-200">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="f9ed4-201">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="f9ed4-201">Next steps</span></span>  

<span data-ttu-id="f9ed4-202">Para continuar con el aprendizaje sobre WebView2, vaya a los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-202">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <span data-ttu-id="f9ed4-203">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f9ed4-203">See also</span></span>  

*   <span data-ttu-id="f9ed4-204">Para obtener un ejemplo completo de las capacidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="f9ed4-204">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="f9ed4-205">Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="f9ed4-205">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f9ed4-206">Es posible que el objeto WinRT CoreWebView2 no esté disponible con la versión de la API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-206">The WinRT CoreWebView2 object may not be available with the release of the WebView2 API.</span></span>  <span data-ttu-id="f9ed4-207">Para comprender qué API están disponibles para los controles WebView2, ve a [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] para obtener una lista de las API que están disponibles.</span><span class="sxs-lookup"><span data-stu-id="f9ed4-207">To understand which APIs are available to WebView2 controls, navigate to [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span>  
    
*   <span data-ttu-id="f9ed4-208">Para obtener información detallada acerca de la API de WebView2, vaya a [la especificación de WebView2][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="f9ed4-208">For detailed information about the WebView2 API, navigate to [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  
    
## <span data-ttu-id="f9ed4-209">Introducción al equipo de Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="f9ed4-209">Getting in touch with the Microsoft Edge WebView team</span></span>  

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

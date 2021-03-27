---
description: Guía de introducción a WebView2 para aplicaciones WinUI
title: Introducción a WebView2 para aplicaciones WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, aplicaciones winui, winui, edge, CoreWebView2, control de explorador, html perimetral, introducción, Introducción, .NET
ms.openlocfilehash: 52d84afb6f9fe1e120f75525b2669a797309fdfe
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461209"
---
# <a name="getting-started-with-webview2-in-winui-3-preview"></a><span data-ttu-id="766c3-104">Introducción a WebView2 en WinUI 3 (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="766c3-104">Getting started with WebView2 in WinUI 3 (Preview)</span></span>  

<span data-ttu-id="766c3-105">En este artículo, empieza a crear tu primera aplicación WebView2 y obtén información sobre las características principales de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="766c3-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="766c3-106">La primera aplicación WebView2 usa WinUI3.</span><span class="sxs-lookup"><span data-stu-id="766c3-106">Your first WebView2 app uses WinUI3.</span></span>  <span data-ttu-id="766c3-107">Para obtener más información sobre las API individuales, vaya a [Referencia de api][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="766c3-107">For more information on individual APIs, navigate to [API reference][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="766c3-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="766c3-108">Prerequisites</span></span>  

<span data-ttu-id="766c3-109">Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="766c3-109">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="766c3-110">[WebView2 Runtime][Webview2Installer] o cualquier canal no estable de [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado en Windows 10 versión 1803 \(compilación 17134\) o posterior.</span><span class="sxs-lookup"><span data-stu-id="766c3-110">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="766c3-111">Para obtener más información acerca de Windows 10, ve a [Windows Update: Faq][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="766c3-111">For more information about Windows 10, navigate to [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="766c3-112">El equipo de WebView recomienda usar el canal Canary y la versión mínima necesaria es 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="766c3-112">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="766c3-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, versión 16.9 Preview.</span><span class="sxs-lookup"><span data-stu-id="766c3-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, version 16.9 Preview.</span></span>  <span data-ttu-id="766c3-114">Para obtener más información, vaya a Biblioteca de [la interfaz de usuario de Windows 3 Versión preliminar 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="766c3-114">For more information, navigate to [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
    *   <span data-ttu-id="766c3-115">Incluya las siguientes cargas de trabajo al instalar Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="766c3-115">Include the following workloads when you install Visual Studio.</span></span>  
        *   <span data-ttu-id="766c3-116">Desarrollo de escritorio de .NET \(el instalador también instala .NET 5\)</span><span class="sxs-lookup"><span data-stu-id="766c3-116">.NET Desktop Development \(the installer also installs .NET 5\)</span></span>  
        *   <span data-ttu-id="766c3-117">Desarrollo de la Plataforma universal de Windows</span><span class="sxs-lookup"><span data-stu-id="766c3-117">Universal Windows Platform development</span></span>  
    *   <span data-ttu-id="766c3-118">Para crear aplicaciones de C++, también debe incluir las siguientes cargas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="766c3-118">To build C++ apps, you must also include the following workloads.</span></span>  
        *   <span data-ttu-id="766c3-119">Desarrollo de escritorio con C++</span><span class="sxs-lookup"><span data-stu-id="766c3-119">Desktop development with C++</span></span>  
        *   <span data-ttu-id="766c3-120">El componente opcional de herramientas de la Plataforma universal de Windows C++ \(v142\) para la carga de trabajo de la Plataforma universal de Windows.</span><span class="sxs-lookup"><span data-stu-id="766c3-120">The C++ \(v142\) Universal Windows Platform tools optional component for the Universal Windows Platform workload.</span></span>  <span data-ttu-id="766c3-121">Para obtener más información, vaya **a Detalles de instalación** en la sección Desarrollo de la Plataforma universal de **Windows,** en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="766c3-121">For more information,  navigate to **Installation Details** under the **Universal Windows Platform development** section, on the right pane.</span></span>  
        
## <a name="step-0---visual-studio-settings"></a><span data-ttu-id="766c3-122">Paso 0: configuración Visual Studio configuración</span><span class="sxs-lookup"><span data-stu-id="766c3-122">Step 0 - Visual Studio settings</span></span>  

1.  <span data-ttu-id="766c3-123">Asegúrese de que el sistema tiene un origen de paquete NuGet habilitado para [nuget.org][NugetHome].  Para obtener más información, vaya a [Configuraciones comunes de NuGet y][NugetConsumePackagesConfiguringNugetBehavior] [Windows Community Toolkit][WindowsCommunitytoolkit].</span><span class="sxs-lookup"><span data-stu-id="766c3-123">Ensure your system has a NuGet package source enabled for [nuget.org][NugetHome].  For more information, navigate to [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span></span>  
1.  <span data-ttu-id="766c3-124">Descargue e instale el paquete [VSIX de WinUI 3 Preview 3][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span><span class="sxs-lookup"><span data-stu-id="766c3-124">Download and install the [WinUI 3 Preview 3 VSIX package][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span></span>  <span data-ttu-id="766c3-125">El instalador agrega las plantillas de proyecto WinUI 3 y el paquete NuGet que contiene las bibliotecas WinUI 3 a Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="766c3-125">The installer adds both the WinUI 3 project templates and the NuGet package containing the WinUI 3 libraries to Visual Studio 2019.</span></span>  
    
    <span data-ttu-id="766c3-126">Para obtener instrucciones sobre cómo agregar el paquete a Visual Studio, vaya a `VSIX` Buscar y usar Visual Studio [extensiones][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span><span class="sxs-lookup"><span data-stu-id="766c3-126">For instructions on how to add the `VSIX` package to Visual Studio, navigate to [Finding and Using Visual Studio Extensions][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span></span>
    
1.  <span data-ttu-id="766c3-127">Para obtener acceso a todas las características de Visual Studio específicas del [desarrollador,][WindowsUwpGetStartedEnableYourDeviceForDevelopment]active el modo de desarrollador .</span><span class="sxs-lookup"><span data-stu-id="766c3-127">To access all developer-specific Visual Studio features, turn on [Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment].</span></span>  
    
## <a name="step-1---create-project"></a><span data-ttu-id="766c3-128">Paso 1: Crear proyecto</span><span class="sxs-lookup"><span data-stu-id="766c3-128">Step 1 - Create Project</span></span>  

<span data-ttu-id="766c3-129">Comience con un proyecto de escritorio básico que contenga una sola ventana principal.</span><span class="sxs-lookup"><span data-stu-id="766c3-129">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="766c3-130">En Visual Studio, elija **Crear un nuevo proyecto**.</span><span class="sxs-lookup"><span data-stu-id="766c3-130">In Visual Studio, choose **Create a new project**.</span></span>  
1.  <span data-ttu-id="766c3-131">En la lista desplegable del proyecto, **elija C#**, **Windows**y **WinUI** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="766c3-131">In the project drop-down, choose **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Crear un nuevo proyecto WinUI mediante Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        <span data-ttu-id="766c3-133">Crear un nuevo proyecto WinUI mediante Visual Studio</span><span class="sxs-lookup"><span data-stu-id="766c3-133">Create a new WinUI project using Visual Studio</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="766c3-134">Elija **Aplicación en blanco, empaquetada (WinUI en escritorio)**  >  **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="766c3-134">Choose **Blank App, Packaged (WinUI in Desktop)** > **Next**.</span></span>  
1.  <span data-ttu-id="766c3-135">Escriba un nombre de proyecto.</span><span class="sxs-lookup"><span data-stu-id="766c3-135">Enter a project name.</span></span>
1.  <span data-ttu-id="766c3-136">Elija las opciones según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="766c3-136">Choose options as needed.</span></span>  
1.  <span data-ttu-id="766c3-137">Elija **Crear**.</span><span class="sxs-lookup"><span data-stu-id="766c3-137">Choose **Create**.</span></span>  
1.  <span data-ttu-id="766c3-138">En **Nuevo proyecto de plataforma universal de Windows,** elija los siguientes valores y, a continuación, elija **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="766c3-138">In **New Universal Windows Platform Project**, choose the following values, and then choose **OK**.</span></span>  
    *   <span data-ttu-id="766c3-139">**Versión de**destino:  **Windows 10, versión 1903 (compilación 18362)** o posterior</span><span class="sxs-lookup"><span data-stu-id="766c3-139">**Target version**:  **Windows 10, version 1903 (build 18362)** or later</span></span>  
    *   <span data-ttu-id="766c3-140">**Versión mínima:**  **Windows 10, versión 1803 (compilación 17134)**</span><span class="sxs-lookup"><span data-stu-id="766c3-140">**Minimum version**:  **Windows 10, version 1803 (build 17134)**</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Cuadro de diálogo Nuevo proyecto de plataforma universal de Windows con los valores elegidos para la versión de destino y la versión mínima." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="766c3-142">Cuadro de diálogo Nuevo proyecto de plataforma universal de Windows con los valores elegidos para la versión de destino y la versión mínima.</span><span class="sxs-lookup"><span data-stu-id="766c3-142">The New Universal Windows Platform Project dialog with chosen values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="766c3-143">En el Explorador de soluciones, se generan dos proyectos.</span><span class="sxs-lookup"><span data-stu-id="766c3-143">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="766c3-144">**Nombre del proyecto (Escritorio).**</span><span class="sxs-lookup"><span data-stu-id="766c3-144">**Your project name (Desktop)**.</span></span>  <span data-ttu-id="766c3-145">El proyecto de escritorio contiene el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="766c3-145">The Desktop project contains the code for your app.</span></span>  <span data-ttu-id="766c3-146">El `App.xaml.cs` archivo define una clase que representa la instancia de la `Application` aplicación.</span><span class="sxs-lookup"><span data-stu-id="766c3-146">The `App.xaml.cs` file defines an `Application` class that represents your app instance.</span></span>  <span data-ttu-id="766c3-147">El `MainWindow.xaml.cs` archivo define una clase que representa la ventana principal que muestra la instancia de la `MainWindow` aplicación.</span><span class="sxs-lookup"><span data-stu-id="766c3-147">The `MainWindow.xaml.cs` file defines a `MainWindow` class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="766c3-148">Las clases derivan de tipos en el `Microsoft.UI.Xaml` espacio de nombres de WinUI.</span><span class="sxs-lookup"><span data-stu-id="766c3-148">The classes derive from types in the `Microsoft.UI.Xaml` namespace of WinUI.</span></span>  
    *   <span data-ttu-id="766c3-149">**Nombre del proyecto (paquete).**</span><span class="sxs-lookup"><span data-stu-id="766c3-149">**Your project name (Package)**.</span></span>  <span data-ttu-id="766c3-150">El proyecto Package es un proyecto de empaquetado de aplicaciones de Windows que está configurado para compilar la aplicación en un paquete MSIX para su implementación.</span><span class="sxs-lookup"><span data-stu-id="766c3-150">The Package project is a Windows Application Packaging Project that is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="766c3-151">El proyecto contiene el manifiesto del paquete de la aplicación y es el proyecto de inicio de la solución de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="766c3-151">The project contains the package manifest for your app, and is the startup project for your solution by default.</span></span>  <span data-ttu-id="766c3-152">Para obtener más información, vaya a Configurar la aplicación de escritorio para el empaquetado [MSIX][WindowsMsixDesktopToUwpPackagingDotNet] en Visual Studio y Referencia del esquema de manifiesto del paquete [para Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="766c3-152">For more information, navigate to [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>  
1.  <span data-ttu-id="766c3-153">En el Explorador de soluciones, para mostrar el código, abra el `MainWindow.xaml` archivo.</span><span class="sxs-lookup"><span data-stu-id="766c3-153">In the Solution Explorer, to display the code, open the `MainWindow.xaml` file.</span></span>  <span data-ttu-id="766c3-154">Para ejecutar el proyecto y mostrar una ventana con un botón, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="766c3-154">To run your project and display a window with a button, select `F5`.</span></span>  
    
## <a name="step-2---add-a-webview2-control-to-your-project"></a><span data-ttu-id="766c3-155">Paso 2: Agregar un control WebView2 al proyecto</span><span class="sxs-lookup"><span data-stu-id="766c3-155">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="766c3-156">Agregue un control WebView2 al proyecto.</span><span class="sxs-lookup"><span data-stu-id="766c3-156">Add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="766c3-157">En el `MainWindow.xaml` archivo, para agregar el espacio de nombres XAML webView2, inserte la siguiente línea dentro de la `<Window/>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="766c3-157">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="766c3-158">Asegúrese de que el código `MainWindow.xaml` es similar al siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="766c3-158">Ensure your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="766c3-159">Para agregar el control WebView2, reemplace las `<StackPanel>` etiquetas por el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="766c3-159">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="766c3-160">La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="766c3-160">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="766c3-161">En el `MainWindow.xaml.cs` archivo, comenta la siguiente línea.</span><span class="sxs-lookup"><span data-stu-id="766c3-161">In the `MainWindow.xaml.cs` file, comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="766c3-162">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="766c3-162">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="766c3-163">Asegúrese de que el control WebView2 muestra [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="766c3-163">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="El control WebView2 muestra microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="766c3-165">El control WebView2 muestra microsoft.com</span><span class="sxs-lookup"><span data-stu-id="766c3-165">WebView2 control displays microsoft.com</span></span>  
    :::image-end:::  
    
## <a name="step-3---add-navigation-controls"></a><span data-ttu-id="766c3-166">Paso 3: Agregar controles de navegación</span><span class="sxs-lookup"><span data-stu-id="766c3-166">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="766c3-167">Para permitir a los usuarios controlar la página web que se muestra en el control WebView2, agregue una barra de direcciones a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="766c3-167">To allow users to control the webpage that is displayed in your WebView2 control, add an address bar to your app.</span></span>  

1.  <span data-ttu-id="766c3-168">En el archivo, copie y pegue el siguiente fragmento de código `MainWindow.xaml` dentro del elemento que contiene el `<Grid>` `WebView2` elemento.</span><span class="sxs-lookup"><span data-stu-id="766c3-168">In the `MainWindow.xaml` file, copy and paste the following code snippet inside the `<Grid>` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="766c3-169">Asegúrese de `<Grid>` que el elemento del archivo es similar al siguiente fragmento de `MainWindow.xaml` código.</span><span class="sxs-lookup"><span data-stu-id="766c3-169">Ensure your `<Grid>` element in the `MainWindow.xaml` file is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="766c3-170">En el archivo, copie el siguiente fragmento de código en , que navega el control WebView2 a la `MainWindow.xaml.cs` dirección URL especificada en la barra de `myButton_Click` direcciones.</span><span class="sxs-lookup"><span data-stu-id="766c3-170">In the `MainWindow.xaml.cs` file, copy the following code snippet into `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="766c3-171">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="766c3-171">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="766c3-172">Escriba una nueva dirección URL en la barra de direcciones y, a continuación, elija **Ir**.</span><span class="sxs-lookup"><span data-stu-id="766c3-172">Enter a new URL in the address bar, and then choose **Go**.</span></span>  <span data-ttu-id="766c3-173">Por ejemplo, escriba `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="766c3-173">For example, enter `https://www.bing.com`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="766c3-174">Asegúrese de escribir direcciones URL completas en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="766c3-174">Ensure you enter complete URLs in the address bar.</span></span>  `ArgumentException` <span data-ttu-id="766c3-175">excepciones se inician si la dirección URL no comienza con `http://` o `https://` .</span><span class="sxs-lookup"><span data-stu-id="766c3-175">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="766c3-177">bing.com</span><span class="sxs-lookup"><span data-stu-id="766c3-177">bing.com</span></span>  
    :::image-end:::  
    
## <a name="step-4---navigation-events"></a><span data-ttu-id="766c3-178">Paso 4: Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="766c3-178">Step 4 - Navigation events</span></span>  

<span data-ttu-id="766c3-179">Las aplicaciones que hospedan controles WebView2 escuchan los siguientes eventos que se genera mediante controles WebView2 durante la navegación en la página web.</span><span class="sxs-lookup"><span data-stu-id="766c3-179">Apps that host WebView2 controls listen for the following events that are raised by WebView2 controls during webpage navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="766c3-180">Si se produce un redireccionamiento HTTP, hay varios `NavigationStarting` eventos en una fila.</span><span class="sxs-lookup"><span data-stu-id="766c3-180">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="766c3-181">Para obtener más información, vaya a [Eventos de navegación][Webviews2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="766c3-181">For more information, navigate to [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="766c3-182">Cuando se producen errores, se producen los siguientes eventos y se puede navegar a una página web de error.</span><span class="sxs-lookup"><span data-stu-id="766c3-182">When errors occur, the following events are raised and may navigate to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="766c3-183">Como ejemplo de cómo usar los eventos, registre un controlador para que cancele las solicitudes que no son `NavigationStarting` HTTPS.</span><span class="sxs-lookup"><span data-stu-id="766c3-183">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  <span data-ttu-id="766c3-184">In `MainWindow.xaml.cs` , modify the constructor to register , and add the function so that it matches the following `EnsureHttps` code `EnsureHttps` snippet.</span><span class="sxs-lookup"><span data-stu-id="766c3-184">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="766c3-185">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="766c3-185">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="766c3-186">Asegúrese de que la navegación está bloqueada en sitios HTTP y permitida para sitios HTTPS.</span><span class="sxs-lookup"><span data-stu-id="766c3-186">Ensure navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <a name="step-5---scripting"></a><span data-ttu-id="766c3-187">Paso 5: scripting</span><span class="sxs-lookup"><span data-stu-id="766c3-187">Step 5 - Scripting</span></span>  

<span data-ttu-id="766c3-188">Puede usar aplicaciones host para insertar código JavaScript en controles WebView2 en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="766c3-188">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="766c3-189">Puede realizar la tarea WebView para ejecutar JavaScript arbitrario o agregar scripts de inicialización.</span><span class="sxs-lookup"><span data-stu-id="766c3-189">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="766c3-190">JavaScript inyectado se aplica a todos los nuevos documentos de nivel superior y a los fotogramas secundarios hasta que se quita JavaScript.</span><span class="sxs-lookup"><span data-stu-id="766c3-190">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="766c3-191">JavaScript inyectado se ejecuta con un tiempo específico.</span><span class="sxs-lookup"><span data-stu-id="766c3-191">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="766c3-192">Ejecutarlo después de la creación del objeto global.</span><span class="sxs-lookup"><span data-stu-id="766c3-192">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="766c3-193">Ejecutarlo antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="766c3-193">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="766c3-194">Por ejemplo, agregue scripts que envíen una alerta cuando un usuario navegue a sitios que no son HTTPS.</span><span class="sxs-lookup"><span data-stu-id="766c3-194">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="766c3-195">Modifique la `EnsureHttps` función para insertar un script en el contenido web que usa [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="766c3-195">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="766c3-196">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="766c3-196">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="766c3-197">Asegúrate de que la aplicación muestra una alerta cuando navegas a sitios web que no son HTTPS.</span><span class="sxs-lookup"><span data-stu-id="766c3-197">Ensure your app displays an alert when you navigate to any non-HTTPS websites.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="El control WebView2 muestra un cuadro de diálogo de alerta" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="766c3-199">El control WebView2 muestra un cuadro de diálogo de alerta</span><span class="sxs-lookup"><span data-stu-id="766c3-199">WebView2 control displays an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="766c3-200">Enhorabuena, has creado tu primera aplicación WebView2.</span><span class="sxs-lookup"><span data-stu-id="766c3-200">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="766c3-201">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="766c3-201">Next steps</span></span>  

<span data-ttu-id="766c3-202">Para seguir aprendiendo más sobre WebView2, vaya a los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="766c3-202">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <a name="see-also"></a><span data-ttu-id="766c3-203">Consulte también</span><span class="sxs-lookup"><span data-stu-id="766c3-203">See also</span></span>  

*   <span data-ttu-id="766c3-204">Para obtener un ejemplo completo de las capacidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="766c3-204">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="766c3-205">Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="766c3-205">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="766c3-206">Es posible que el objeto WinRT CoreWebView2 no esté disponible con la versión de la API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="766c3-206">The WinRT CoreWebView2 object may not be available with the release of the WebView2 API.</span></span>  <span data-ttu-id="766c3-207">Para comprender qué API están disponibles para los controles WebView2, vaya a [WebView2 Spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2] para obtener una lista de las API que están disponibles.</span><span class="sxs-lookup"><span data-stu-id="766c3-207">To understand which APIs are available to WebView2 controls, navigate to [WebView2 Spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span>  
    
*   <span data-ttu-id="766c3-208">Para obtener información detallada acerca de la API de WebView2, vaya a [WebView2 spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="766c3-208">For detailed information about the WebView2 API, navigate to [WebView2 spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="766c3-209">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="766c3-209">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<span data-ttu-id="766c3-210">Para enviar las solicitudes de características específicas de WinUI o los errores, vaya a [Problemas - microsoft/microsoft-ui-xaml][GithubMicrosoftMicrosoftUiXamlIssues] y elija **Nuevo problema**.</span><span class="sxs-lookup"><span data-stu-id="766c3-210">To send your WinUI-specific feature requests or bugs, navigate to [Issues - microsoft/microsoft-ui-xaml][GithubMicrosoftMicrosoftUiXamlIssues] and choose **New issue**.</span></span>  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: ../index.md "Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegación | Microsoft Docs"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Configuraciones comunes de NuGet | Microsoft Docs"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Referencia de esquema de manifiesto de paquete para Windows 10 | Microsoft Docs"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Instalar sin usar el cuadro de diálogo Administrar extensiones: administrar extensiones para Visual Studio | Microsoft Docs"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurar el entorno de desarrollo: Windows UI Library 3.0 Preview 1 (mayo de 2020) | Microsoft Docs"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Documentación de Windows Community Toolkit | Microsoft Docs"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurar la aplicación de escritorio para el empaquetado MSIX en Visual Studio | Microsoft Docs"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Habilitar el dispositivo para desarrollo | Microsoft Docs"  

[GithubMicrosoftMicrosoftUiXamlIssues]: https://github.com/microsoft/microsoft-ui-xaml/issues "Problemas: microsoft/microsoft-ui-xaml | GitHub"  
[GithubMicrosoftMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "Especificación de WebView2: microsoft/microsoft-ui-xaml-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: Preguntas más frecuentes"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[NugetHome]: https://nuget.org "Inicio | Galería nuGet"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Descargar dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Plantillas de proyecto de WinUI 3 | Visual Studio Marketplace"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador de WebView2" 

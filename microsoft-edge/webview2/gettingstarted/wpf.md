---
description: Guía de introducción a WebView2 para aplicaciones de WPF
title: Introducción a WebView2 para las aplicaciones de WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicaciones WPF, WPF, Edge, CoreWebView2, control de explorador, código HTML de Edge, introducción, .NET
ms.openlocfilehash: e928dae0aa63f15ca5fa21860c83fa5529e905df
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182377"
---
# <span data-ttu-id="43d76-104">Introducción a WebView2 en WPF</span><span class="sxs-lookup"><span data-stu-id="43d76-104">Getting started with WebView2 in WPF</span></span>

<span data-ttu-id="43d76-105">En este artículo, empiece a crear su primera aplicación de WebView2 y conozca las características principales de [WebView2](../index.md).</span><span class="sxs-lookup"><span data-stu-id="43d76-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2](../index.md).</span></span>  <span data-ttu-id="43d76-106">Para obtener más información sobre las API individuales, consulta referencia de la [API](/dotnet/api/microsoft.web.webview2.wpf).</span><span class="sxs-lookup"><span data-stu-id="43d76-106">For more information on individual APIs, see [API reference](/dotnet/api/microsoft.web.webview2.wpf).</span></span>  

## <span data-ttu-id="43d76-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="43d76-107">Prerequisites</span></span>  

<span data-ttu-id="43d76-108">Asegúrese de haber instalado la siguiente lista de requisitos previos antes de continuar:</span><span class="sxs-lookup"><span data-stu-id="43d76-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="43d76-109">[WebView2 en tiempo de ejecución][Webview2Installer] o cualquier [canal Canarias no estable de Microsoft Edge (cromo)](https://www.microsoftedgeinsider.com/download) instalado en windows 10, Windows 8,1 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="43d76-109">[WebView2 Runtime][Webview2Installer] or any [non-stable Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download) installed on Windows 10, Windows 8.1, or Windows 7.</span></span>  
* <span data-ttu-id="43d76-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 o posterior.</span><span class="sxs-lookup"><span data-stu-id="43d76-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 or later.</span></span>  

## <span data-ttu-id="43d76-111">Paso 1: crear una aplicación de una sola ventana</span><span class="sxs-lookup"><span data-stu-id="43d76-111">Step 1 - Create a single window application</span></span>  

<span data-ttu-id="43d76-112">Empiece con un proyecto de escritorio básico que contenga una única ventana principal.</span><span class="sxs-lookup"><span data-stu-id="43d76-112">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="43d76-113">Abra **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="43d76-113">Open **Visual Studio**.</span></span>  
1.  <span data-ttu-id="43d76-114">Seleccione aplicación **.net Core de WPF** o **aplicación .NET Framework de WPF**y, a continuación, seleccione **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="43d76-114">Select **WPF .NET Core App** or **WPF .NET Framework App**, and then select **Next**.</span></span>  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="WPF Core":::
             <span data-ttu-id="43d76-116">WPF Core</span><span class="sxs-lookup"><span data-stu-id="43d76-116">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Marco WPF":::
             <span data-ttu-id="43d76-118">Marco WPF</span><span class="sxs-lookup"><span data-stu-id="43d76-118">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="43d76-119">Escriba los valores para **el nombre** y la **Ubicación**del proyecto.</span><span class="sxs-lookup"><span data-stu-id="43d76-119">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="43d76-120">Seleccione .NET Framework 4.6.2 o posterior o .NET Core 3,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="43d76-120">Select .NET Framework 4.6.2 or later, or .NET Core 3.0 or later.</span></span>  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Crear núcleo":::
                 <span data-ttu-id="43d76-122">Crear núcleo</span><span class="sxs-lookup"><span data-stu-id="43d76-122">Create core</span></span> :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Crear marco de trabajo":::
                 <span data-ttu-id="43d76-124">Crear marco de trabajo</span><span class="sxs-lookup"><span data-stu-id="43d76-124">Create Framework</span></span> :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  <span data-ttu-id="43d76-125">Seleccione **crear** para crear el proyecto.</span><span class="sxs-lookup"><span data-stu-id="43d76-125">Select **Create** to create your project.</span></span>  
    
## <span data-ttu-id="43d76-126">Paso 2: instalar el SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="43d76-126">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="43d76-127">A continuación, agregue el SDK de WebView2 al proyecto con NuGet.</span><span class="sxs-lookup"><span data-stu-id="43d76-127">Next add the WebView2 SDK to the project using NuGet.</span></span>  

1.  <span data-ttu-id="43d76-128">Abra el menú contextual en el proyecto \ (haga clic con el botón derecho \) y seleccione **administrar paquetes NuGet...**.</span><span class="sxs-lookup"><span data-stu-id="43d76-128">Open the context menu on the project \(right-click\), and select **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       <span data-ttu-id="43d76-130">NuGet</span><span class="sxs-lookup"><span data-stu-id="43d76-130">NuGet</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="43d76-131">Escriba `Microsoft.Web.WebView2` en la barra de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="43d76-131">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="43d76-132">Seleccione **Microsoft. Web. WebView2** en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="43d76-132">Select **Microsoft.Web.WebView2** from the search results.</span></span>  
   
     ![Nuget](./media/installnuget.PNG)
    
    <span data-ttu-id="43d76-134">Ya está todo listo para empezar a desarrollar aplicaciones con la API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="43d76-134">You're all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="43d76-135">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="43d76-135">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="43d76-136">El proyecto en ejecución muestra una ventana vacía.</span><span class="sxs-lookup"><span data-stu-id="43d76-136">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Aplicación vacía":::
       <span data-ttu-id="43d76-138">Aplicación vacía</span><span class="sxs-lookup"><span data-stu-id="43d76-138">Empty app</span></span>
    :::image-end:::  
    
## <span data-ttu-id="43d76-139">Paso 3: crear una sola vista previa en MainWindow. Xaml</span><span class="sxs-lookup"><span data-stu-id="43d76-139">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="43d76-140">A continuación, agregue una vista de vista a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="43d76-140">Next add a WebView to your application.</span></span>  

1.  <span data-ttu-id="43d76-141">Abra `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="43d76-141">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="43d76-142">Agrega el espacio de nombres XAML WebView2 insertando la siguiente línea dentro de la `<Window/>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="43d76-142">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    <span data-ttu-id="43d76-143">Confirme que el código de `MainWindow.xaml` la es similar al siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="43d76-143">Confirm that the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="43d76-144">Agregue el control WebView2 reemplazando las `<Grid>` etiquetas, con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="43d76-144">Add the WebView2 control by replacing the `<Grid>` tags, with the following code snippet.</span></span>  <span data-ttu-id="43d76-145">La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="43d76-145">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  <span data-ttu-id="43d76-146">Pulse `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="43d76-146">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="43d76-147">Confirme que se muestra el control WebView2 [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="43d76-147">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="43d76-149">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="43d76-149">Microsoft.com</span></span>
    :::image-end:::  
    
## <span data-ttu-id="43d76-150">Paso 4: navegación</span><span class="sxs-lookup"><span data-stu-id="43d76-150">Step 4 - Navigation</span></span>  

<span data-ttu-id="43d76-151">Agregue una barra de direcciones a la aplicación para permitir a los usuarios que cambien la dirección URL que muestra el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="43d76-151">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="43d76-152">En **MainWindow. Xaml**, agregue una barra de direcciones copiando y pegando el siguiente fragmento de código dentro de la DockPanel que contiene la vista de gráfico.</span><span class="sxs-lookup"><span data-stu-id="43d76-152">In **MainWindow.xaml**, add an address bar by copying and pasting the following code snippet inside the DockPanel that contains the WebView.</span></span>  
    
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
    
    <span data-ttu-id="43d76-153">Confirme que la `DockPanel` sección de `MainWindow.xaml` aparece como el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="43d76-153">Confirm that the `DockPanel` section of `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="43d76-154">Abrir `MainWindow.xaml.cs` en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="43d76-154">Open `MainWindow.xaml.cs` in Visual Studio.</span></span>  <span data-ttu-id="43d76-155">Para agregar el `CoreWebView2` espacio de nombres, inserte el siguiente fragmento de código en la parte superior de `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="43d76-155">Add the `CoreWebView2` namespace by inserting the following code snippet at the top of `MainWindow.xaml.cs`.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  <span data-ttu-id="43d76-156">En **MainWindow.Xaml.CS**, copie el siguiente fragmento de código para crear el `ButtonGo_Click` método, que navega por la vista en vista previa a la dirección URL que se escribe en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="43d76-156">In **MainWindow.xaml.cs**, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    <span data-ttu-id="43d76-157">Pulse `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="43d76-157">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="43d76-158">Escriba una nueva dirección URL en la barra de direcciones y seleccione **ir**.</span><span class="sxs-lookup"><span data-stu-id="43d76-158">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="43d76-159">Por ejemplo, escriba `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="43d76-159">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="43d76-160">Confirme que el control WebView2 se desplaza hasta la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="43d76-160">Confirm that the WebView2 control navigates to the URL.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="43d76-161">Asegúrese de que se escribe una dirección URL completa en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="43d76-161">Make sure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="43d76-162">`ArgumentException`Se inicia una si la dirección URL no comienza con `http://` o `https://` .</span><span class="sxs-lookup"><span data-stu-id="43d76-162">An `ArgumentException` is thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       <span data-ttu-id="43d76-164">Bing</span><span class="sxs-lookup"><span data-stu-id="43d76-164">Bing</span></span>
    :::image-end:::
    
## <span data-ttu-id="43d76-165">Paso 5: eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="43d76-165">Step 5 - Navigation events</span></span>  

<span data-ttu-id="43d76-166">Durante la navegación de páginas web, el control WebView2 desencadena eventos.</span><span class="sxs-lookup"><span data-stu-id="43d76-166">During webpage navigation, the WebView2 control raises events.</span></span> <span data-ttu-id="43d76-167">La aplicación que hospeda los controles WebView2 escucha los siguientes eventos.</span><span class="sxs-lookup"><span data-stu-id="43d76-167">The application that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="43d76-168">Para obtener más información, vea [eventos de navegación](../concepts/navigation-events.md).</span><span class="sxs-lookup"><span data-stu-id="43d76-168">For more information, see [Navigation Events](../concepts/navigation-events.md).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación":::
   <span data-ttu-id="43d76-170">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="43d76-170">Navigation events</span></span>
:::image-end:::  

<span data-ttu-id="43d76-171">Cuando se produce un error, se producen los eventos siguientes y puede que dependan de la navegación a una página de error.</span><span class="sxs-lookup"><span data-stu-id="43d76-171">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

<span data-ttu-id="43d76-172">Cuando hay una redirección de HTTP, hay varios `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="43d76-172">When there's an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="43d76-173">Para mostrar cómo usar estos eventos, comienza registrando un controlador para `NavigationStarting` que cancele todas las solicitudes que no usen https.</span><span class="sxs-lookup"><span data-stu-id="43d76-173">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span>  

<span data-ttu-id="43d76-174">En `MainWindow.xaml.cs` , modifique el constructor como se muestra a continuación y agregue la `EnsureHttps` función.</span><span class="sxs-lookup"><span data-stu-id="43d76-174">In `MainWindow.xaml.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="43d76-175">En el constructor, EnsureHttps se registra como el controlador de eventos en el `NavigationStarting` evento en el control de WebView2.</span><span class="sxs-lookup"><span data-stu-id="43d76-175">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="43d76-176">Pulse `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="43d76-176">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="43d76-177">Confirme que, al navegar a un sitio HTTP, la WebView no sufre **cambios**.</span><span class="sxs-lookup"><span data-stu-id="43d76-177">Confirm that when navigating to an HTTP site, the WebView **remains unchanged**.</span></span>  <span data-ttu-id="43d76-178">Sin embargo, la vista Web se desplaza a sitios HTTPS.</span><span class="sxs-lookup"><span data-stu-id="43d76-178">However, the WebView navigates to HTTPS sites.</span></span>  

## <span data-ttu-id="43d76-179">Paso 6: scripting</span><span class="sxs-lookup"><span data-stu-id="43d76-179">Step 6 - Scripting</span></span>  

<span data-ttu-id="43d76-180">Puede usar aplicaciones host para inyectar código JavaScript en controles WebView2 en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="43d76-180">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="43d76-181">El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a cualquier fotograma secundario, hasta que se quite el JavaScript.</span><span class="sxs-lookup"><span data-stu-id="43d76-181">The injected JavaScript applies to all new top-level documents and any child frames, until the JavaScript is removed.</span></span>  <span data-ttu-id="43d76-182">El código JavaScript insertado se ejecuta después de la creación del objeto global y antes de los scripts incluidos en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="43d76-182">The injected JavaScript is run after creation of the global object, and before any scripts included in the HTML document.</span></span>  

<span data-ttu-id="43d76-183">Puede usar scripting para avisar al usuario cuando navegue a un sitio que no es HTTPS.</span><span class="sxs-lookup"><span data-stu-id="43d76-183">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="43d76-184">Modifique la `EnsureHttps` función para que inserte el script en el contenido web con el método [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) .</span><span class="sxs-lookup"><span data-stu-id="43d76-184">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) method.</span></span>  

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

<span data-ttu-id="43d76-185">Pulse `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="43d76-185">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="43d76-186">Confirme que la aplicación muestra una alerta cuando navegue a un sitio que no usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="43d76-186">Confirm that the application displays an alert when you navigate to a site that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="43d76-188">HTTPS</span><span class="sxs-lookup"><span data-stu-id="43d76-188">HTTPS</span></span>
:::image-end:::  

## <span data-ttu-id="43d76-189">Paso 7: comunicación entre el host y el contenido web</span><span class="sxs-lookup"><span data-stu-id="43d76-189">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="43d76-190">El host y el contenido web pueden comunicarse entre sí mediante las `postMessage` siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="43d76-190">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

*   <span data-ttu-id="43d76-191">El contenido Web de un control WebView2 puede publicar un mensaje en el host mediante `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="43d76-191">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="43d76-192">El anfitrión controla el mensaje con cualquier registro `WebMessageReceived` en el host.</span><span class="sxs-lookup"><span data-stu-id="43d76-192">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="43d76-193">Los anfitriones se exponen en el contenido web en un control WebView2 mediante `CoreWebView2.PostWebMessageAsString` o `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="43d76-193">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="43d76-194">Estos mensajes los detectan los controladores agregados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="43d76-194">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="43d76-195">Este mecanismo de comunicación permite que el contenido web transmita mensajes al host mediante capacidades nativas.</span><span class="sxs-lookup"><span data-stu-id="43d76-195">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="43d76-196">En el proyecto, cuando el control WebView2 navega a una dirección URL, muestra la dirección URL en la barra de direcciones y alerta al usuario de la dirección URL que se muestra en el control de WebView2.</span><span class="sxs-lookup"><span data-stu-id="43d76-196">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="43d76-197">En **MainWindow.Xaml.CS**, actualice el constructor y cree una `InitializeAsync` función tal como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="43d76-197">In **MainWindow.xaml.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="43d76-198">La `InitializeAsync` función espera [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) porque la inicialización `CoreWebView2` es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="43d76-198">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  
    
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
    
1.  <span data-ttu-id="43d76-199">Después de inicializar **CoreWebView2** , registra un controlador de eventos para responder `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="43d76-199">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="43d76-200">En **MainWindow.Xaml.CS**, actualice `InitializeAsync` y agregue `UpdateAddressBar` con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="43d76-200">In **MainWindow.xaml.cs**, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="43d76-201">Para que la vista Web pueda enviar y responder al mensaje Web, después de que `CoreWebView2` se inicialice, el host:</span><span class="sxs-lookup"><span data-stu-id="43d76-201">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  
    
    1.  <span data-ttu-id="43d76-202">Inserta un script en el contenido web que registra un controlador para imprimir el mensaje desde el host.</span><span class="sxs-lookup"><span data-stu-id="43d76-202">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    1.  <span data-ttu-id="43d76-203">Inserta un script en el contenido web que publica la dirección URL en el host.</span><span class="sxs-lookup"><span data-stu-id="43d76-203">Injects a script to the web content that posts the URL to the host.</span></span>  
    
    <span data-ttu-id="43d76-204">En `MainWindow.xaml.cs` , actualice `InitializeAsync` como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="43d76-204">In `MainWindow.xaml.cs`, update `InitializeAsync` as follows:</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    <span data-ttu-id="43d76-205">Pulse `F5` para compilar y ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="43d76-205">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="43d76-206">Ahora, la barra de direcciones muestra el URI en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="43d76-206">Now, the address bar displays the URI in the WebView2 control.</span></span> <span data-ttu-id="43d76-207">Cuando navegue correctamente a un nuevo URI, el control WebView2 alerta al usuario del URI que se muestra en el control de WebView2.</span><span class="sxs-lookup"><span data-stu-id="43d76-207">When you successfully navigate to a new URI, the WebView2 control alerts the user of the URI that's displayed in the WebView2 control.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="Direcciones":::
       <span data-ttu-id="43d76-209">Direcciones</span><span class="sxs-lookup"><span data-stu-id="43d76-209">addressBar</span></span>
    :::image-end:::

<span data-ttu-id="43d76-210">¡ Enhorabuena! has creado tu primera WebView2 aplicación.</span><span class="sxs-lookup"><span data-stu-id="43d76-210">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="43d76-211">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="43d76-211">Next steps</span></span>  

*   <span data-ttu-id="43d76-212">Para obtener un ejemplo completo de las capacidades de WebView2, consulta [repositorio de WebView2Samples](https://github.com/MicrosoftEdge/WebView2Samples) en github.</span><span class="sxs-lookup"><span data-stu-id="43d76-212">For a comprehensive example of WebView2 capabilities, see [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) on GitHub.</span></span>  
*   <span data-ttu-id="43d76-213">Para obtener información más detallada sobre las API de WebView2, consulta referencia de la [API](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span><span class="sxs-lookup"><span data-stu-id="43d76-213">For more detailed information about WebView2 APIs, see [API reference](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span></span>  
*   <span data-ttu-id="43d76-214">Para obtener más información sobre WebView2, consulte [recursos WebView2](../index.md#next-steps).</span><span class="sxs-lookup"><span data-stu-id="43d76-214">For more information about  WebView2, see [WebView2 Resources](../index.md#next-steps).</span></span>  

## <span data-ttu-id="43d76-215">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="43d76-215">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  


<!-- links -->  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador de WebView2" 

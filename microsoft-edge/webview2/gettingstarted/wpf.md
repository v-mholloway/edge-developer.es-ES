---
description: Hospedar contenido web en la aplicación WPF con el control de WebView 2 de Microsoft Edge
title: Vista previa de Microsoft Edge 2 para aplicaciones de WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicaciones WPF, WPF, Edge, CoreWebView2, control de explorador, código HTML de Edge, introducción, .NET
ms.openlocfilehash: 01d92322a85e38dab3c502e8dd76729fef8400b1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655182"
---
# <span data-ttu-id="48cf3-104">Introducción a WebView2 en WPF (vista previa)</span><span class="sxs-lookup"><span data-stu-id="48cf3-104">Getting Started with WebView2 in WPF (Preview)</span></span>  

<span data-ttu-id="48cf3-105">En este artículo, empiece a crear su primera aplicación de WebView2 y obtenga información sobre las características principales de [WebView2 (versión preliminar)](/microsoft-edge/hosting/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="48cf3-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/hosting/webview2/index).</span></span>  <span data-ttu-id="48cf3-106">Para obtener más información sobre las API individuales, consulta referencia de la [API](../reference/dotnet/0-9-515-reference-webview2.md).</span><span class="sxs-lookup"><span data-stu-id="48cf3-106">For more information on individual APIs, see [API reference](../reference/dotnet/0-9-515-reference-webview2.md).</span></span>  

## <span data-ttu-id="48cf3-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="48cf3-107">Prerequisites</span></span>  

<span data-ttu-id="48cf3-108">Asegúrese de haber instalado la siguiente lista de requisitos previos antes de continuar:</span><span class="sxs-lookup"><span data-stu-id="48cf3-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="48cf3-109">[Microsoft Edge (cromo)](https://www.microsoftedgeinsider.com/download/) instalado en Windows 10, Windows 8,1 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="48cf3-109">[Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) installed on Windows 10, Windows 8.1, or Windows 7.</span></span>  <span data-ttu-id="48cf3-110">El equipo de WebView de Microsoft Edge recomienda el uso del canal Canarias.</span><span class="sxs-lookup"><span data-stu-id="48cf3-110">The Microsoft Edge WebView team recommends using the Canary channel.</span></span>  
* <span data-ttu-id="48cf3-111">[Visual Studio](https://visualstudio.microsoft.com/) 2015 o posterior.</span><span class="sxs-lookup"><span data-stu-id="48cf3-111">[Visual Studio](https://visualstudio.microsoft.com/) 2015 or later.</span></span>  

## <span data-ttu-id="48cf3-112">Paso 1: crear una aplicación de una sola ventana</span><span class="sxs-lookup"><span data-stu-id="48cf3-112">Step 1 - Create a single window application</span></span>

<span data-ttu-id="48cf3-113">Empiece con un proyecto de escritorio básico que contenga una única ventana principal.</span><span class="sxs-lookup"><span data-stu-id="48cf3-113">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="48cf3-114">Abra **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="48cf3-114">Open **Visual Studio.**</span></span>
2. <span data-ttu-id="48cf3-115">Elija aplicación **.net Core de WPF** o **aplicación .NET Framework de WPF**y, a continuación, elija **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="48cf3-115">Choose **WPF .NET Core App** or **WPF .NET Framework App**, and then choose **Next**.</span></span>  

    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="WPF Core":::
             <span data-ttu-id="48cf3-117">WPF Core</span><span class="sxs-lookup"><span data-stu-id="48cf3-117">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Marco WPF":::
             <span data-ttu-id="48cf3-119">Marco WPF</span><span class="sxs-lookup"><span data-stu-id="48cf3-119">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::

3. <span data-ttu-id="48cf3-120">Escriba los valores para **el nombre** y la **Ubicación**del proyecto.</span><span class="sxs-lookup"><span data-stu-id="48cf3-120">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="48cf3-121">Seleccione .NET Framework 4.6.2 o posterior o .NET Core 3,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="48cf3-121">Select .NET Framework 4.6.2 or later, or .NET Core 3.0 or later.</span></span>  

:::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Crear núcleo":::
             <span data-ttu-id="48cf3-123">Crear núcleo</span><span class="sxs-lookup"><span data-stu-id="48cf3-123">Create core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Crear marco de trabajo":::
             <span data-ttu-id="48cf3-125">Crear marco de trabajo</span><span class="sxs-lookup"><span data-stu-id="48cf3-125">Create Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::

4. <span data-ttu-id="48cf3-126">Elija **crear** para crear el proyecto.</span><span class="sxs-lookup"><span data-stu-id="48cf3-126">Choose **Create** to create your project.</span></span>  

## <span data-ttu-id="48cf3-127">Paso 2: instalar el SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="48cf3-127">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="48cf3-128">A continuación, agregue el SDK de WebView2 al proyecto.</span><span class="sxs-lookup"><span data-stu-id="48cf3-128">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="48cf3-129">Para obtener la vista previa, instala el SDK de WebView2 con Nuget.</span><span class="sxs-lookup"><span data-stu-id="48cf3-129">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="48cf3-130">Abra el menú contextual en el proyecto \ (haga clic con el botón derecho \) y elija **administrar paquetes NuGet...**.</span><span class="sxs-lookup"><span data-stu-id="48cf3-130">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Nuget":::
       <span data-ttu-id="48cf3-132">Nuget</span><span class="sxs-lookup"><span data-stu-id="48cf3-132">Nuget</span></span> :::image-end:::

2. <span data-ttu-id="48cf3-133">Escriba `Microsoft.Web.WebView2` en la barra de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="48cf3-133">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="48cf3-134">Seleccione **Microsoft. Web. WebView2** en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="48cf3-134">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  <span data-ttu-id="48cf3-135">Establezca la versión del paquete como **versión preliminar**y, a continuación, elija **instalar**.</span><span class="sxs-lookup"><span data-stu-id="48cf3-135">Set the package version to **pre-release**, and then choose **Install**.</span></span>  

     ![Nuget](./media/installnuget.PNG)

<span data-ttu-id="48cf3-137">Ya está todo listo para empezar a desarrollar aplicaciones con la API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="48cf3-137">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="48cf3-138">Pulse `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="48cf3-138">Press `F5` to build and run the project.</span></span>  <span data-ttu-id="48cf3-139">El proyecto en ejecución muestra una ventana vacía.</span><span class="sxs-lookup"><span data-stu-id="48cf3-139">The running project displays an empty window.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Aplicación vacía":::
   <span data-ttu-id="48cf3-141">Aplicación vacía</span><span class="sxs-lookup"><span data-stu-id="48cf3-141">Empty app</span></span>
:::image-end:::

## <span data-ttu-id="48cf3-142">Paso 3: crear una sola vista previa en MainWindow. Xaml</span><span class="sxs-lookup"><span data-stu-id="48cf3-142">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="48cf3-143">A continuación, agregue una vista de vista a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="48cf3-143">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="48cf3-144">Abra `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="48cf3-144">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="48cf3-145">Agrega el espacio de nombres XAML WebView2 insertando la siguiente línea dentro de la `<Window/>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="48cf3-145">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  

    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  

    <span data-ttu-id="48cf3-146">Confirme que el código de `MainWindow.xaml` la es similar al siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="48cf3-146">Confirm that the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  

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
        />
        <Grid>

                </Grid>
    </Window>
    ```  

2. <span data-ttu-id="48cf3-147">Agregue el control WebView2 reemplazando las `<Grid>` etiquetas, con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="48cf3-147">Add the WebView2 control by replacing the `<Grid>` tags, with the following code snippet.</span></span>  <span data-ttu-id="48cf3-148">La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="48cf3-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  

    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  

3. <span data-ttu-id="48cf3-149">Pulse `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="48cf3-149">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="48cf3-150">Confirme que se muestra el control WebView2 [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="48cf3-150">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="48cf3-152">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="48cf3-152">Microsoft.com</span></span> :::image-end:::

## <span data-ttu-id="48cf3-153">Paso 4: navegación</span><span class="sxs-lookup"><span data-stu-id="48cf3-153">Step 4 - Navigation</span></span>  

<span data-ttu-id="48cf3-154">Agregue una barra de direcciones a la aplicación para permitir a los usuarios que cambien la dirección URL que muestra el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="48cf3-154">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="48cf3-155">En **MainWindow. Xaml**, agregue una barra de direcciones copiando y pegando el siguiente fragmento de código dentro de la DockPanel que contiene la vista de gráfico.</span><span class="sxs-lookup"><span data-stu-id="48cf3-155">In **MainWindow.xaml**, add an address bar by copying and pasting the following code snippet inside the DockPanel that contains the WebView.</span></span>  

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

<span data-ttu-id="48cf3-156">Confirme que la `DockPanel` sección de `MainWindow.xaml` aparece como el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="48cf3-156">Confirm that the `DockPanel` section of `MainWindow.xaml` looks like the following code snippet.</span></span>  

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

2. <span data-ttu-id="48cf3-157">Abrir `MainWindow.xaml.cs` en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="48cf3-157">Open `MainWindow.xaml.cs` in Visual Studio.</span></span>  <span data-ttu-id="48cf3-158">Para agregar el `CoreWebView2` espacio de nombres, inserte el siguiente fragmento de código en la parte superior de `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="48cf3-158">Add the `CoreWebView2` namespace by inserting the following code snippet at the top of `MainWindow.xaml.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

3. <span data-ttu-id="48cf3-159">En **MainWindow.Xaml.CS**, copie el siguiente fragmento de código para crear el `ButtonGo_Click` método, que navega por la vista en vista previa a la dirección URL que se escribe en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="48cf3-159">In **MainWindow.xaml.cs**, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  

    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="48cf3-160">Pulse `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="48cf3-160">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="48cf3-161">Escriba una nueva dirección URL en la barra de direcciones y haga clic en **ir**.</span><span class="sxs-lookup"><span data-stu-id="48cf3-161">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="48cf3-162">Por ejemplo, escriba `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="48cf3-162">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="48cf3-163">Confirme que el control WebView2 se desplaza hasta la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="48cf3-163">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="48cf3-164">Asegúrese de que se escribe una dirección URL completa en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="48cf3-164">Make sure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="48cf3-165">`ArgumentException`Se inicia una si la dirección URL no comienza con `http://` o</span><span class="sxs-lookup"><span data-stu-id="48cf3-165">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
   <span data-ttu-id="48cf3-167">Bing</span><span class="sxs-lookup"><span data-stu-id="48cf3-167">Bing</span></span>
:::image-end:::

## <span data-ttu-id="48cf3-168">Paso 5: eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="48cf3-168">Step 5 - Navigation events</span></span>  

<span data-ttu-id="48cf3-169">La aplicación que hospeda los controles WebView2 escucha los siguientes eventos provocados por el control WebView2 durante la navegación a páginas Web.</span><span class="sxs-lookup"><span data-stu-id="48cf3-169">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="48cf3-170">Para obtener más información, vea [eventos de navegación](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span><span class="sxs-lookup"><span data-stu-id="48cf3-170">For more information, see [Navigation Events](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación":::
   <span data-ttu-id="48cf3-172">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="48cf3-172">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="48cf3-173">Cuando se produce un error, se producen los eventos siguientes y puede que dependan de la navegación a una página de error.</span><span class="sxs-lookup"><span data-stu-id="48cf3-173">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="48cf3-174">Cuando hay una redirección de HTTP, hay varios `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="48cf3-174">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="48cf3-175">Para mostrar cómo usar estos eventos, comienza registrando un controlador para `NavigationStarting` que cancele todas las solicitudes que no usen https.</span><span class="sxs-lookup"><span data-stu-id="48cf3-175">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="48cf3-176">En `MainWindow.xaml.cs` , modifique el constructor como se muestra a continuación y agregue la `EnsureHttps` función.</span><span class="sxs-lookup"><span data-stu-id="48cf3-176">In `MainWindow.xaml.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="48cf3-177">En el constructor, EnsureHttps se registra como el controlador de eventos en el `NavigationStarting` evento en el control de WebView2.</span><span class="sxs-lookup"><span data-stu-id="48cf3-177">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="48cf3-178">Pulse `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="48cf3-178">Press `F5` to build and run your project.</span></span> <span data-ttu-id="48cf3-179">Confirme que, al navegar a un sitio HTTP, la WebView no sufre **cambios**.</span><span class="sxs-lookup"><span data-stu-id="48cf3-179">Confirm that when navigating to an HTTP site, the WebView **remains unchanged**.</span></span> <span data-ttu-id="48cf3-180">Sin embargo, la vista Web se desplazará a sitios HTTPS.</span><span class="sxs-lookup"><span data-stu-id="48cf3-180">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="48cf3-181">Paso 6: scripting</span><span class="sxs-lookup"><span data-stu-id="48cf3-181">Step 6 - Scripting</span></span>  

<span data-ttu-id="48cf3-182">Puede usar aplicaciones host para inyectar código JavaScript en controles WebView2 en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="48cf3-182">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="48cf3-183">El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a los fotogramas secundarios hasta que se quite el JavaScript.</span><span class="sxs-lookup"><span data-stu-id="48cf3-183">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="48cf3-184">El código JavaScript insertado se ejecuta después de la creación del objeto global y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="48cf3-184">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="48cf3-185">Puede usar scripting para avisar al usuario cuando navegue a un sitio que no es HTTPS.</span><span class="sxs-lookup"><span data-stu-id="48cf3-185">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="48cf3-186">Modifique la `EnsureHttps` función para que inserte el script en el contenido web con el método [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) .</span><span class="sxs-lookup"><span data-stu-id="48cf3-186">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) method.</span></span>  

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

<span data-ttu-id="48cf3-187">Pulse `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="48cf3-187">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="48cf3-188">Confirme que la aplicación muestra una alerta cuando se desplaza a un sitio que no usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="48cf3-188">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="48cf3-190">HTTPS</span><span class="sxs-lookup"><span data-stu-id="48cf3-190">HTTPS</span></span>
:::image-end:::

## <span data-ttu-id="48cf3-191">Paso 7: comunicación entre el host y el contenido web</span><span class="sxs-lookup"><span data-stu-id="48cf3-191">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="48cf3-192">El host y el contenido web pueden comunicarse entre sí mediante las `postMessage` siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="48cf3-192">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="48cf3-193">El contenido Web de un control WebView2 puede publicar un mensaje en el host mediante `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="48cf3-193">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="48cf3-194">El anfitrión controla el mensaje con cualquier registro `WebMessageReceived` en el host.</span><span class="sxs-lookup"><span data-stu-id="48cf3-194">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="48cf3-195">Los anfitriones se exponen en el contenido web en un control WebView2 mediante `CoreWebView2.PostWebMessageAsString` o `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="48cf3-195">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="48cf3-196">Estos mensajes los detectan los controladores agregados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="48cf3-196">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="48cf3-197">Este mecanismo de comunicación permite que el contenido web transmita mensajes al host mediante capacidades nativas.</span><span class="sxs-lookup"><span data-stu-id="48cf3-197">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="48cf3-198">En el proyecto, cuando el control WebView2 navega a una dirección URL, muestra la dirección URL en la barra de direcciones y alerta al usuario de la dirección URL que se muestra en el control de WebView2.</span><span class="sxs-lookup"><span data-stu-id="48cf3-198">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="48cf3-199">En **MainWindow.Xaml.CS**, actualice el constructor y cree una `InitializeAsync` función tal como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="48cf3-199">In **MainWindow.xaml.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="48cf3-200">La `InitializeAsync` función espera [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) porque la inicialización `CoreWebView2` es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="48cf3-200">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

2. <span data-ttu-id="48cf3-201">Después de inicializar **CoreWebView2** , registra un controlador de eventos para responder `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="48cf3-201">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="48cf3-202">En la actualización de **MainWindow.Xaml.CS** `InitializeAsync` y agregue `UpdateAddressBar` con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="48cf3-202">In **MainWindow.xaml.cs** update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

3. <span data-ttu-id="48cf3-203">Para que la vista Web pueda enviar y responder al mensaje Web, después de que `CoreWebView2` se inicialice, el host:</span><span class="sxs-lookup"><span data-stu-id="48cf3-203">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  

    1. <span data-ttu-id="48cf3-204">Inserta un script en el contenido web que registra un controlador para imprimir el mensaje desde el host.</span><span class="sxs-lookup"><span data-stu-id="48cf3-204">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    2. <span data-ttu-id="48cf3-205">Inserta un script en el contenido web que publica la dirección URL en el host.</span><span class="sxs-lookup"><span data-stu-id="48cf3-205">Injects a script to the web content that posts the URL to the host.</span></span>  

<span data-ttu-id="48cf3-206">En `MainWindow.xaml.cs` , actualice `InitializeAsync` como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="48cf3-206">In `MainWindow.xaml.cs`, update `InitializeAsync` as follows:</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="48cf3-207">Pulse `F5` para compilar y ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="48cf3-207">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="48cf3-208">Ahora la barra de direcciones muestra el URI en la vista de vista previa y, al navegar correctamente a un nuevo URI, la WebView alerta al usuario del URI que se muestra en la vista de vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="48cf3-208">Now the address bar displays the URI in the WebView and when you successfully navigate to a new URI, the WebView alerts the user of the URI displayed in the WebView.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="Direcciones":::
   <span data-ttu-id="48cf3-210">Direcciones</span><span class="sxs-lookup"><span data-stu-id="48cf3-210">addressBar</span></span>
:::image-end:::

<span data-ttu-id="48cf3-211">¡ Enhorabuena! has creado tu primera WebView2 aplicación.</span><span class="sxs-lookup"><span data-stu-id="48cf3-211">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="48cf3-212">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="48cf3-212">Next Steps</span></span>  

<span data-ttu-id="48cf3-213">Existen numerosas funcionalidades de WebView2 que no se cubren en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="48cf3-213">There are plenty of WebView2 functionalities that are not covered in this walkthrough.</span></span>  

<span data-ttu-id="48cf3-214">Para obtener más información:</span><span class="sxs-lookup"><span data-stu-id="48cf3-214">To learn more:</span></span>  

* <span data-ttu-id="48cf3-215">Para obtener información detallada sobre cada API, [consulta la referencia](../reference/dotnet/0-9-515-reference-webview2.md) de la API.</span><span class="sxs-lookup"><span data-stu-id="48cf3-215">Please explore [API reference](../reference/dotnet/0-9-515-reference-webview2.md) for detailed information about each API.</span></span>  

## <span data-ttu-id="48cf3-216">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="48cf3-216">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="48cf3-217">Ayuda a crear una experiencia WebView2 más rica compartiendo tus comentarios.</span><span class="sxs-lookup"><span data-stu-id="48cf3-217">Help build a richer WebView2 experience by sharing your feedback!</span></span>  <span data-ttu-id="48cf3-218">Visite el [repositorio de comentarios](https://aka.ms/webviewfeedback) de WebView de Microsoft Edge para enviar solicitudes de características o informes de errores o buscar problemas conocidos.</span><span class="sxs-lookup"><span data-stu-id="48cf3-218">Visit the Microsoft Edge WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>  

---
description: Guía de introducción a WebView2 para aplicaciones WPF
title: Introducción a WebView2 para aplicaciones WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, aplicaciones wpf, wpf, edge, CoreWebView2, control de explorador, html perimetral, introducción, introducción, .NET
ms.openlocfilehash: e7ddb3977d34e8150a10354e638226bcf96d610d
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536214"
---
# <a name="get-started-with-webview2-in-wpf"></a><span data-ttu-id="f3299-104">Introducción a WebView2 en WPF</span><span class="sxs-lookup"><span data-stu-id="f3299-104">Get started with WebView2 in WPF</span></span>

<span data-ttu-id="f3299-105">En este artículo, empieza a crear tu primera aplicación WebView2 y obtén información sobre las características principales de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="f3299-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="f3299-106">Para obtener más información sobre las API individuales, vaya a [Referencia de api][DotnetApiMicrosoftWebWebview2Wpf].</span><span class="sxs-lookup"><span data-stu-id="f3299-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Wpf].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="f3299-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f3299-107">Prerequisites</span></span>  

<span data-ttu-id="f3299-108">Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="f3299-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="f3299-109">[WebView2 Runtime][Webview2Installer] o cualquier canal no estable de [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado en el sistema operativo compatible \(actualmente Windows 10, Windows 8.1 y Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="f3299-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
*   <span data-ttu-id="f3299-110">[Visual Studio][MicrosoftVisualstudioMain] 2017 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f3299-110">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
## <a name="step-1---create-a-single-window-app"></a><span data-ttu-id="f3299-111">Paso 1: Crear una aplicación de una sola ventana</span><span class="sxs-lookup"><span data-stu-id="f3299-111">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="f3299-112">Comience con un proyecto de escritorio básico que contenga una sola ventana principal.</span><span class="sxs-lookup"><span data-stu-id="f3299-112">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="f3299-113">En Visual Studio, elija **WPF .NET Core App** \(or **WPF .NET Framework App**\) > **Next**.</span><span class="sxs-lookup"><span data-stu-id="f3299-113">In Visual Studio, choose **WPF .NET Core App** \(or **WPF .NET Framework App**\) > **Next**.</span></span>  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-wpf-core.png" alt-text="Núcleo de WPF":::
             <span data-ttu-id="f3299-115">Núcleo de WPF</span><span class="sxs-lookup"><span data-stu-id="f3299-115">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-wpf-fw.png" alt-text="Marco WPF":::
             <span data-ttu-id="f3299-117">Marco WPF</span><span class="sxs-lookup"><span data-stu-id="f3299-117">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="f3299-118">Escriba valores para **Nombre del proyecto y** **Ubicación**.</span><span class="sxs-lookup"><span data-stu-id="f3299-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="f3299-119">Elija **.NET Framework 4.6.2** o posterior **\(o .NET Core 3.0** o posterior\).</span><span class="sxs-lookup"><span data-stu-id="f3299-119">Choose **.NET Framework 4.6.2** or later \(or **.NET Core 3.0** or later\).</span></span>  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-create-core.png" alt-text="Crear núcleo":::
             <span data-ttu-id="f3299-121">Crear núcleo</span><span class="sxs-lookup"><span data-stu-id="f3299-121">Create core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-create-fw.png" alt-text="Crear marco":::
             <span data-ttu-id="f3299-123">Crear marco</span><span class="sxs-lookup"><span data-stu-id="f3299-123">Create Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="f3299-124">Para crear el proyecto, elija **Crear**.</span><span class="sxs-lookup"><span data-stu-id="f3299-124">To create your project, choose **Create**.</span></span>  
    
## <a name="step-2---install-webview2-sdk"></a><span data-ttu-id="f3299-125">Paso 2: Instalar WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="f3299-125">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="f3299-126">Use NuGet para agregar el SDK de WebView2 al proyecto.</span><span class="sxs-lookup"><span data-stu-id="f3299-126">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="f3299-127">Mantenga el mouse sobre el proyecto, abra el menú contextual \(haga clic con el botón secundario\) y elija **Administrar paquetes NuGet...**.</span><span class="sxs-lookup"><span data-stu-id="f3299-127">Hover on the projecty, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-getting-started-mng-nuget.png" alt-text="Administrar paquetes NuGet" lightbox="./media/wpf-getting-started-mng-nuget.png":::
       <span data-ttu-id="f3299-129">Administrar paquetes NuGet</span><span class="sxs-lookup"><span data-stu-id="f3299-129">Manage NuGet packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="f3299-130">En la barra de búsqueda, `Microsoft.Web.WebView2` escriba > **elija Microsoft.Web.WebView2**.</span><span class="sxs-lookup"><span data-stu-id="f3299-130">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    
    :::image type="complex" source="./media/install-nuget.png" alt-text="NuGet" lightbox="./media/install-nuget.png":::
       <span data-ttu-id="f3299-132">NuGet</span><span class="sxs-lookup"><span data-stu-id="f3299-132">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="f3299-133">Listo para empezar a desarrollar aplicaciones con la API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="f3299-133">Ready to start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="f3299-134">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="f3299-134">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="f3299-135">El proyecto en ejecución muestra una ventana vacía.</span><span class="sxs-lookup"><span data-stu-id="f3299-135">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/winforms-empty-app.png" alt-text="Aplicación vacía" lightbox="./media/winforms-empty-app.png":::
       <span data-ttu-id="f3299-137">Aplicación vacía</span><span class="sxs-lookup"><span data-stu-id="f3299-137">Empty app</span></span>  
    :::image-end:::  
    
## <a name="step-3---create-a-single-webview"></a><span data-ttu-id="f3299-138">Paso 3: Crear un único WebView</span><span class="sxs-lookup"><span data-stu-id="f3299-138">Step 3 - Create a single WebView</span></span> 

<span data-ttu-id="f3299-139">A continuación, agregue un WebView a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f3299-139">Next add a WebView to your app.</span></span>  

1.  <span data-ttu-id="f3299-140">En el `MainWindow.xaml` archivo, para agregar el espacio de nombres XAML webView2, inserte la siguiente línea dentro de la `<Window/>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="f3299-140">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    <span data-ttu-id="f3299-141">Asegúrese de que el código de `MainWindow.xaml` es similar al siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="f3299-141">Ensure the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="f3299-142">Para agregar el control WebView2, reemplace las `<Grid>` etiquetas por el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="f3299-142">To add the WebView2 control, replace the `<Grid>` tags with the following code snippet.</span></span>  <span data-ttu-id="f3299-143">La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="f3299-143">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  <span data-ttu-id="f3299-144">Para compilar y ejecutar el proyecto, seleccione `F5`  Asegurarse de que el control WebView2 muestre [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="f3299-144">To build and run the project, select `F5`  Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/wpf-getting-started-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="f3299-146">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="f3299-146">Microsoft.com</span></span>
    :::image-end:::  
    
## <a name="step-4---navigation"></a><span data-ttu-id="f3299-147">Paso 4: navegación</span><span class="sxs-lookup"><span data-stu-id="f3299-147">Step 4 - Navigation</span></span>  

<span data-ttu-id="f3299-148">Agregue la capacidad de permitir a los usuarios cambiar la dirección URL que muestra el control WebView2 agregando una barra de direcciones a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f3299-148">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="f3299-149">En el archivo, agregue una barra de direcciones copiando y pegando el siguiente fragmento de código dentro del `MainWindow.xaml` `<DockPanel>` que contiene WebView.</span><span class="sxs-lookup"><span data-stu-id="f3299-149">In the `MainWindow.xaml` file, add an address bar by copying and pasting the following code snippet inside the `<DockPanel>` that contains the WebView.</span></span>  
    
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
    
    <span data-ttu-id="f3299-150">Asegúrese de `<DockPanel>` que la sección del archivo coincide con el siguiente fragmento de `MainWindow.xaml` código.</span><span class="sxs-lookup"><span data-stu-id="f3299-150">Ensure the `<DockPanel>` section of the `MainWindow.xaml` file matches the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="f3299-151">En Visual Studio, en el archivo, para agregar el espacio de nombres, inserte el siguiente fragmento de código `MainWindow.xaml.cs` `CoreWebView2` en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="f3299-151">In Visual Studio, in the `MainWindow.xaml.cs` file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  <span data-ttu-id="f3299-152">En el archivo, copie el siguiente fragmento de código para crear el método, que navega webview a la `MainWindow.xaml.cs` dirección URL especificada en la barra de `ButtonGo_Click` direcciones.</span><span class="sxs-lookup"><span data-stu-id="f3299-152">In the `MainWindow.xaml.cs`file, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    <span data-ttu-id="f3299-153">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="f3299-153">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="f3299-154">Escriba una nueva dirección URL en la barra de direcciones y elija **Ir**.</span><span class="sxs-lookup"><span data-stu-id="f3299-154">Type a new URL in the address bar and choose **Go**.</span></span>  <span data-ttu-id="f3299-155">Por ejemplo, escribe `https://www.bing.com`.</span><span class="sxs-lookup"><span data-stu-id="f3299-155">For example, type `https://www.bing.com`.</span></span>  <span data-ttu-id="f3299-156">Asegúrese de que el control WebView2 navega a la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f3299-156">Ensure the WebView2 control navigates to the URL.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f3299-157">Asegúrese de que se ha escrito una dirección URL completa en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f3299-157">Make sure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="f3299-158">Se `ArgumentException` produce un error si la dirección URL no comienza con o `http://` `https://` .</span><span class="sxs-lookup"><span data-stu-id="f3299-158">An `ArgumentException` is thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/wpf-getting-started-bing.png" alt-text="Bing":::
       <span data-ttu-id="f3299-160">bing.com</span><span class="sxs-lookup"><span data-stu-id="f3299-160">bing.com</span></span>
    :::image-end:::
    
## <a name="step-5---navigation-events"></a><span data-ttu-id="f3299-161">Paso 5: eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="f3299-161">Step 5 - Navigation events</span></span>  

<span data-ttu-id="f3299-162">Durante la navegación por la página web, el control WebView2 genera eventos.</span><span class="sxs-lookup"><span data-stu-id="f3299-162">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="f3299-163">La aplicación que hospeda los controles WebView2 escucha los siguientes eventos.</span><span class="sxs-lookup"><span data-stu-id="f3299-163">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  
    
<span data-ttu-id="f3299-164">Para obtener más información, vaya a [Eventos de navegación][Webview2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="f3299-164">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación":::
   <span data-ttu-id="f3299-166">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="f3299-166">Navigation events</span></span>
:::image-end:::  

<span data-ttu-id="f3299-167">Cuando se produce un error, se producen los siguientes eventos y pueden depender de la navegación a una página web de error.</span><span class="sxs-lookup"><span data-stu-id="f3299-167">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
    
> [!NOTE]
> <span data-ttu-id="f3299-168">Si se produce un redireccionamiento HTTP, hay varios `NavigationStarting` eventos en una fila.</span><span class="sxs-lookup"><span data-stu-id="f3299-168">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="f3299-169">Para demostrar cómo usar los eventos, registre un controlador para que cancele las solicitudes que no son `NavigationStarting` HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f3299-169">To demonstrate how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  

<span data-ttu-id="f3299-170">En el `MainWindow.xaml.cs` archivo, modifique el constructor para que coincida con el siguiente fragmento de código y agregue la `EnsureHttps` función.</span><span class="sxs-lookup"><span data-stu-id="f3299-170">In the `MainWindow.xaml.cs` file, modify the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="f3299-171">En el constructor, `EnsureHttps` se registra como el controlador de eventos en el evento en el control `NavigationStarting` WebView2.</span><span class="sxs-lookup"><span data-stu-id="f3299-171">In the constructor, `EnsureHttps` is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="f3299-172">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="f3299-172">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="f3299-173">Asegúrese de que al navegar a un sitio HTTP, webView permanece sin cambios.</span><span class="sxs-lookup"><span data-stu-id="f3299-173">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="f3299-174">Sin embargo, WebView navega a sitios HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f3299-174">However, the WebView navigates to HTTPS sites.</span></span>  

## <a name="step-6---scripting"></a><span data-ttu-id="f3299-175">Paso 6: Scripting</span><span class="sxs-lookup"><span data-stu-id="f3299-175">Step 6 - Scripting</span></span>  

<span data-ttu-id="f3299-176">Puede usar aplicaciones host para insertar código JavaScript en controles WebView2 en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f3299-176">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="f3299-177">Puede realizar la tarea WebView para ejecutar JavaScript arbitrario o agregar scripts de inicialización.</span><span class="sxs-lookup"><span data-stu-id="f3299-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="f3299-178">JavaScript inyectado se aplica a todos los nuevos documentos de nivel superior y a los fotogramas secundarios hasta que se quita JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f3299-178">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="f3299-179">JavaScript inyectado se ejecuta con un tiempo específico.</span><span class="sxs-lookup"><span data-stu-id="f3299-179">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="f3299-180">Ejecutarlo después de la creación del objeto global.</span><span class="sxs-lookup"><span data-stu-id="f3299-180">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="f3299-181">Ejecutarlo antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="f3299-181">Run it before any other script included in the HTML document is run.</span></span>  
    
<span data-ttu-id="f3299-182">Por ejemplo, agregue scripts que envíen una alerta cuando un usuario navegue a sitios que no son HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f3299-182">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="f3299-183">Modifique la `EnsureHttps` función para insertar un script en el contenido web que usa el método [ExecuteScriptAsync.](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync)</span><span class="sxs-lookup"><span data-stu-id="f3299-183">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) method.</span></span>  

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

<span data-ttu-id="f3299-184">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="f3299-184">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="f3299-185">Asegúrate de que la aplicación muestra una alerta cuando navegas a un sitio web que no usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f3299-185">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-getting-started-https.png" alt-text="HTTPS":::
   <span data-ttu-id="f3299-187">HTTPS</span><span class="sxs-lookup"><span data-stu-id="f3299-187">HTTPS</span></span>
:::image-end:::  

## <a name="step-7---communication-between-host-and-web-content"></a><span data-ttu-id="f3299-188">Paso 7: comunicación entre contenido de host y web</span><span class="sxs-lookup"><span data-stu-id="f3299-188">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="f3299-189">El contenido de host y web puede comunicarse de las siguientes maneras mediante `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="f3299-189">The host and web content may communicate in the following ways using `postMessage`.</span></span>  

*   <span data-ttu-id="f3299-190">El contenido web de un control WebView2 puede publicar un mensaje en el host mediante `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="f3299-190">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="f3299-191">El host controla el mensaje con cualquier registrado `WebMessageReceived` en el host.</span><span class="sxs-lookup"><span data-stu-id="f3299-191">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="f3299-192">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="f3299-192">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="f3299-193">Los controladores agregados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="f3299-193">The messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  
    
<span data-ttu-id="f3299-194">El mecanismo de comunicación pasa mensajes del contenido web al host mediante funcionalidades nativas.</span><span class="sxs-lookup"><span data-stu-id="f3299-194">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="f3299-195">En el proyecto, cuando el control WebView2 navega a una dirección URL, muestra la dirección URL en la barra de direcciones y alerta al usuario de la dirección URL mostrada en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="f3299-195">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="f3299-196">En el `MainWindow.xaml.cs` archivo, actualice el constructor y cree una `InitializeAsync` función que coincida con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="f3299-196">In the `MainWindow.xaml.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="f3299-197">La `InitializeAsync` función espera [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) porque la inicialización de `CoreWebView2` es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f3299-197">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  
    
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
    
1.  <span data-ttu-id="f3299-198">Después **de inicializar CoreWebView2,** registre un controlador de eventos para responder a `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="f3299-198">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="f3299-199">In `MainWindow.xaml.cs` , update and add using the following code `InitializeAsync` `UpdateAddressBar` snippet.</span><span class="sxs-lookup"><span data-stu-id="f3299-199">In `MainWindow.xaml.cs`, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="f3299-200">Para que WebView envíe y responda al mensaje web, después `CoreWebView2` de inicializarse, el host:</span><span class="sxs-lookup"><span data-stu-id="f3299-200">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  
    1.  <span data-ttu-id="f3299-201">Inserta un script en el contenido web que registra un controlador para imprimir el mensaje desde el host.</span><span class="sxs-lookup"><span data-stu-id="f3299-201">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    1.  <span data-ttu-id="f3299-202">Inserta un script en el contenido web que publica la dirección URL en el host.</span><span class="sxs-lookup"><span data-stu-id="f3299-202">Injects a script to the web content that posts the URL to the host.</span></span>  
        
    <span data-ttu-id="f3299-203">En el `MainWindow.xaml.cs` archivo, actualice `InitializeAsync` para que coincida con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="f3299-203">In the `MainWindow.xaml.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    <span data-ttu-id="f3299-204">Para compilar y ejecutar la aplicación, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="f3299-204">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="f3299-205">Ahora, la barra de direcciones muestra el URI en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="f3299-205">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="f3299-206">Cuando navega correctamente a un nuevo URI, el control WebView2 avisa al usuario del URI que se muestra en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="f3299-206">When you successfully navigate to a new URI, the WebView2 control alerts the user of the URI that's displayed in the WebView2 control.</span></span>  
    
    :::image type="complex" source="./media/wpf-getting-started-searchbar.png" alt-text="addressBar":::
       <span data-ttu-id="f3299-208">addressBar</span><span class="sxs-lookup"><span data-stu-id="f3299-208">addressBar</span></span>
    :::image-end:::
    
<span data-ttu-id="f3299-209">Enhorabuena, has creado tu primera aplicación WebView2.</span><span class="sxs-lookup"><span data-stu-id="f3299-209">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="f3299-210">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="f3299-210">Next steps</span></span>  

<span data-ttu-id="f3299-211">Para seguir aprendiendo más sobre WebView2, vaya a los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="f3299-211">To continue learning more about WebView2, navigate to the following resources.</span></span>  

*   <span data-ttu-id="f3299-212">Para obtener más información sobre cómo crear aplicaciones webView2, vaya a Procedimientos recomendados de desarrollo [de WebView2][WV2BestPractices].</span><span class="sxs-lookup"><span data-stu-id="f3299-212">To learn more about building WebView2 applications, navigate to [WebView2 development best practices][WV2BestPractices].</span></span>  
*   <span data-ttu-id="f3299-213">Para obtener un ejemplo completo de las capacidades de WebView2, vaya al repositorio [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain] en GitHub.</span><span class="sxs-lookup"><span data-stu-id="f3299-213">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samplesMain] on GitHub.</span></span>  
*   <span data-ttu-id="f3299-214">Para obtener información más detallada acerca de la API de WebView2, vaya a [Referencia de API](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span><span class="sxs-lookup"><span data-stu-id="f3299-214">For more detailed information about WebView2 API, navigate to [API reference](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span></span>  
*   <span data-ttu-id="f3299-215">Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2](../index.md#next-steps).</span><span class="sxs-lookup"><span data-stu-id="f3299-215">For more information about  WebView2, navigate to [WebView2 Resources](../index.md#next-steps).</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="f3299-216">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="f3299-216">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  
 
[WV2BestPractices]: ../concepts/developer-guide.md "Procedimientos recomendados de desarrollo de WebView2 | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegación | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Espacio de nombres Microsoft.Web.WebView2.Wpf | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Clase WebView2 | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "Método WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Desarrollador de Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualStudioMain]: https://visualstudio.microsoft.com "Microsoft Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador de WebView2" 

---
description: Guía de introducción a WebView2 para aplicaciones de WinForms
title: Introducción a WebView2 para aplicaciones de WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicaciones de WinForms, WinForms, Edge, CoreWebView2, control de explorador, ASP.net de Edge, introducción, introducción, .NET, Windows Forms
ms.openlocfilehash: f4768c38f293d1931e625136ea7068a61176541e
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182391"
---
# <span data-ttu-id="0bcbf-104">Introducción a WebView2 en Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0bcbf-104">Getting started with WebView2 in Windows Forms</span></span>

<span data-ttu-id="0bcbf-105">En este artículo, empiece a crear su primera aplicación de WebView2 y conozca las características principales de [WebView2](/microsoft-edge/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="0bcbf-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2](/microsoft-edge/webview2/index).</span></span>  <span data-ttu-id="0bcbf-106">Para obtener más información sobre las API individuales, consulta referencia de la [API](/dotnet/api/microsoft.web.webview2.winforms).</span><span class="sxs-lookup"><span data-stu-id="0bcbf-106">For more information on individual APIs, see [API reference](/dotnet/api/microsoft.web.webview2.winforms).</span></span>  

## <span data-ttu-id="0bcbf-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0bcbf-107">Prerequisites</span></span>  

<span data-ttu-id="0bcbf-108">Asegúrese de haber instalado la siguiente lista de requisitos previos antes de continuar:</span><span class="sxs-lookup"><span data-stu-id="0bcbf-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="0bcbf-109">[WebView2 en tiempo de ejecución][Webview2Installer] o cualquier [canal Canarias no estable de Microsoft Edge (cromo)](https://www.microsoftedgeinsider.com/download) instalado en windows 10, Windows 8,1 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-109">[WebView2 Runtime][Webview2Installer] or any [non-stable Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download) installed on Windows 10, Windows 8.1, or Windows 7.</span></span> 
* <span data-ttu-id="0bcbf-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 o posterior.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 or later.</span></span>

> [!NOTE]
> <span data-ttu-id="0bcbf-111">WebView2 actualmente no admite los diseñadores de .NET 5 y .NET Core.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-111">WebView2 currently does not support the .NET 5 and .NET Core designers.</span></span>

## <span data-ttu-id="0bcbf-112">Paso 1: crear una aplicación de una sola ventana</span><span class="sxs-lookup"><span data-stu-id="0bcbf-112">Step 1 - Create a single window application</span></span>

<span data-ttu-id="0bcbf-113">Empiece con un proyecto de escritorio básico que contenga una única ventana principal.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-113">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="0bcbf-114">Abra **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="0bcbf-114">Open **Visual Studio.**</span></span>

1. <span data-ttu-id="0bcbf-115">Elija **aplicación de Windows Forms .NET Framework** y, a continuación, elija **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-115">Choose **Windows Forms .NET Framework App** and then choose **Next**.</span></span>

    ![NewProject](./media/winforms-newproject.png)

1. <span data-ttu-id="0bcbf-117">Escriba los valores para **el nombre** y la **Ubicación**del proyecto.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-117">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="0bcbf-118">Seleccione **.NET Framework 4.6.2** o posterior.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-118">Select **.NET Framework 4.6.2** or later.</span></span>  

    ![startproject](./media/winforms-startproj.png)

1. <span data-ttu-id="0bcbf-120">Elija **crear** para crear el proyecto.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-120">Choose **Create** to create your project.</span></span>

## <span data-ttu-id="0bcbf-121">Paso 2: instalar el SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="0bcbf-121">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="0bcbf-122">A continuación, agregue el SDK de WebView2 al proyecto con NuGet.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-122">Next add the WebView2 SDK to the project using NuGet.</span></span>

1. <span data-ttu-id="0bcbf-123">Abra el menú contextual en el proyecto \ (haga clic con el botón derecho \) y elija **administrar paquetes NuGet...**.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-123">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Administrar paquetes NuGet":::
       <span data-ttu-id="0bcbf-125">Administrar paquetes NuGet</span><span class="sxs-lookup"><span data-stu-id="0bcbf-125">Manage NuGet Packages</span></span> :::image-end:::

1. <span data-ttu-id="0bcbf-126">Escriba `Microsoft.Web.WebView2` en la barra de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-126">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="0bcbf-127">Seleccione **Microsoft. Web. WebView2** en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-127">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  

    ![Nuget](./media/installnuget.png)

<span data-ttu-id="0bcbf-129">Ya está todo listo para empezar a desarrollar aplicaciones con la API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-129">You're all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="0bcbf-130">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-130">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="0bcbf-131">El proyecto en ejecución muestra una ventana vacía.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-131">The running project displays an empty window.</span></span>  

![emptyApp](./media/winforms-emptyApp.png)

## <span data-ttu-id="0bcbf-133">Paso 3: crear un único WebView</span><span class="sxs-lookup"><span data-stu-id="0bcbf-133">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="0bcbf-134">A continuación, agregue una vista de vista a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-134">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="0bcbf-135">Abra el **Diseñador de Windows Forms**.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-135">Open the **Windows Forms Designer**.</span></span>  
1. <span data-ttu-id="0bcbf-136">Busque **WebView2** en el **cuadro de herramientas**.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-136">Search for **WebView2** in the **Toolbox**.</span></span> <span data-ttu-id="0bcbf-137">Arrastre y coloque el control **WebView2** en la aplicación Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-137">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Cuadro de herramientas que muestra WebView2":::
       <span data-ttu-id="0bcbf-139">Cuadro de herramientas que muestra WebView2</span><span class="sxs-lookup"><span data-stu-id="0bcbf-139">Toolbox displaying WebView2</span></span> :::image-end:::  

1. <span data-ttu-id="0bcbf-140">Cambie la `Name` propiedad a `webView` .</span><span class="sxs-lookup"><span data-stu-id="0bcbf-140">Change the `Name` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Propiedades del control WebView2":::
       <span data-ttu-id="0bcbf-142">Propiedades del control WebView2</span><span class="sxs-lookup"><span data-stu-id="0bcbf-142">Properties of the WebView2 control</span></span> :::image-end:::

1. <span data-ttu-id="0bcbf-143">La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-143">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span> <span data-ttu-id="0bcbf-144">Establezca la propiedad Source en</span><span class="sxs-lookup"><span data-stu-id="0bcbf-144">Set the Source property to</span></span> <https://www.microsoft.com>
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Propiedad Source del control WebView2":::
       <span data-ttu-id="0bcbf-146">Propiedad Source del control WebView2</span><span class="sxs-lookup"><span data-stu-id="0bcbf-146">The Source property of the WebView2 control</span></span> :::image-end:::

<span data-ttu-id="0bcbf-147">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-147">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="0bcbf-148">Confirme que se muestra el control WebView2 [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="0bcbf-148">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> <span data-ttu-id="0bcbf-150">Si está trabajando en un monitor de alta definición de PPP, es posible que tenga que [configurar la aplicación de Windows Forms para una compatibilidad con alta definición de PPP](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span><span class="sxs-lookup"><span data-stu-id="0bcbf-150">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span></span>

## <span data-ttu-id="0bcbf-151">Paso 4: controlar los eventos de ajuste de tamaño de la ventana</span><span class="sxs-lookup"><span data-stu-id="0bcbf-151">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="0bcbf-152">Agregue algunos controles más a sus formularios Windows Forms desde el cuadro de herramientas y, a continuación, administre los eventos de tamaño de ventana correctamente.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-152">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1. <span data-ttu-id="0bcbf-153">En el **Diseñador de Windows Forms**, abra el **cuadro de herramientas**</span><span class="sxs-lookup"><span data-stu-id="0bcbf-153">In the **Windows Forms Designer**, open the **Toolbox**</span></span>
1. <span data-ttu-id="0bcbf-154">Arrastre y coloque un **cuadro de texto** en la aplicación de formularios Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-154">Drag and Drop a **TextBox** into the Windows Forms App.</span></span> <span data-ttu-id="0bcbf-155">Asigne un nombre al **cuadro** `addressBar` de texto en la **pestaña propiedades**.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-155">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>
1. <span data-ttu-id="0bcbf-156">Arrastre y coloque un **botón** en la aplicación Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-156">Drag and Drop a **Button** into the Windows Forms App.</span></span> <span data-ttu-id="0bcbf-157">Cambie el texto del **botón** a `Go!` y asígnele el nombre **Button** `goButton` de la **pestaña propiedades**.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-157">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

    <span data-ttu-id="0bcbf-158">La aplicación debe ser similar a la de la siguiente imagen en el diseñador.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-158">The app should look like the following image in the designer.</span></span>
    
    ![diseñador](./media/winforms-designer.png)

1. <span data-ttu-id="0bcbf-160">En **Form1.CS** define `Form_Resize` para mantener los controles en su lugar cuando se cambie el tamaño de la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-160">In **Form1.cs** define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);
}

private void Form_Resize(object sender, EventArgs e)
{
    webView.Size = this.ClientSize - new System.Drawing.Size(webView.Location);
    goButton.Left = this.ClientSize.Width - goButton.Width;
    addressBar.Width = goButton.Left - addressBar.Left;
}
```

<span data-ttu-id="0bcbf-161">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-161">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="0bcbf-162">Confirme que la aplicación se muestra de forma similar a la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-162">Confirm that the app displays similar to the following screenshot.</span></span>

![aplicación](./media/winforms-app.png)

## <span data-ttu-id="0bcbf-164">Paso 5: navegación</span><span class="sxs-lookup"><span data-stu-id="0bcbf-164">Step 5 - Navigation</span></span>

<span data-ttu-id="0bcbf-165">Agregue una barra de direcciones a la aplicación para permitir a los usuarios que cambien la dirección URL que muestra el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-165">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="0bcbf-166">En `Form1.cs` Agregar el `CoreWebView2` espacio de nombres, inserte el siguiente fragmento de código en la parte superior de `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="0bcbf-166">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1. <span data-ttu-id="0bcbf-167">En el **Diseñador de Windows Forms**, haga doble clic en el `Go!` botón para crear el `goButton_Click` método `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="0bcbf-167">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in `Form1.cs`.</span></span> <span data-ttu-id="0bcbf-168">Copie y pegue el siguiente fragmento de código dentro de la función.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-168">Copy and paste the following snippet inside the function.</span></span> <span data-ttu-id="0bcbf-169">Ahora, la `goButton_Click` función navega por la vista WebView a la dirección URL que se escribe en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-169">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="0bcbf-170">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-170">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="0bcbf-171">Escriba una nueva dirección URL en la barra de direcciones y seleccione **ir**.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-171">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="0bcbf-172">Por ejemplo, escriba `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="0bcbf-172">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="0bcbf-173">Confirme que el control WebView2 se desplaza hasta la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-173">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="0bcbf-174">Asegúrese de que se escribe una dirección URL completa en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-174">Ensure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="0bcbf-175">`ArgumentException`Se inicia una si la dirección URL no comienza con `http://` o</span><span class="sxs-lookup"><span data-stu-id="0bcbf-175">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

![bing](./media/winforms-bing.png)

## <span data-ttu-id="0bcbf-177">Paso 6: eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="0bcbf-177">Step 6 - Navigation events</span></span>  

<span data-ttu-id="0bcbf-178">Durante la navegación de páginas web, el control WebView2 desencadena eventos.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-178">During webpage navigation, the WebView2 control raises events.</span></span> <span data-ttu-id="0bcbf-179">La aplicación que hospeda los controles WebView2 escucha los siguientes eventos.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-179">The application that hosts WebView2 controls listens for the following events.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="0bcbf-180">Para obtener más información, vea [eventos de navegación](../concepts/navigation-events.md).</span><span class="sxs-lookup"><span data-stu-id="0bcbf-180">For more information, see [Navigation Events](../concepts/navigation-events.md).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación":::
   <span data-ttu-id="0bcbf-182">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="0bcbf-182">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="0bcbf-183">Cuando se produce un error, se producen los eventos siguientes y puede que dependan de la navegación a una página de error.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-183">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="0bcbf-184">Cuando hay una redirección de HTTP, hay varios `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-184">When there's an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="0bcbf-185">Para mostrar cómo usar estos eventos, comienza registrando un controlador para `NavigationStarting` que cancele todas las solicitudes que no usen https.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-185">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span>  

<span data-ttu-id="0bcbf-186">En `Form1.cs` , modifique el constructor como se muestra a continuación y agregue la `EnsureHttps` función.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-186">In `Form1.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);

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

<span data-ttu-id="0bcbf-187">En el constructor, EnsureHttps se registra como el controlador de eventos en el `NavigationStarting` evento en el control de WebView2.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-187">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="0bcbf-188">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-188">Select `F5` to build and run your project.</span></span> <span data-ttu-id="0bcbf-189">Confirme que, al navegar a un sitio HTTP, la WebView no sufre cambios.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-189">Confirm that when navigating to an HTTP site, the WebView remains unchanged.</span></span> <span data-ttu-id="0bcbf-190">Sin embargo, la vista Web se desplazará a sitios HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-190">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="0bcbf-191">Paso 7: scripting</span><span class="sxs-lookup"><span data-stu-id="0bcbf-191">Step 7 - Scripting</span></span>  

<span data-ttu-id="0bcbf-192">Puede usar aplicaciones host para inyectar código JavaScript en controles WebView2 en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-192">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="0bcbf-193">El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a cualquier fotograma secundario, hasta que se quite el JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-193">The injected JavaScript applies to all new top-level documents and any child frames, until the JavaScript is removed.</span></span>  <span data-ttu-id="0bcbf-194">El código JavaScript insertado se ejecuta después de la creación del objeto global y antes de los scripts incluidos en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-194">The injected JavaScript is run after creation of the global object, and before any scripts included in the HTML document.</span></span>  

<span data-ttu-id="0bcbf-195">Puede usar scripting para avisar al usuario cuando navegue a un sitio que no es HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-195">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="0bcbf-196">Modifique la `EnsureHttps` función para que inserte el script en el contenido web con el método [ExecuteScriptAsync]() .</span><span class="sxs-lookup"><span data-stu-id="0bcbf-196">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync]() method.</span></span>  

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

<span data-ttu-id="0bcbf-197">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-197">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="0bcbf-198">Confirme que la aplicación muestra una alerta cuando navegue a un sitio que no usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-198">Confirm that the application displays an alert when you navigate to a site that doesn't use HTTPS.</span></span>  

![https](./media/winforms-https.png)

## <span data-ttu-id="0bcbf-200">Paso 8: comunicación entre el contenido del host y el Web</span><span class="sxs-lookup"><span data-stu-id="0bcbf-200">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="0bcbf-201">El host y el contenido web pueden comunicarse entre sí mediante las `postMessage` siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="0bcbf-201">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="0bcbf-202">El contenido Web de un control WebView2 puede publicar un mensaje en el host mediante `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="0bcbf-202">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="0bcbf-203">El anfitrión controla el mensaje con cualquier registro `WebMessageReceived` en el host.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-203">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="0bcbf-204">Los anfitriones se exponen en el contenido web en un control WebView2 mediante `CoreWebView2.PostWebMessageAsString` o `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="0bcbf-204">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="0bcbf-205">Estos mensajes los detectan los controladores agregados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="0bcbf-205">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="0bcbf-206">Este mecanismo de comunicación permite que el contenido web transmita mensajes al host mediante capacidades nativas.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-206">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="0bcbf-207">En el proyecto, cuando el control WebView2 navega a una dirección URL, muestra la dirección URL en la barra de direcciones y alerta al usuario de la dirección URL que se muestra en el control de WebView2.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-207">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="0bcbf-208">En **Form1.CS**, actualice el constructor y cree una `InitializeAsync` función tal como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-208">In **Form1.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="0bcbf-209">La `InitializeAsync` función espera [EnsureCoreWebView2Async]() porque la inicialización `CoreWebView2` es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-209">The `InitializeAsync` function awaits [EnsureCoreWebView2Async]() because the initialization of `CoreWebView2` is asynchronous.</span></span>  

    ```csharp
    public Form1()
    {
        InitializeComponent();
        this.Resize += new System.EventHandler(this.Form_Resize);
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }

    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  

1. <span data-ttu-id="0bcbf-210">Después de inicializar **CoreWebView2** , registra un controlador de eventos para responder `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="0bcbf-210">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="0bcbf-211">En `Form1.cs` , actualice `InitializeAsync` y agregue `UpdateAddressBar` con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-211">In `Form1.cs`, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1. <span data-ttu-id="0bcbf-212">Para que la vista Web pueda enviar y responder al mensaje Web, después de que `CoreWebView2` se inicialice, el anfitrión inyecta una secuencia de comandos en el contenido web a:</span><span class="sxs-lookup"><span data-stu-id="0bcbf-212">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1. <span data-ttu-id="0bcbf-213">Envíe la dirección URL al host mediante `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="0bcbf-213">Send the URL to the host using `postMessage`.</span></span>
    1. <span data-ttu-id="0bcbf-214">Registre un controlador de eventos para imprimir un mensaje enviado desde el host.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-214">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="0bcbf-215">En `Form1.cs` , actualice `InitializeAsync` tal como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-215">In `Form1.cs`, update `InitializeAsync` as shown in the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="0bcbf-216">Seleccione `F5` para compilar y ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-216">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="0bcbf-217">Confirme que la barra de direcciones muestra la dirección URL del sitio que se muestra en la vista Web.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-217">Confirm that the address bar displays the URL of the site displayed in the WebView.</span></span> <span data-ttu-id="0bcbf-218">Además, cuando navegues correctamente a una nueva dirección URL, WebView avisará al usuario de la dirección URL que se muestra en la vista de vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-218">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

![finalapp](./media/winforms-finalapp.png)

<span data-ttu-id="0bcbf-220">¡ Enhorabuena! has creado tu primera WebView2 aplicación.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-220">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="0bcbf-221">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="0bcbf-221">Next steps</span></span> 

<span data-ttu-id="0bcbf-222">Para continuar aprendiendo más acerca de WebView2, vaya a los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-222">To continue learning more about WebView2, navigate to the following resources.</span></span>

* <span data-ttu-id="0bcbf-223">El [repositorio de WebView2Samples](https://github.com/MicrosoftEdge/WebView2Samples) tiene un ejemplo completo de las capacidades de WebView2's.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-223">The [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) has a comprehensive example of WebView2's capabilities.</span></span>
* <span data-ttu-id="0bcbf-224">La [referencia](/dotnet/api/microsoft.web.webview2.winforms.webview2) de la API para obtener información más detallada sobre nuestras API.</span><span class="sxs-lookup"><span data-stu-id="0bcbf-224">The [API reference](/dotnet/api/microsoft.web.webview2.winforms.webview2) for more detailed information about our APIs.</span></span>
* <span data-ttu-id="0bcbf-225">[Recursos de WebView2](../index.md#next-steps).</span><span class="sxs-lookup"><span data-stu-id="0bcbf-225">[WebView2 Resources](../index.md#next-steps).</span></span>


## <span data-ttu-id="0bcbf-226">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0bcbf-226">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  


<!-- links -->  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador de WebView2" 

---
description: Guía de introducción a WebView2 para aplicaciones de WinForms
title: Introducción a WebView2 para aplicaciones de WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicaciones de WinForms, WinForms, Edge, CoreWebView2, control de explorador, ASP.net de Edge, introducción, introducción, .NET, Windows Forms
ms.openlocfilehash: e9451d4bfafacf78f723be75379e57400d0ba914
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119083"
---
# <span data-ttu-id="e21bd-104">Introducción a WebView2 en Windows Forms (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="e21bd-104">Getting started with WebView2 in Windows Forms (Preview)</span></span>  

<span data-ttu-id="e21bd-105">En este artículo, empiece a crear su primera aplicación de WebView2 y obtenga información sobre las características principales de [WebView2 (versión preliminar)](/microsoft-edge/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="e21bd-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/webview2/index).</span></span>  <span data-ttu-id="e21bd-106">Para obtener más información sobre las API individuales, consulta referencia de la [API](/dotnet/api/microsoft.web.webview2.winforms).</span><span class="sxs-lookup"><span data-stu-id="e21bd-106">For more information on individual APIs, see [API reference](/dotnet/api/microsoft.web.webview2.winforms).</span></span>  

## <span data-ttu-id="e21bd-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e21bd-107">Prerequisites</span></span>  

<span data-ttu-id="e21bd-108">Asegúrese de haber instalado la siguiente lista de requisitos previos antes de continuar:</span><span class="sxs-lookup"><span data-stu-id="e21bd-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="e21bd-109">[Canal Canarias de Microsoft Edge (cromo)](https://www.microsoftedgeinsider.com/download) instalado en Windows 10, Windows 8,1 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e21bd-109">[Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download) installed on Windows 10, Windows 8.1, or Windows 7.</span></span> 
* <span data-ttu-id="e21bd-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e21bd-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 or later.</span></span>

> [!NOTE]
> <span data-ttu-id="e21bd-111">WebView2 actualmente no es compatible con el diseñador de .NET Core 3.0 [(versión preliminar)](https://visualstudio.microsoft.com/vs/preview).</span><span class="sxs-lookup"><span data-stu-id="e21bd-111">WebView2 does not currently support the .NET Core 3.0's [designer (preview)](https://visualstudio.microsoft.com/vs/preview).</span></span>

## <span data-ttu-id="e21bd-112">Paso 1: crear una aplicación de una sola ventana</span><span class="sxs-lookup"><span data-stu-id="e21bd-112">Step 1 - Create a single window application</span></span>

<span data-ttu-id="e21bd-113">Empiece con un proyecto de escritorio básico que contenga una única ventana principal.</span><span class="sxs-lookup"><span data-stu-id="e21bd-113">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="e21bd-114">Abra **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="e21bd-114">Open **Visual Studio.**</span></span>

1. <span data-ttu-id="e21bd-115">Elija **aplicación de Windows Forms .NET Framework** y, a continuación, elija **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e21bd-115">Choose **Windows Forms .NET Framework App** and then choose **Next**.</span></span>

    ![NewProject](./media/winforms-newproject.png)

1. <span data-ttu-id="e21bd-117">Escriba los valores para **el nombre** y la **Ubicación**del proyecto.</span><span class="sxs-lookup"><span data-stu-id="e21bd-117">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="e21bd-118">Seleccione **.NET Framework 4.6.2** o posterior.</span><span class="sxs-lookup"><span data-stu-id="e21bd-118">Select **.NET Framework 4.6.2** or later.</span></span>  

    ![startproject](./media/winforms-startproj.png)

1. <span data-ttu-id="e21bd-120">Elija **crear** para crear el proyecto.</span><span class="sxs-lookup"><span data-stu-id="e21bd-120">Choose **Create** to create your project.</span></span>

## <span data-ttu-id="e21bd-121">Paso 2: instalar el SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="e21bd-121">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="e21bd-122">A continuación, agregue el SDK de WebView2 al proyecto.</span><span class="sxs-lookup"><span data-stu-id="e21bd-122">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="e21bd-123">Para obtener la vista previa, instala el SDK de WebView2 con Nuget.</span><span class="sxs-lookup"><span data-stu-id="e21bd-123">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="e21bd-124">Abra el menú contextual en el proyecto \ (haga clic con el botón derecho \) y elija **administrar paquetes NuGet...**.</span><span class="sxs-lookup"><span data-stu-id="e21bd-124">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Administrar paquetes NuGet":::
       <span data-ttu-id="e21bd-126">Administrar paquetes NuGet</span><span class="sxs-lookup"><span data-stu-id="e21bd-126">Manage NuGet Packages</span></span> :::image-end:::

1. <span data-ttu-id="e21bd-127">Escriba `Microsoft.Web.WebView2` en la barra de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e21bd-127">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="e21bd-128">Seleccione **Microsoft. Web. WebView2** en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e21bd-128">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="e21bd-129">Asegúrese de que marca la opción **incluir**versión, seleccione un paquete de versión preliminar en **versión**y, a continuación, elija **instalar**.</span><span class="sxs-lookup"><span data-stu-id="e21bd-129">Ensure you check **Include prerelease**, select a prerelease package in **Version**, and then choose **Install**.</span></span>  

    ![Nuget](./media/installnuget.png)

<span data-ttu-id="e21bd-131">Ya está todo listo para empezar a desarrollar aplicaciones con la API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="e21bd-131">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="e21bd-132">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="e21bd-132">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="e21bd-133">El proyecto en ejecución muestra una ventana vacía.</span><span class="sxs-lookup"><span data-stu-id="e21bd-133">The running project displays an empty window.</span></span>  

![emptyApp](./media/winforms-emptyApp.png)

## <span data-ttu-id="e21bd-135">Paso 3: crear un único WebView</span><span class="sxs-lookup"><span data-stu-id="e21bd-135">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="e21bd-136">A continuación, agregue una vista de vista a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e21bd-136">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="e21bd-137">Abra el **Diseñador de Windows Forms**.</span><span class="sxs-lookup"><span data-stu-id="e21bd-137">Open the **Windows Forms Designer**.</span></span>  
1. <span data-ttu-id="e21bd-138">Busque **WebView2** en el **cuadro de herramientas**.</span><span class="sxs-lookup"><span data-stu-id="e21bd-138">Search for **WebView2** in the **Toolbox**.</span></span> <span data-ttu-id="e21bd-139">Arrastre y coloque el control **WebView2** en la aplicación Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e21bd-139">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Administrar paquetes NuGet":::
       <span data-ttu-id="e21bd-141">Cuadro de herramientas que muestra WebView2</span><span class="sxs-lookup"><span data-stu-id="e21bd-141">Toolbox displaying WebView2</span></span> :::image-end:::  

1. <span data-ttu-id="e21bd-142">Cambie la `Name` propiedad a `webView` .</span><span class="sxs-lookup"><span data-stu-id="e21bd-142">Change the `Name` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Administrar paquetes NuGet":::
       <span data-ttu-id="e21bd-144">Propiedades del control WebView2</span><span class="sxs-lookup"><span data-stu-id="e21bd-144">Properties of the WebView2 control</span></span> :::image-end:::

1. <span data-ttu-id="e21bd-145">La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="e21bd-145">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span> <span data-ttu-id="e21bd-146">Establezca la propiedad Source en</span><span class="sxs-lookup"><span data-stu-id="e21bd-146">Set the Source property to</span></span> <https://www.microsoft.com>
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Administrar paquetes NuGet":::
       <span data-ttu-id="e21bd-148">Propiedad Source del control WebView2</span><span class="sxs-lookup"><span data-stu-id="e21bd-148">The Source property of the WebView2 control</span></span> :::image-end:::

<span data-ttu-id="e21bd-149">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="e21bd-149">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="e21bd-150">Confirme que se muestra el control WebView2 [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="e21bd-150">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> <span data-ttu-id="e21bd-152">Si está trabajando en un monitor de alta definición de PPP, es posible que tenga que [configurar la aplicación de Windows Forms para una compatibilidad con alta definición de PPP](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span><span class="sxs-lookup"><span data-stu-id="e21bd-152">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span></span>

## <span data-ttu-id="e21bd-153">Paso 4: controlar los eventos de ajuste de tamaño de la ventana</span><span class="sxs-lookup"><span data-stu-id="e21bd-153">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="e21bd-154">Agregue algunos controles más a sus formularios Windows Forms desde el cuadro de herramientas y, a continuación, administre los eventos de tamaño de ventana correctamente.</span><span class="sxs-lookup"><span data-stu-id="e21bd-154">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1. <span data-ttu-id="e21bd-155">En el **Diseñador de Windows Forms** , abra el **cuadro de herramientas**</span><span class="sxs-lookup"><span data-stu-id="e21bd-155">In the **Windows Forms Designer** open the **Toolbox**</span></span>
1. <span data-ttu-id="e21bd-156">Arrastre y coloque un **cuadro de texto** en la aplicación de formularios Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e21bd-156">Drag and Drop a **TextBox** into the Windows Forms App.</span></span> <span data-ttu-id="e21bd-157">Asigne un nombre al **cuadro** `addressBar` de texto en la **pestaña propiedades**.</span><span class="sxs-lookup"><span data-stu-id="e21bd-157">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>
1. <span data-ttu-id="e21bd-158">Arrastre y coloque un **botón** en la aplicación Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e21bd-158">Drag and Drop a **Button** into the Windows Forms App.</span></span> <span data-ttu-id="e21bd-159">Cambie el texto del **botón** a `Go!` y asígnele el nombre **Button** `goButton` de la **pestaña propiedades**.</span><span class="sxs-lookup"><span data-stu-id="e21bd-159">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

    <span data-ttu-id="e21bd-160">La aplicación debe tener un aspecto similar al siguiente en el diseñador:</span><span class="sxs-lookup"><span data-stu-id="e21bd-160">The app should look like the following in the designer:</span></span>
    
    ![diseñador](./media/winforms-designer.png)

1. <span data-ttu-id="e21bd-162">En **Form1.CS** define `Form_Resize` para mantener los controles en su lugar cuando se cambie el tamaño de la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e21bd-162">In **Form1.cs** define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

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

<span data-ttu-id="e21bd-163">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="e21bd-163">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="e21bd-164">Confirme que la aplicación se muestra de forma similar a la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e21bd-164">Confirm that the app displays similar to the following screenshot.</span></span>

![aplicación](./media/winforms-app.png)

## <span data-ttu-id="e21bd-166">Paso 5: navegación</span><span class="sxs-lookup"><span data-stu-id="e21bd-166">Step 5 - Navigation</span></span>

<span data-ttu-id="e21bd-167">Agregue una barra de direcciones a la aplicación para permitir a los usuarios que cambien la dirección URL que muestra el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="e21bd-167">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="e21bd-168">En `Form1.cs` Agregar el `CoreWebView2` espacio de nombres, inserte el siguiente fragmento de código en la parte superior de `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="e21bd-168">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1. <span data-ttu-id="e21bd-169">En el **Diseñador de Windows Forms**, haga doble clic en el `Go!` botón para crear el `goButton_Click` método `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="e21bd-169">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in `Form1.cs`.</span></span> <span data-ttu-id="e21bd-170">Copie y pegue el siguiente fragmento de código dentro de la función.</span><span class="sxs-lookup"><span data-stu-id="e21bd-170">Copy and paste the following snippet inside the function.</span></span> <span data-ttu-id="e21bd-171">Ahora, la `goButton_Click` función navega por la vista WebView a la dirección URL que se escribe en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e21bd-171">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="e21bd-172">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="e21bd-172">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="e21bd-173">Escriba una nueva dirección URL en la barra de direcciones y haga clic en **ir**.</span><span class="sxs-lookup"><span data-stu-id="e21bd-173">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="e21bd-174">Por ejemplo, escriba `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="e21bd-174">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="e21bd-175">Confirme que el control WebView2 se desplaza hasta la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e21bd-175">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="e21bd-176">Asegúrese de que se escribe una dirección URL completa en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e21bd-176">Ensure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="e21bd-177">`ArgumentException`Se inicia una si la dirección URL no comienza con `http://` o</span><span class="sxs-lookup"><span data-stu-id="e21bd-177">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

![bing](./media/winforms-bing.png)

## <span data-ttu-id="e21bd-179">Paso 6: eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="e21bd-179">Step 6 - Navigation events</span></span>  

<span data-ttu-id="e21bd-180">La aplicación que hospeda los controles WebView2 escucha los siguientes eventos provocados por el control WebView2 durante la navegación a páginas Web.</span><span class="sxs-lookup"><span data-stu-id="e21bd-180">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="e21bd-181">Para obtener más información, vea [eventos de navegación](../concepts/navigation-events.md).</span><span class="sxs-lookup"><span data-stu-id="e21bd-181">For more information, see [Navigation Events](../concepts/navigation-events.md).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Administrar paquetes NuGet":::
   <span data-ttu-id="e21bd-183">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="e21bd-183">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="e21bd-184">Cuando se produce un error, se producen los eventos siguientes y puede que dependan de la navegación a una página de error.</span><span class="sxs-lookup"><span data-stu-id="e21bd-184">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="e21bd-185">Cuando hay una redirección de HTTP, hay varios `NavigationStarting` eventos.</span><span class="sxs-lookup"><span data-stu-id="e21bd-185">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="e21bd-186">Para mostrar cómo usar estos eventos, comienza registrando un controlador para `NavigationStarting` que cancele todas las solicitudes que no usen https.</span><span class="sxs-lookup"><span data-stu-id="e21bd-186">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="e21bd-187">En `Form1.cs` , modifique el constructor como se muestra a continuación y agregue la `EnsureHttps` función.</span><span class="sxs-lookup"><span data-stu-id="e21bd-187">In `Form1.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="e21bd-188">En el constructor, EnsureHttps se registra como el controlador de eventos en el `NavigationStarting` evento en el control de WebView2.</span><span class="sxs-lookup"><span data-stu-id="e21bd-188">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="e21bd-189">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="e21bd-189">Select `F5` to build and run your project.</span></span> <span data-ttu-id="e21bd-190">Confirme que, al navegar a un sitio HTTP, la WebView no sufre cambios.</span><span class="sxs-lookup"><span data-stu-id="e21bd-190">Confirm that when navigating to an HTTP site, the WebView remains unchanged.</span></span> <span data-ttu-id="e21bd-191">Sin embargo, la vista Web se desplazará a sitios HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e21bd-191">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="e21bd-192">Paso 7: scripting</span><span class="sxs-lookup"><span data-stu-id="e21bd-192">Step 7 - Scripting</span></span>  

<span data-ttu-id="e21bd-193">Puede usar aplicaciones host para inyectar código JavaScript en controles WebView2 en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e21bd-193">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="e21bd-194">El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a los fotogramas secundarios hasta que se quite el JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e21bd-194">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="e21bd-195">El código JavaScript insertado se ejecuta después de la creación del objeto global y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="e21bd-195">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="e21bd-196">Puede usar scripting para avisar al usuario cuando navegue a un sitio que no es HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e21bd-196">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="e21bd-197">Modifique la `EnsureHttps` función para que inserte el script en el contenido web con el método [ExecuteScriptAsync]() .</span><span class="sxs-lookup"><span data-stu-id="e21bd-197">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync]() method.</span></span>  

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

<span data-ttu-id="e21bd-198">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="e21bd-198">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="e21bd-199">Confirme que la aplicación muestra una alerta cuando se desplaza a un sitio que no usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e21bd-199">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

![https](./media/winforms-https.png)

## <span data-ttu-id="e21bd-201">Paso 8: comunicación entre el contenido del host y el Web</span><span class="sxs-lookup"><span data-stu-id="e21bd-201">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="e21bd-202">El host y el contenido web pueden comunicarse entre sí mediante las `postMessage` siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="e21bd-202">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="e21bd-203">El contenido Web de un control WebView2 puede publicar un mensaje en el host mediante `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="e21bd-203">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="e21bd-204">El anfitrión controla el mensaje con cualquier registro `WebMessageReceived` en el host.</span><span class="sxs-lookup"><span data-stu-id="e21bd-204">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="e21bd-205">Los anfitriones se exponen en el contenido web en un control WebView2 mediante `CoreWebView2.PostWebMessageAsString` o `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="e21bd-205">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="e21bd-206">Estos mensajes los detectan los controladores agregados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="e21bd-206">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="e21bd-207">Este mecanismo de comunicación permite que el contenido web transmita mensajes al host mediante capacidades nativas.</span><span class="sxs-lookup"><span data-stu-id="e21bd-207">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="e21bd-208">En el proyecto, cuando el control WebView2 navega a una dirección URL, muestra la dirección URL en la barra de direcciones y alerta al usuario de la dirección URL que se muestra en el control de WebView2.</span><span class="sxs-lookup"><span data-stu-id="e21bd-208">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="e21bd-209">En **Form1.CS**, actualice el constructor y cree una `InitializeAsync` función tal como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e21bd-209">In **Form1.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="e21bd-210">La `InitializeAsync` función espera [EnsureCoreWebView2Async]() porque la inicialización `CoreWebView2` es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e21bd-210">The `InitializeAsync` function awaits [EnsureCoreWebView2Async]() because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

1. <span data-ttu-id="e21bd-211">Después de inicializar **CoreWebView2** , registra un controlador de eventos para responder `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="e21bd-211">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="e21bd-212">En `Form1.cs` Update `InitializeAsync` y Add, `UpdateAddressBar` use el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e21bd-212">In `Form1.cs` update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1. <span data-ttu-id="e21bd-213">Para que la vista Web pueda enviar y responder al mensaje Web, después de que `CoreWebView2` se inicialice, el anfitrión inyecta una secuencia de comandos en el contenido web a:</span><span class="sxs-lookup"><span data-stu-id="e21bd-213">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1. <span data-ttu-id="e21bd-214">Envíe la dirección URL al host mediante `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="e21bd-214">Send the URL to the host using `postMessage`.</span></span>
    1. <span data-ttu-id="e21bd-215">Registre un controlador de eventos para imprimir un mensaje enviado desde el host.</span><span class="sxs-lookup"><span data-stu-id="e21bd-215">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="e21bd-216">En `Form1.cs` , actualice `InitializeAsync` tal como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e21bd-216">In `Form1.cs`, update `InitializeAsync` as shown in the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="e21bd-217">Seleccione `F5` para compilar y ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e21bd-217">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="e21bd-218">Confirme que la barra de direcciones muestra la dirección URL del sitio que se muestra en la vista Web.</span><span class="sxs-lookup"><span data-stu-id="e21bd-218">Confirm that the address bar displays the URL of the site displayed in the WebView.</span></span> <span data-ttu-id="e21bd-219">Además, cuando navegues correctamente a una nueva dirección URL, WebView avisará al usuario de la dirección URL que se muestra en la vista de vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="e21bd-219">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

![finalapp](./media/winforms-finalapp.png)

<span data-ttu-id="e21bd-221">¡ Enhorabuena! has creado tu primera WebView2 aplicación.</span><span class="sxs-lookup"><span data-stu-id="e21bd-221">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="e21bd-222">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="e21bd-222">Next steps</span></span> 

* <span data-ttu-id="e21bd-223">Desproteja el [repositorio de WebView2Samples](https://github.com/MicrosoftEdge/WebView2Samples) para obtener un ejemplo completo de las capacidades de WebView2's</span><span class="sxs-lookup"><span data-stu-id="e21bd-223">Checkout the [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) for a comprehensive example of WebView2's capabilities</span></span>
* <span data-ttu-id="e21bd-224">[Consulta la referencia](/dotnet/api/microsoft.web.webview2.winformswebview2) de la API para obtener información más detallada sobre nuestras API</span><span class="sxs-lookup"><span data-stu-id="e21bd-224">Checkout [API reference](/dotnet/api/microsoft.web.webview2.winformswebview2) for more detailed information about our APIs</span></span>
* <span data-ttu-id="e21bd-225">Desproteja una lista de [recursos de WebView2](../index.md#next-steps) para obtener más información sobre WebView2</span><span class="sxs-lookup"><span data-stu-id="e21bd-225">Checkout a list of [WebView2 Resources](../index.md#next-steps) to learn more about WebView2</span></span>


## <span data-ttu-id="e21bd-226">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e21bd-226">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

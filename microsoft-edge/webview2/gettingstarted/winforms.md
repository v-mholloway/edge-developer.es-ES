---
description: Guía de introducción a aplicaciones webView2 para WinForms
title: Introducción a webView2 para aplicaciones de WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, aplicaciones de winforms, winforms, edge, CoreWebView2, control de explorador, html perimetral, introducción, Introducción, .NET, formularios de windows
ms.openlocfilehash: 9d797e87ff8b5f11d957442c2cea08ae2f8c66a7
ms.sourcegitcommit: 2ddfd98d1e871be9c61380a8ca57da398d38bd54
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "11470868"
---
# <a name="getting-started-with-webview2-in-windows-forms"></a><span data-ttu-id="e46ab-104">Introducción a WebView2 en Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e46ab-104">Getting started with WebView2 in Windows Forms</span></span>

<span data-ttu-id="e46ab-105">En este artículo, empieza a crear tu primera aplicación WebView2 y obtén información sobre las características principales de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="e46ab-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="e46ab-106">Para obtener más información sobre las API individuales, vaya a [Referencia de api][DotnetApiMicrosoftWebWebview2Winforms].</span><span class="sxs-lookup"><span data-stu-id="e46ab-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Winforms].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="e46ab-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e46ab-107">Prerequisites</span></span>  

<span data-ttu-id="e46ab-108">Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="e46ab-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="e46ab-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] o cualquier canal no estable de [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado en el sistema operativo compatible \(actualmente Windows 10, Windows 8.1 y Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="e46ab-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e46ab-110">El equipo de WebView recomienda usar el canal Canary y la versión mínima necesaria es 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="e46ab-110">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="e46ab-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e46ab-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="e46ab-112">WebView2 actualmente no admite los diseñadores de .NET 5 y .NET Core.</span><span class="sxs-lookup"><span data-stu-id="e46ab-112">WebView2 currently does not support the .NET 5 and .NET Core designers.</span></span>  

## <a name="step-1---create-a-single-window-app"></a><span data-ttu-id="e46ab-113">Paso 1: Crear una aplicación de una sola ventana</span><span class="sxs-lookup"><span data-stu-id="e46ab-113">Step 1 - Create a single-window app</span></span>

<span data-ttu-id="e46ab-114">Comience con un proyecto de escritorio básico que contenga una sola ventana principal.</span><span class="sxs-lookup"><span data-stu-id="e46ab-114">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="e46ab-115">En Visual Studio, elija **Windows Forms .NET Framework App**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="e46ab-115">In Visual Studio, choose **Windows Forms .NET Framework App** > **Next**.</span></span>
    
    :::image type="complex" source="./media/winforms-newproject.png" alt-text="Nuevo proyecto" lightbox="./media/winforms-newproject.png":::
       <span data-ttu-id="e46ab-117">Nuevo proyecto</span><span class="sxs-lookup"><span data-stu-id="e46ab-117">New project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="e46ab-118">Escriba valores para **Nombre del proyecto y** **Ubicación**.</span><span class="sxs-lookup"><span data-stu-id="e46ab-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="e46ab-119">Elija **.NET Framework 4.6.2** o posterior.</span><span class="sxs-lookup"><span data-stu-id="e46ab-119">Choose **.NET Framework 4.6.2** or later.</span></span>  
    
    :::image type="complex" source="./media/winforms-startproj.png" alt-text="Iniciar proyecto" lightbox="./media/winforms-startproj.png":::
       <span data-ttu-id="e46ab-121">Iniciar proyecto</span><span class="sxs-lookup"><span data-stu-id="e46ab-121">Start project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="e46ab-122">Para crear el proyecto, elija **Crear**.</span><span class="sxs-lookup"><span data-stu-id="e46ab-122">To create your project, choose **Create**.</span></span>
    
## <a name="step-2---install-webview2-sdk"></a><span data-ttu-id="e46ab-123">Paso 2: Instalar WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="e46ab-123">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="e46ab-124">Use NuGet para agregar el SDK de WebView2 al proyecto.</span><span class="sxs-lookup"><span data-stu-id="e46ab-124">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="e46ab-125">Mantenga el mouse en el proyecto, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Administrar paquetes NuGet...**.</span><span class="sxs-lookup"><span data-stu-id="e46ab-125">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Administrar paquetes nuget":::
       <span data-ttu-id="e46ab-127">Administrar paquetes nuget</span><span class="sxs-lookup"><span data-stu-id="e46ab-127">Manage NuGet Packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="e46ab-128">En la barra de búsqueda, `Microsoft.Web.WebView2` escriba > **elija Microsoft.Web.WebView2**.</span><span class="sxs-lookup"><span data-stu-id="e46ab-128">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       <span data-ttu-id="e46ab-130">NuGet</span><span class="sxs-lookup"><span data-stu-id="e46ab-130">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="e46ab-131">Comience a desarrollar aplicaciones con la API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="e46ab-131">Start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="e46ab-132">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-132">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="e46ab-133">El proyecto en ejecución muestra una ventana vacía.</span><span class="sxs-lookup"><span data-stu-id="e46ab-133">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Aplicación vacía" lightbox="./media/winforms-emptyapp.png":::
       <span data-ttu-id="e46ab-135">Aplicación vacía</span><span class="sxs-lookup"><span data-stu-id="e46ab-135">Empty app</span></span>  
    :::image-end:::
    
## <a name="step-3---create-a-single-webview"></a><span data-ttu-id="e46ab-136">Paso 3: Crear un único WebView</span><span class="sxs-lookup"><span data-stu-id="e46ab-136">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="e46ab-137">Agrega un WebView a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e46ab-137">Add a WebView to your app.</span></span>  

1.  <span data-ttu-id="e46ab-138">Abra el **Diseñador de Windows Forms**.</span><span class="sxs-lookup"><span data-stu-id="e46ab-138">Open the **Windows Forms Designer**.</span></span>  
1.  <span data-ttu-id="e46ab-139">Busque **WebView2 en** el cuadro **de herramientas**.</span><span class="sxs-lookup"><span data-stu-id="e46ab-139">Search for **WebView2** in the **Toolbox**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e46ab-140">Si usa Visual Studio 2017, es posible que **WebView2** no se muestre de forma predeterminada en el cuadro **de herramientas**.</span><span class="sxs-lookup"><span data-stu-id="e46ab-140">If you are using Visual Studio 2017, by default **WebView2** may not display in the **Toolbox**.</span></span>  <span data-ttu-id="e46ab-141">Para habilitar el comportamiento, elija **Opciones**  >  **de**herramientas  >  **Generales** > \*\*\*\* la configuración Del cuadro de herramientas Rellenar automáticamente en `True` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-141">To enable the behavior, choose **Tools** > **Options** > **General** > set the **Automatically Populate Toolbox** setting to `True`.</span></span>  
    
    <span data-ttu-id="e46ab-142">Arrastre y coloque el control **WebView2** en la aplicación de Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e46ab-142">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Cuadro de herramientas que muestra WebView2":::
       <span data-ttu-id="e46ab-144">Cuadro de herramientas que muestra WebView2</span><span class="sxs-lookup"><span data-stu-id="e46ab-144">Toolbox displaying WebView2</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="e46ab-145">Establezca la `(Name)` propiedad en `webView` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-145">Set the `(Name)` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Propiedades del control WebView2":::
       <span data-ttu-id="e46ab-147">Propiedades del control WebView2</span><span class="sxs-lookup"><span data-stu-id="e46ab-147">Properties of the WebView2 control</span></span>
    :::image-end:::

1.  <span data-ttu-id="e46ab-148">La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="e46ab-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  <span data-ttu-id="e46ab-149">Establezca la `Source` propiedad en `https://www.microsoft.com` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-149">Set the `Source` property to `https://www.microsoft.com`.</span></span>  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="La propiedad Source del control WebView2":::
       <span data-ttu-id="e46ab-151">La **propiedad Source** del control WebView2</span><span class="sxs-lookup"><span data-stu-id="e46ab-151">The **Source** property of the WebView2 control</span></span>
    :::image-end:::  

<span data-ttu-id="e46ab-152">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-152">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="e46ab-153">Asegúrese de que el control WebView2 muestra [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="e46ab-153">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>

:::image type="complex" source="./media/winforms-hellowebview.png" alt-text="hello webview" lightbox="./media/winforms-hellowebview.png":::
   <span data-ttu-id="e46ab-155">hello webview</span><span class="sxs-lookup"><span data-stu-id="e46ab-155">hello webview</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e46ab-156">Si estás trabajando en un monitor de PPP alto, es posible que debas configurar la aplicación de Windows Forms para que sea [compatible con PPP alto.][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]</span><span class="sxs-lookup"><span data-stu-id="e46ab-156">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport].</span></span>  

## <a name="step-4---handle-window-resize-events"></a><span data-ttu-id="e46ab-157">Paso 4: Controlar eventos de cambio de tamaño de ventana</span><span class="sxs-lookup"><span data-stu-id="e46ab-157">Step 4 - Handle Window Resize Events</span></span>  

<span data-ttu-id="e46ab-158">Agrega algunos controles más a Windows Forms desde el cuadro de herramientas y, a continuación, controla los eventos de cambio de tamaño de la ventana correctamente.</span><span class="sxs-lookup"><span data-stu-id="e46ab-158">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>  

1.  <span data-ttu-id="e46ab-159">En el **Diseñador de Windows Forms,** abra el **cuadro de herramientas**.</span><span class="sxs-lookup"><span data-stu-id="e46ab-159">In the **Windows Forms Designer**, open the **Toolbox**.</span></span>  
1.  <span data-ttu-id="e46ab-160">Arrastre y coloque un **textbox** en la aplicación de Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e46ab-160">Drag and Drop a **TextBox** into the Windows Forms App.</span></span>  <span data-ttu-id="e46ab-161">Asigne el **nombre TextBox** `addressBar` a la pestaña **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="e46ab-161">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>  
1.  <span data-ttu-id="e46ab-162">Arrastre y coloque un **botón** en la aplicación de Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e46ab-162">Drag and Drop a **Button** into the Windows Forms App.</span></span>  <span data-ttu-id="e46ab-163">Cambie el texto del **botón a y** asigne un nombre al botón `Go!` **en** la `goButton` pestaña **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="e46ab-163">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>  
    
    <span data-ttu-id="e46ab-164">La aplicación debe tener el aspecto de la siguiente imagen en el diseñador.</span><span class="sxs-lookup"><span data-stu-id="e46ab-164">The app should look like the following image in the designer.</span></span>  
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="Diseñador de WinForms" lightbox="./media/winforms-designer.png":::
       <span data-ttu-id="e46ab-166">Diseñador de WinForms</span><span class="sxs-lookup"><span data-stu-id="e46ab-166">WinForms designer</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="e46ab-167">En el archivo, defina para mantener los controles en su lugar cuando se cambie el tamaño de `Form1.cs` la ventana de la `Form_Resize` aplicación.</span><span class="sxs-lookup"><span data-stu-id="e46ab-167">In the `Form1.cs` file, define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

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

<span data-ttu-id="e46ab-168">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-168">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="e46ab-169">Asegúrate de que la aplicación se muestre de forma similar a la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e46ab-169">Ensure the app displays similar to the following screenshot.</span></span>

:::image type="complex" source="./media/winforms-app.png" alt-text="aplicación" lightbox="./media/winforms-app.png":::
   <span data-ttu-id="e46ab-171">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e46ab-171">App</span></span>  
:::image-end:::

## <a name="step-5---navigation"></a><span data-ttu-id="e46ab-172">Paso 5: navegación</span><span class="sxs-lookup"><span data-stu-id="e46ab-172">Step 5 - Navigation</span></span>

<span data-ttu-id="e46ab-173">Agregue la capacidad de permitir a los usuarios cambiar la dirección URL que muestra el control WebView2 agregando una barra de direcciones a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e46ab-173">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>  

1.  <span data-ttu-id="e46ab-174">Seleccione `F5` para compilar y ejecutar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="e46ab-174">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="e46ab-175">Confirme que la aplicación se muestra de forma similar a la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e46ab-175">Confirm that the app displays similar to the following screenshot.</span></span>  
    
    :::image type="complex" source="./media/winforms-app.png" alt-text="WinForms App" lightbox="./media/winforms-app.png":::
       <span data-ttu-id="e46ab-177">WinForms App</span><span class="sxs-lookup"><span data-stu-id="e46ab-177">WinForms App</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e46ab-178">En el `Form1.cs` archivo, para agregar el espacio `CoreWebView2` de nombres, inserte el siguiente fragmento de código en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="e46ab-178">In the `Form1.cs`file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  

1.  <span data-ttu-id="e46ab-179">En `Form1.cs` agregar el espacio de nombres `CoreWebView2` insertando el siguiente fragmento de código en la parte superior de `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-179">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1.  <span data-ttu-id="e46ab-180">En el **Diseñador de Windows Forms,** haga doble clic en el `Go!` botón para crear el método en el `goButton_Click` `Form1.cs` archivo.</span><span class="sxs-lookup"><span data-stu-id="e46ab-180">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in the `Form1.cs` file.</span></span>  <span data-ttu-id="e46ab-181">Copie y pegue el siguiente fragmento de código dentro de la función.</span><span class="sxs-lookup"><span data-stu-id="e46ab-181">Copy and paste the following snippet inside the function.</span></span>  <span data-ttu-id="e46ab-182">Ahora, la `goButton_Click` función navega por WebView hasta la dirección URL especificada en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e46ab-182">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="e46ab-183">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-183">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="e46ab-184">Escriba una nueva dirección URL en la barra de direcciones y seleccione **Ir**.</span><span class="sxs-lookup"><span data-stu-id="e46ab-184">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="e46ab-185">Por ejemplo, escriba `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-185">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="e46ab-186">Asegúrese de que el control WebView2 navega a la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e46ab-186">Ensure the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="e46ab-187">Asegúrese de que se ha escrito una dirección URL completa en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e46ab-187">Ensure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="e46ab-188">Se `ArgumentException` produce un error si la dirección URL no comienza con `http://` o</span><span class="sxs-lookup"><span data-stu-id="e46ab-188">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   <span data-ttu-id="e46ab-190">bing.com</span><span class="sxs-lookup"><span data-stu-id="e46ab-190">bing.com</span></span>  
:::image-end:::

## <a name="step-6---navigation-events"></a><span data-ttu-id="e46ab-191">Paso 6: eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="e46ab-191">Step 6 - Navigation events</span></span>  

<span data-ttu-id="e46ab-192">Durante la navegación por la página web, el control WebView2 genera eventos.</span><span class="sxs-lookup"><span data-stu-id="e46ab-192">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="e46ab-193">La aplicación que hospeda los controles WebView2 escucha los siguientes eventos.</span><span class="sxs-lookup"><span data-stu-id="e46ab-193">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="e46ab-194">Para obtener más información, vaya a [Eventos de navegación][Webview2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="e46ab-194">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación":::
   <span data-ttu-id="e46ab-196">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="e46ab-196">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="e46ab-197">Cuando se produce un error, se producen los siguientes eventos y pueden depender de la navegación a una página web de error.</span><span class="sxs-lookup"><span data-stu-id="e46ab-197">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> <span data-ttu-id="e46ab-198">Si se produce un redireccionamiento HTTP, hay varios `NavigationStarting` eventos en una fila.</span><span class="sxs-lookup"><span data-stu-id="e46ab-198">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="e46ab-199">Para demostrar cómo usar los eventos, empiece registrando un controlador para que cancele las solicitudes que no `NavigationStarting` usen HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e46ab-199">To demonstrate how to use the events, start by registering a handler for `NavigationStarting` that cancels any requests not using HTTPS.</span></span>  

<span data-ttu-id="e46ab-200">En el `Form1.cs` archivo, actualice el constructor para que coincida con el siguiente fragmento de código y agregue la `EnsureHttps` función.</span><span class="sxs-lookup"><span data-stu-id="e46ab-200">In the `Form1.cs` file, update the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="e46ab-201">En el constructor, `EnsureHttps` se registra como el controlador de eventos en el evento en el control `NavigationStarting` WebView2.</span><span class="sxs-lookup"><span data-stu-id="e46ab-201">In the constructor, `EnsureHttps` is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="e46ab-202">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-202">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="e46ab-203">Asegúrese de que al navegar a un sitio HTTP, webView permanece sin cambios.</span><span class="sxs-lookup"><span data-stu-id="e46ab-203">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="e46ab-204">Sin embargo, WebView navegará a los sitios HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e46ab-204">However, the WebView will navigate to HTTPS sites.</span></span>

## <a name="step-7---scripting"></a><span data-ttu-id="e46ab-205">Paso 7: scripting</span><span class="sxs-lookup"><span data-stu-id="e46ab-205">Step 7 - Scripting</span></span>  

<span data-ttu-id="e46ab-206">Puede usar aplicaciones host para insertar código JavaScript en controles WebView2 en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e46ab-206">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="e46ab-207">Puede realizar la tarea WebView para ejecutar JavaScript arbitrario o agregar scripts de inicialización.</span><span class="sxs-lookup"><span data-stu-id="e46ab-207">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="e46ab-208">JavaScript inyectado se aplica a todos los nuevos documentos de nivel superior y a los fotogramas secundarios hasta que se quita JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e46ab-208">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="e46ab-209">JavaScript inyectado se ejecuta con un tiempo específico.</span><span class="sxs-lookup"><span data-stu-id="e46ab-209">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="e46ab-210">Ejecutarlo después de la creación del objeto global.</span><span class="sxs-lookup"><span data-stu-id="e46ab-210">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="e46ab-211">Ejecutarlo antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="e46ab-211">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="e46ab-212">Por ejemplo, agregue scripts que envíen una alerta cuando un usuario navegue a sitios que no son HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e46ab-212">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="e46ab-213">Modifique la `EnsureHttps` función para insertar un script en el contenido web que usa el método [ExecuteScriptAsync.][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]</span><span class="sxs-lookup"><span data-stu-id="e46ab-213">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync] method.</span></span>  

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

<span data-ttu-id="e46ab-214">Para compilar y ejecutar el proyecto, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-214">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="e46ab-215">Asegúrate de que la aplicación muestra una alerta cuando navegas a un sitio web que no usa HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e46ab-215">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   <span data-ttu-id="e46ab-217">https</span><span class="sxs-lookup"><span data-stu-id="e46ab-217">https</span></span>  
:::image-end:::

## <a name="step-8---communication-between-host-and-web-content"></a><span data-ttu-id="e46ab-218">Paso 8: comunicación entre el contenido de host y web</span><span class="sxs-lookup"><span data-stu-id="e46ab-218">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="e46ab-219">El host y el contenido web pueden `postMessage` usarse para comunicarse entre sí de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="e46ab-219">The host and web content may use `postMessage` to communicate with each other as follows:</span></span>  

*   <span data-ttu-id="e46ab-220">El contenido web de un control WebView2 puede `window.chrome.webview.postMessage` usarse para publicar un mensaje en el host.</span><span class="sxs-lookup"><span data-stu-id="e46ab-220">Web content in a WebView2 control may use `window.chrome.webview.postMessage` to post a message to the host.</span></span>  <span data-ttu-id="e46ab-221">El host controla el mensaje con cualquier registrado `WebMessageReceived` en el host.</span><span class="sxs-lookup"><span data-stu-id="e46ab-221">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="e46ab-222">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-222">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="e46ab-223">Estos mensajes son capturados por controladores agregados a `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-223">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="e46ab-224">El mecanismo de comunicación pasa mensajes del contenido web al host mediante funcionalidades nativas.</span><span class="sxs-lookup"><span data-stu-id="e46ab-224">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="e46ab-225">En el proyecto, cuando el control WebView2 navega a una dirección URL, muestra la dirección URL en la barra de direcciones y alerta al usuario de la dirección URL mostrada en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="e46ab-225">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="e46ab-226">En el `Form1.cs` archivo, actualice el constructor y cree una `InitializeAsync` función que coincida con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e46ab-226">In the `Form1.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="e46ab-227">La `InitializeAsync` función espera [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] porque la inicialización de `CoreWebView2` es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e46ab-227">The `InitializeAsync` function awaits [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

1.  <span data-ttu-id="e46ab-228">Después `CoreWebView2` de inicializarse, registre un controlador de eventos para responder a `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-228">After `CoreWebView2` is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="e46ab-229">En el `Form1.cs` archivo, actualice `InitializeAsync` y agregue con el siguiente fragmento de `UpdateAddressBar` código.</span><span class="sxs-lookup"><span data-stu-id="e46ab-229">In the `Form1.cs` file, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1.  <span data-ttu-id="e46ab-230">Para que WebView envíe y responda al mensaje web, después de inicializarse, el host inserta un script en el `CoreWebView2` contenido web para:</span><span class="sxs-lookup"><span data-stu-id="e46ab-230">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1.  <span data-ttu-id="e46ab-231">Envíe la dirección URL al host mediante `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-231">Send the URL to the host using `postMessage`.</span></span>
    1.  <span data-ttu-id="e46ab-232">Registrar un controlador de eventos para imprimir un mensaje enviado desde el host.</span><span class="sxs-lookup"><span data-stu-id="e46ab-232">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="e46ab-233">En el `Form1.cs` archivo, actualice `InitializeAsync` para que coincida con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e46ab-233">In the `Form1.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="e46ab-234">Para compilar y ejecutar la aplicación, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e46ab-234">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="e46ab-235">Ahora, la barra de direcciones muestra el URI en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="e46ab-235">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="e46ab-236">Además, cuando navega correctamente a una nueva dirección URL, WebView alerta al usuario de la dirección URL que se muestra en WebView.</span><span class="sxs-lookup"><span data-stu-id="e46ab-236">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

:::image type="complex" source="./media/winforms-finalapp.png" alt-text="Aplicación final" lightbox="./media/winforms-finalapp.png":::
   <span data-ttu-id="e46ab-238">Aplicación final</span><span class="sxs-lookup"><span data-stu-id="e46ab-238">Final app</span></span>  
:::image-end:::

<span data-ttu-id="e46ab-239">Enhorabuena, has creado tu primera aplicación WebView2.</span><span class="sxs-lookup"><span data-stu-id="e46ab-239">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="e46ab-240">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="e46ab-240">Next steps</span></span>  

<span data-ttu-id="e46ab-241">Para seguir aprendiendo más sobre WebView2, vaya a los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="e46ab-241">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <a name="see-also"></a><span data-ttu-id="e46ab-242">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e46ab-242">See also</span></span>  

*   <span data-ttu-id="e46ab-243">Para obtener un ejemplo completo de las capacidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="e46ab-243">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="e46ab-244">Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="e46ab-244">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
*   <span data-ttu-id="e46ab-245">Para obtener información detallada acerca de la API de WebView2, vaya a [Referencia de api][DotnetApiMicrosoftWebWebview2WinformsWebview2].</span><span class="sxs-lookup"><span data-stu-id="e46ab-245">For detailed information about the WebView2 API, navigate to [API reference][DotnetApiMicrosoftWebWebview2WinformsWebview2].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="e46ab-246">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="e46ab-246">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegación | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Espacio de nombres Microsoft.Web.WebView2.WinForms | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Clase WebView2 | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "Método WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) | Microsoft Docs"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Configuración de la aplicación de Windows Forms para la compatibilidad con PPP alto: compatibilidad con PPP alto en Windows Forms | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Desarrollador de Microsoft Edge"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

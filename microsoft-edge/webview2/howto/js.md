---
description: Más información sobre cómo usar JavaScript en escenarios complejos en aplicaciones de WebView2
title: Usar JavaScript en aplicaciones de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/15/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 0fd4e33b7cfc16dcd19a850147b6efbca8922a8e
ms.sourcegitcommit: 442de63da52d00c6dc27fa08ccdb736534127566
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "11120076"
---
# <span data-ttu-id="2c986-104">Usar JavaScript en vista previa para escenarios extendidos</span><span class="sxs-lookup"><span data-stu-id="2c986-104">Use JavaScript in WebView for extended scenarios</span></span>  

<span data-ttu-id="2c986-105">El uso de JavaScript en WebView2 permite personalizar aplicaciones nativas para satisfacer sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="2c986-105">Using JavaScript in WebView2 controls allows you to customize native apps to meet your requirements.</span></span>  <span data-ttu-id="2c986-106">En este artículo se explica cómo usar JavaScript en WebView2 y se revisa cómo desarrollar con las características y funcionalidades avanzadas de WebView2.</span><span class="sxs-lookup"><span data-stu-id="2c986-106">This article explores how to use JavaScript in WebView2, and reviews how to develop using advanced WebView2 features and functionality.</span></span>  

## <span data-ttu-id="2c986-107">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="2c986-107">Before you begin</span></span>  

<span data-ttu-id="2c986-108">En este artículo se da por supuesto que ya tiene un proyecto en curso.</span><span class="sxs-lookup"><span data-stu-id="2c986-108">This article assumes that you already have a working project.</span></span>  <span data-ttu-id="2c986-109">Si no tiene un proyecto y quiere seguirlo, vaya a la [Guía de introducción de WebView2][Webview2GettingstartedWpf].</span><span class="sxs-lookup"><span data-stu-id="2c986-109">If you do not have a project and want to follow along, navigate to the [WebView2 Getting Started Guide][Webview2GettingstartedWpf].</span></span>  

## <span data-ttu-id="2c986-110">Funciones de WebView2 básicas</span><span class="sxs-lookup"><span data-stu-id="2c986-110">Basic WebView2 Functions</span></span>  

<span data-ttu-id="2c986-111">Use las siguientes funciones para empezar a incrustar JavaScript en la aplicación WebView.</span><span class="sxs-lookup"><span data-stu-id="2c986-111">Use the following functions to begin embedding JavaScript in your WebView app.</span></span>  

| <span data-ttu-id="2c986-112">API</span><span class="sxs-lookup"><span data-stu-id="2c986-112">API</span></span>  | <span data-ttu-id="2c986-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c986-113">Description</span></span>  |
|:--- |:--- |  
| [<span data-ttu-id="2c986-114">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="2c986-114">ExecuteScriptAsync</span></span>][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | <span data-ttu-id="2c986-115">Ejecutar JavaScript en un control WebView.</span><span class="sxs-lookup"><span data-stu-id="2c986-115">Run JavaScript in a WebView control.</span></span> <span data-ttu-id="2c986-116">Para obtener más información, vaya al tutorial Introducción.</span><span class="sxs-lookup"><span data-stu-id="2c986-116">For more information, navigate to the Getting Started tutorial.</span></span> |
| [<span data-ttu-id="2c986-117">OnDocumentCreatedAsync</span><span class="sxs-lookup"><span data-stu-id="2c986-117">OnDocumentCreatedAsync</span></span>][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | <span data-ttu-id="2c986-118">Se ejecuta cuando se crea el modelo de objetos de documento \ (DOM \).</span><span class="sxs-lookup"><span data-stu-id="2c986-118">Runs when the Document Object Model \(DOM\) is created.</span></span> |
      
## <span data-ttu-id="2c986-119">Escenario: ejecutar un archivo de script dedicado</span><span class="sxs-lookup"><span data-stu-id="2c986-119">Scenario:  Running a dedicated script file</span></span>  

<span data-ttu-id="2c986-120">En esta sección, accede a un archivo de JavaScript dedicado desde el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="2c986-120">In this section, access a dedicated JavaScript file from your WebView2 control.</span></span>  

> [!NOTE]
> <span data-ttu-id="2c986-121">Aunque escribir JavaScript en línea puede ser eficaz para los comandos rápidos de JavaScript, pierde los temas de color y el formato de las líneas de JavaScript que dificulta escribir grandes secciones de código en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2c986-121">Although writing JavaScript inline may be efficient for quick JavaScript commands, you lose JavaScript color themes and line formatting that makes it difficult to write large sections of code in Visual Studio.</span></span>  

<span data-ttu-id="2c986-122">Para resolver el problema, cree un archivo JavaScript independiente con el código y, a continuación, pase una referencia a ese archivo usando los `ExecuteScriptAsync` parámetros.</span><span class="sxs-lookup"><span data-stu-id="2c986-122">To solve the problem, create a separate JavaScript file with your code, and then pass a reference to that file using the `ExecuteScriptAsync` parameters.</span></span>  

1.  <span data-ttu-id="2c986-123">Cree un `.js` archivo en el proyecto y agregue el código JavaScript que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="2c986-123">Create a `.js` file in your project, and add the JavaScript code that you want to run.</span></span>  <span data-ttu-id="2c986-124">Por ejemplo, cree un archivo denominado `script.js` .</span><span class="sxs-lookup"><span data-stu-id="2c986-124">For example, create a file called `script.js`.</span></span>  
1.  <span data-ttu-id="2c986-125">Convierte el archivo JavaScript en una cadena que se pasa a `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="2c986-125">Convert the JavaScript file to a string that is passed to `ExecuteScriptAsync`.</span></span>  
    1.  <span data-ttu-id="2c986-126">Para convertir el archivo de JavaScript en una cadena, copie el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="2c986-126">To convert your JavaScript file into a string, copy the following code snippet.</span></span>  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  <span data-ttu-id="2c986-127">Pega el código en `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="2c986-127">Paste the code into `MainWindow.xaml.cs`.</span></span>  
1.  <span data-ttu-id="2c986-128">Pase la variable de texto con `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="2c986-128">Pass your text variable using `ExecuteScriptAsync`.</span></span>  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## <span data-ttu-id="2c986-129">Escenario: quitar la funcionalidad de arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="2c986-129">Scenario:  Remove drag-and-drop functionality</span></span>  

<span data-ttu-id="2c986-130">En esta sección, use JavaScript para quitar la funcionalidad de arrastrar y colocar de su control WebView2.</span><span class="sxs-lookup"><span data-stu-id="2c986-130">In this section, use JavaScript to remove the drag-and-drop functionality from your WebView2 control.</span></span>  

<span data-ttu-id="2c986-131">Para empezar, explore la funcionalidad actual de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="2c986-131">To begin, explore the current drag-and-drop functionality.</span></span>  

1.  <span data-ttu-id="2c986-132">Cree un `.txt` archivo para arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="2c986-132">Create a `.txt` file in order to drag-and-drop.</span></span>  <span data-ttu-id="2c986-133">Por ejemplo, cree un archivo con el nombre `contoso.txt` y agréguele texto.</span><span class="sxs-lookup"><span data-stu-id="2c986-133">For example, create a file named `contoso.txt` and add text to it.</span></span>  
1.  <span data-ttu-id="2c986-134">Ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="2c986-134">Run your project.</span></span>  
1.  <span data-ttu-id="2c986-135">Arrastre el archivo y colóquelo `contoso.txt` en el control WebView.</span><span class="sxs-lookup"><span data-stu-id="2c986-135">Drag-and-drop the `contoso.txt` file onto the WebView control.</span></span>  <span data-ttu-id="2c986-136">Se abrirá una nueva ventana, que es el resultado del código de su proyecto de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2c986-136">A new window opens, which is the result of the code in your sample project.</span></span>  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Resultado de arrastrar y soltar contoso.txt" lightbox="./media/dragtext.png":::
       <span data-ttu-id="2c986-138">Resultado de arrastrar y soltar contoso.txt</span><span class="sxs-lookup"><span data-stu-id="2c986-138">Result of dragging and dropping contoso.txt</span></span>  
    :::image-end:::  

<span data-ttu-id="2c986-139">Ahora, agregue código para quitar la funcionalidad de arrastrar y colocar del control WebView2.</span><span class="sxs-lookup"><span data-stu-id="2c986-139">Now, add code to remove the drag-and-drop functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="2c986-140">Copie y pegue el siguiente fragmento de código en `InitializeAsync()` en `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="2c986-140">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  <span data-ttu-id="2c986-141">Ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="2c986-141">Run your project.</span></span>  
1.  <span data-ttu-id="2c986-142">Intente arrastrar y colocar `contoso.txt` .</span><span class="sxs-lookup"><span data-stu-id="2c986-142">Try to drag-and-drop `contoso.txt`.</span></span>  <span data-ttu-id="2c986-143">Confirme que no puede arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="2c986-143">Confirm that you are not able to drag-and-drop.</span></span>  

## <span data-ttu-id="2c986-144">Escenario: quitar el menú contextual</span><span class="sxs-lookup"><span data-stu-id="2c986-144">Scenario:  Removing the Context Menu</span></span>  

<span data-ttu-id="2c986-145">En esta sección, quite el menú contextual predeterminado del control WebView2.</span><span class="sxs-lookup"><span data-stu-id="2c986-145">In this section, remove the default context menu from your WebView2 control.</span></span>  

<span data-ttu-id="2c986-146">Para empezar, explore la funcionalidad actual del menú contextual.</span><span class="sxs-lookup"><span data-stu-id="2c986-146">To begin, explore the current contextual menu functionality.</span></span>  

1.  <span data-ttu-id="2c986-147">Ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="2c986-147">Run your project.</span></span>  
1.  <span data-ttu-id="2c986-148">Mantenga el mouse en cualquier lugar del control WebView2 y abra el menú contextual \ (haga clic con el botón derecho \).</span><span class="sxs-lookup"><span data-stu-id="2c986-148">Hover anywhere on the WebView2 control and open the context menu \(right-click\).</span></span>  <span data-ttu-id="2c986-149">El menú contextual muestra las opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="2c986-149">The context menu displays the default choices.</span></span>  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Resultado de arrastrar y soltar contoso.txt" lightbox="./media/contextmenu.png":::
       <span data-ttu-id="2c986-151">Menú contextual que muestra las opciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="2c986-151">The context menu showing the default choices</span></span>  
    :::image-end:::  
    
<span data-ttu-id="2c986-152">Ahora agregue código para quitar la funcionalidad de menú contextual del control WebView2.</span><span class="sxs-lookup"><span data-stu-id="2c986-152">Now add code to remove the contextual menu functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="2c986-153">Copie y pegue el siguiente fragmento de código en `InitializeAsync()` en `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="2c986-153">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  <span data-ttu-id="2c986-154">Vuelva a ejecutar el código.</span><span class="sxs-lookup"><span data-stu-id="2c986-154">Run the code again.</span></span>  <span data-ttu-id="2c986-155">Confirme que no puede abrir un menú contextual \ (haga clic con el botón derecho \).</span><span class="sxs-lookup"><span data-stu-id="2c986-155">Confirm that you're not able to open a context menu \(right-click\).</span></span>  
   
## <span data-ttu-id="2c986-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2c986-156">See also</span></span>  

*   <span data-ttu-id="2c986-157">Para obtener más información sobre cómo comenzar a usar WebView2, vaya a [WebView2 guías de introducción][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="2c986-157">For more information on getting started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="2c986-158">Para obtener un ejemplo completo de las capacidades de WebView2, navegue hasta el repositorio de [WebView2Samples][GithubMicrosoftedgeWebview2samples] en github.</span><span class="sxs-lookup"><span data-stu-id="2c986-158">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>  
*   <span data-ttu-id="2c986-159">Para obtener información detallada sobre las API de WebView2, vaya a referencia de la [API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="2c986-159">For detailed information on WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>  
*   <span data-ttu-id="2c986-160">Para obtener más información sobre WebView2, vaya a [recursos WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="2c986-160">For more information on WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>  

## <span data-ttu-id="2c986-161">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2c986-161">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  


[Webview2ApiReference]: ../webview2-api-reference.md "Referencia de la API de Microsoft Edge WebView2 | Microsoft docs"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Introducción a WebView2 en WPF (vista previa) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated-0.9.579-interface ICoreWebView2 | Microsoft docs"  
[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync " MétodoWebView2.ExecuteScriptAsync (String) (Microsoft. Web. WebView2. WPF) | Microsoft docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

---
description: Obtenga información sobre cómo usar JavaScript en escenarios complejos en aplicaciones webView2
title: Usar JavaScript en aplicaciones webView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral
ms.openlocfilehash: da04d1e24b95dfa7ea477bbd228fd46b64727ec3
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536740"
---
# <a name="use-javascript-in-webview-for-extended-scenarios"></a><span data-ttu-id="32288-104">Usar JavaScript en WebView para escenarios extendidos</span><span class="sxs-lookup"><span data-stu-id="32288-104">Use JavaScript in WebView for extended scenarios</span></span>  

<span data-ttu-id="32288-105">El uso de JavaScript en controles WebView2 te permite personalizar aplicaciones nativas para satisfacer tus requisitos.</span><span class="sxs-lookup"><span data-stu-id="32288-105">Using JavaScript in WebView2 controls allows you to customize native apps to meet your requirements.</span></span>  <span data-ttu-id="32288-106">En este artículo se explora cómo usar JavaScript en WebView2 y se analiza cómo desarrollar mediante funciones y características avanzadas de WebView2.</span><span class="sxs-lookup"><span data-stu-id="32288-106">This article explores how to use JavaScript in WebView2, and reviews how to develop using advanced WebView2 features and functionality.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="32288-107">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="32288-107">Before you begin</span></span>  

<span data-ttu-id="32288-108">En este artículo se supone que ya tiene un proyecto en funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="32288-108">This article assumes that you already have a working project.</span></span>  <span data-ttu-id="32288-109">Si no tiene un proyecto y desea seguirlo, vaya a la Guía de introducción a [WebView2][Webview2GettingstartedWpf].</span><span class="sxs-lookup"><span data-stu-id="32288-109">If you do not have a project and want to follow along, navigate to the [WebView2 Getting Started Guide][Webview2GettingstartedWpf].</span></span>  

## <a name="basic-webview2-functions"></a><span data-ttu-id="32288-110">Funciones básicas de WebView2</span><span class="sxs-lookup"><span data-stu-id="32288-110">Basic WebView2 Functions</span></span>  

<span data-ttu-id="32288-111">Usa las siguientes funciones para empezar a insertar JavaScript en la aplicación WebView.</span><span class="sxs-lookup"><span data-stu-id="32288-111">Use the following functions to begin embedding JavaScript in your WebView app.</span></span>  

| <span data-ttu-id="32288-112">API</span><span class="sxs-lookup"><span data-stu-id="32288-112">API</span></span>  | <span data-ttu-id="32288-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="32288-113">Description</span></span>  |
|:--- |:--- |  
| [<span data-ttu-id="32288-114">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="32288-114">ExecuteScriptAsync</span></span>][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | <span data-ttu-id="32288-115">Ejecute JavaScript en un control WebView.</span><span class="sxs-lookup"><span data-stu-id="32288-115">Run JavaScript in a WebView control.</span></span> <span data-ttu-id="32288-116">Para obtener más información, vaya al tutorial Introducción.</span><span class="sxs-lookup"><span data-stu-id="32288-116">For more information, navigate to the Getting Started tutorial.</span></span> |
| [<span data-ttu-id="32288-117">OnDocumentCreatedAsync</span><span class="sxs-lookup"><span data-stu-id="32288-117">OnDocumentCreatedAsync</span></span>][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | <span data-ttu-id="32288-118">Se ejecuta cuando se crea el modelo de objetos de documento \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="32288-118">Runs when the Document Object Model \(DOM\) is created.</span></span> |
      
## <a name="scenario--running-a-dedicated-script-file"></a><span data-ttu-id="32288-119">Escenario: ejecución de un archivo de script dedicado</span><span class="sxs-lookup"><span data-stu-id="32288-119">Scenario:  Running a dedicated script file</span></span>  

<span data-ttu-id="32288-120">En esta sección, acceda a un archivo JavaScript dedicado desde el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="32288-120">In this section, access a dedicated JavaScript file from your WebView2 control.</span></span>  

> [!NOTE]
> <span data-ttu-id="32288-121">Aunque escribir JavaScript en línea puede ser eficaz para comandos rápidos de JavaScript, se pierden los temas de color de JavaScript y el formato de línea que dificulta la escritura de grandes secciones de código en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="32288-121">Although writing JavaScript inline may be efficient for quick JavaScript commands, you lose JavaScript color themes and line formatting that makes it difficult to write large sections of code in Visual Studio.</span></span>  

<span data-ttu-id="32288-122">Para solucionar el problema, cree un archivo JavaScript independiente con el código y, a continuación, pase una referencia a ese archivo mediante los `ExecuteScriptAsync` parámetros.</span><span class="sxs-lookup"><span data-stu-id="32288-122">To solve the problem, create a separate JavaScript file with your code, and then pass a reference to that file using the `ExecuteScriptAsync` parameters.</span></span>  

1.  <span data-ttu-id="32288-123">Cree un archivo en el proyecto y agregue el código `.js` JavaScript que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="32288-123">Create a `.js` file in your project, and add the JavaScript code that you want to run.</span></span>  <span data-ttu-id="32288-124">Por ejemplo, cree un archivo denominado `script.js` .</span><span class="sxs-lookup"><span data-stu-id="32288-124">For example, create a file called `script.js`.</span></span>  
1.  <span data-ttu-id="32288-125">Convertir el archivo JavaScript en una cadena que se pasa a `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="32288-125">Convert the JavaScript file to a string that is passed to `ExecuteScriptAsync`.</span></span>  
    1.  <span data-ttu-id="32288-126">Para convertir el archivo JavaScript en una cadena, copie el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="32288-126">To convert your JavaScript file into a string, copy the following code snippet.</span></span>  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  <span data-ttu-id="32288-127">Pegue el código en `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="32288-127">Paste the code into `MainWindow.xaml.cs`.</span></span>  
1.  <span data-ttu-id="32288-128">Pase la variable de texto mediante `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="32288-128">Pass your text variable using `ExecuteScriptAsync`.</span></span>  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## <a name="scenario--remove-drag-and-drop-functionality"></a><span data-ttu-id="32288-129">Escenario: quitar la funcionalidad de arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="32288-129">Scenario:  Remove drag-and-drop functionality</span></span>  

<span data-ttu-id="32288-130">En esta sección, use JavaScript para quitar la funcionalidad de arrastrar y colocar del control WebView2.</span><span class="sxs-lookup"><span data-stu-id="32288-130">In this section, use JavaScript to remove the drag-and-drop functionality from your WebView2 control.</span></span>  

<span data-ttu-id="32288-131">Para empezar, explore la funcionalidad actual de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="32288-131">To begin, explore the current drag-and-drop functionality.</span></span>  

1.  <span data-ttu-id="32288-132">Cree un `.txt` archivo para arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="32288-132">Create a `.txt` file in order to drag-and-drop.</span></span>  <span data-ttu-id="32288-133">Por ejemplo, cree un archivo denominado `contoso.txt` y agréle texto.</span><span class="sxs-lookup"><span data-stu-id="32288-133">For example, create a file named `contoso.txt` and add text to it.</span></span>  
1.  <span data-ttu-id="32288-134">Ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="32288-134">Run your project.</span></span>  
1.  <span data-ttu-id="32288-135">Arrastre y coloque el archivo `contoso.txt` en el control WebView.</span><span class="sxs-lookup"><span data-stu-id="32288-135">Drag-and-drop the `contoso.txt` file onto the WebView control.</span></span>  <span data-ttu-id="32288-136">Se abre una nueva ventana, que es el resultado del código del proyecto de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="32288-136">A new window opens, which is the result of the code in your sample project.</span></span>  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Resultado de arrastrar y colocar contoso.txt" lightbox="./media/dragtext.png":::
       <span data-ttu-id="32288-138">Resultado de arrastrar y colocar contoso.txt</span><span class="sxs-lookup"><span data-stu-id="32288-138">Result of dragging and dropping contoso.txt</span></span>  
    :::image-end:::  

<span data-ttu-id="32288-139">Ahora, agregue código para quitar la funcionalidad de arrastrar y colocar del control WebView2.</span><span class="sxs-lookup"><span data-stu-id="32288-139">Now, add code to remove the drag-and-drop functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="32288-140">Copie y pegue el siguiente fragmento de código `InitializeAsync()` en `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="32288-140">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  <span data-ttu-id="32288-141">Ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="32288-141">Run your project.</span></span>  
1.  <span data-ttu-id="32288-142">Intente arrastrar y colocar `contoso.txt` .</span><span class="sxs-lookup"><span data-stu-id="32288-142">Try to drag-and-drop `contoso.txt`.</span></span>  <span data-ttu-id="32288-143">Confirme que no puede arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="32288-143">Confirm that you are not able to drag-and-drop.</span></span>  

## <a name="scenario--removing-the-context-menu"></a><span data-ttu-id="32288-144">Escenario: quitar el menú contextual</span><span class="sxs-lookup"><span data-stu-id="32288-144">Scenario:  Removing the Context Menu</span></span>  

<span data-ttu-id="32288-145">En esta sección, quite el menú contextual predeterminado del control WebView2.</span><span class="sxs-lookup"><span data-stu-id="32288-145">In this section, remove the default context menu from your WebView2 control.</span></span>  

<span data-ttu-id="32288-146">Para empezar, explore la funcionalidad del menú contextual actual.</span><span class="sxs-lookup"><span data-stu-id="32288-146">To begin, explore the current contextual menu functionality.</span></span>  

1.  <span data-ttu-id="32288-147">Ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="32288-147">Run your project.</span></span>  
1.  <span data-ttu-id="32288-148">Mantenga el mouse en cualquier lugar del control WebView2 y abra el menú contextual \(hacer clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="32288-148">Hover anywhere on the WebView2 control and open the context menu \(right-click\).</span></span>  <span data-ttu-id="32288-149">El menú contextual muestra las opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="32288-149">The context menu displays the default choices.</span></span>  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Menú contextual que muestra las opciones predeterminadas" lightbox="./media/contextmenu.png":::
       <span data-ttu-id="32288-151">Menú contextual que muestra las opciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="32288-151">The context menu showing the default choices</span></span>  
    :::image-end:::  
    
<span data-ttu-id="32288-152">Ahora agregue código para quitar la funcionalidad del menú contextual del control WebView2.</span><span class="sxs-lookup"><span data-stu-id="32288-152">Now add code to remove the contextual menu functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="32288-153">Copie y pegue el siguiente fragmento de código `InitializeAsync()` en `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="32288-153">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  <span data-ttu-id="32288-154">Vuelva a ejecutar el código.</span><span class="sxs-lookup"><span data-stu-id="32288-154">Run the code again.</span></span>  <span data-ttu-id="32288-155">Confirme que no puede abrir un menú contextual \(hacer clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="32288-155">Confirm that you're not able to open a context menu \(right-click\).</span></span>  
   
## <a name="see-also"></a><span data-ttu-id="32288-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="32288-156">See also</span></span>  

*   <span data-ttu-id="32288-157">Para obtener más información sobre cómo empezar a usar WebView2, vaya a [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="32288-157">For more information on getting started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="32288-158">Para obtener un ejemplo completo de las funcionalidades de WebView2, vaya al repositorio [WebView2Samples][GithubMicrosoftedgeWebview2samples] en GitHub.</span><span class="sxs-lookup"><span data-stu-id="32288-158">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>  
*   <span data-ttu-id="32288-159">Para obtener información detallada sobre las API de WebView2, vaya a [Referencia de api][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="32288-159">For detailed information on WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>  
*   <span data-ttu-id="32288-160">Para obtener más información sobre WebView2, vaya a [Recursos de WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="32288-160">For more information on WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="32288-161">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="32288-161">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  


[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2 API Reference | Microsoft Docs"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Introducción a WebView2 en WPF (versión preliminar) | Microsoft Docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated - 0.9.579 - interfaz ICoreWebView2 | Microsoft Docs"  
[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

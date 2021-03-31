---
description: Guía de introducción a WebView2 para aplicaciones de Win32
title: Introducción a WebView2 para aplicaciones de Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones win32, win32, edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, edge html
ms.openlocfilehash: 19bc0c5600ebd072ad9a6aa61d2a965e999865ce
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306162"
---
# <span data-ttu-id="5113b-104">Introducción a WebView2</span><span class="sxs-lookup"><span data-stu-id="5113b-104">Getting started with WebView2</span></span>  

<span data-ttu-id="5113b-105">En este artículo, empieza a crear tu primera aplicación WebView2 y obtén información sobre las características principales [de WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="5113b-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="5113b-106">Para obtener más información acerca de las API webView2 individuales, vaya a la [referencia de la API.][Webview2ReferenceWin32]</span><span class="sxs-lookup"><span data-stu-id="5113b-106">For more information about individual WebView2 APIs, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <span data-ttu-id="5113b-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5113b-107">Prerequisites</span></span>  

<span data-ttu-id="5113b-108">Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="5113b-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="5113b-109">[WebView2 Runtime][Webview2Installer] o cualquier canal no estable de [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado en el sistema operativo compatible \(actualmente Windows 10, Windows 8.1 y Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="5113b-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5113b-110">El equipo de WebView recomienda usar el canal Canary y la versión mínima necesaria es 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="5113b-110">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="5113b-111">[Visual Studio][MicrosoftVisualstudioMain] 2015 o posterior con compatibilidad con C++ instalada.</span><span class="sxs-lookup"><span data-stu-id="5113b-111">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  
    
## <span data-ttu-id="5113b-112">Paso 1: Crear una aplicación de una sola ventana</span><span class="sxs-lookup"><span data-stu-id="5113b-112">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="5113b-113">Comience con un proyecto de escritorio básico que contenga una sola ventana principal.</span><span class="sxs-lookup"><span data-stu-id="5113b-113">Start with a basic desktop project that contains a single main window.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="5113b-114">Para centrar mejor el tutorial, usa código de ejemplo modificado de [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span><span class="sxs-lookup"><span data-stu-id="5113b-114">To better focus the walkthrough, use modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="5113b-115">Para descargar el ejemplo modificado y empezar a trabajar, vaya a [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="5113b-115">To download the modified sample and get started, navigate to [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

1.  <span data-ttu-id="5113b-116">En Visual Studio, abra `WebView2GettingStarted.sln` .</span><span class="sxs-lookup"><span data-stu-id="5113b-116">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  
    <span data-ttu-id="5113b-117">Si usa una versión anterior de Visual Studio, mantenga el puntero sobre el proyecto **WebView2GettingStarted,** abra el menú contextual \(haga clic con el botón secundario\) y elija **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="5113b-117">If you use an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and choose **Properties**.</span></span>  <span data-ttu-id="5113b-118">En **Propiedades de configuración**general, modifica la versión de Windows SDK y el conjunto de herramientas de plataforma para usar el SDK de Win10 y Visual Studio herramientas disponibles para  >   ti.  </span><span class="sxs-lookup"><span data-stu-id="5113b-118">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset available to you.</span></span>  

:::image type="complex" source="../media/tool-version.png" alt-text="Versión de la herramienta" lightbox="../media/tool-version.png":::
   <span data-ttu-id="5113b-120">Versión de la herramienta</span><span class="sxs-lookup"><span data-stu-id="5113b-120">Tool version</span></span>  
:::image-end:::  

<span data-ttu-id="5113b-121">Visual Studio pueden mostrar errores, porque al proyecto le falta el archivo de encabezado WebView2.</span><span class="sxs-lookup"><span data-stu-id="5113b-121">Visual Studio may display errors, because your project is missing the WebView2 header file.</span></span>  <span data-ttu-id="5113b-122">Los errores deben corregirse después [del paso 2.](#step-2---install-webview2-sdk)</span><span class="sxs-lookup"><span data-stu-id="5113b-122">The errors should be fixed after [Step 2](#step-2---install-webview2-sdk).</span></span>  

## <span data-ttu-id="5113b-123">Paso 2: Instalar el SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="5113b-123">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="5113b-124">Agregue el SDK de WebView2 al proyecto.</span><span class="sxs-lookup"><span data-stu-id="5113b-124">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="5113b-125">Usa NuGet para instalar el SDK de Win32.</span><span class="sxs-lookup"><span data-stu-id="5113b-125">Use NuGet to install the Win32 SDK.</span></span>  

1.  <span data-ttu-id="5113b-126">Mantenga el puntero sobre el proyecto, abra el menú contextual \(right-click\) y elija **Administrar paquetes NuGet**.</span><span class="sxs-lookup"><span data-stu-id="5113b-126">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Administrar paquetes NuGet" lightbox="../media/manage-nuget-packages.png":::
       <span data-ttu-id="5113b-128">Administrar paquetes NuGet</span><span class="sxs-lookup"><span data-stu-id="5113b-128">Manage NuGet packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5113b-129">Instala la biblioteca de implementación de Windows.</span><span class="sxs-lookup"><span data-stu-id="5113b-129">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="5113b-130">En la barra de búsqueda, `Microsoft.Windows.ImplementationLibrary` escriba > **Microsoft.Windows.ImplementationLibrary**.</span><span class="sxs-lookup"><span data-stu-id="5113b-130">In the search bar, type `Microsoft.Windows.ImplementationLibrary` > choose **Microsoft.Windows.ImplementationLibrary**.</span></span>  
    1.  <span data-ttu-id="5113b-131">En la ventana del lado derecho, elija **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="5113b-131">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="5113b-132">NuGet descarga la biblioteca en el equipo.</span><span class="sxs-lookup"><span data-stu-id="5113b-132">NuGet downloads the library to your machine.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="5113b-133">La [biblioteca de implementación de Windows][GithubMicrosoftWilMain] y la biblioteca de plantillas [C++][CppCxWrlTemplateLibraryVS2019] de Windows Runtime son opcionales y facilitan el trabajo con COM para el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5113b-133">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Biblioteca de implementación de Windows" lightbox="../media/wil.png":::
           <span data-ttu-id="5113b-135">Biblioteca de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="5113b-135">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="5113b-136">Instale el SDK de WebView2.</span><span class="sxs-lookup"><span data-stu-id="5113b-136">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="5113b-137">En la barra de búsqueda, `Microsoft.Web.WebView2` escriba > **seleccione Microsoft.Web.WebView2**.</span><span class="sxs-lookup"><span data-stu-id="5113b-137">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    1.  <span data-ttu-id="5113b-138">En la ventana del lado derecho, elija **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="5113b-138">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="5113b-139">NuGet descarga el SDK en el equipo.</span><span class="sxs-lookup"><span data-stu-id="5113b-139">NuGet downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet Administrador de paquetes" lightbox="../media/nuget.png":::
           <span data-ttu-id="5113b-141">NuGet Administrador de paquetes</span><span class="sxs-lookup"><span data-stu-id="5113b-141">NuGet Package Manager</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="5113b-142">Agregue el encabezado WebView2 al proyecto.</span><span class="sxs-lookup"><span data-stu-id="5113b-142">Add WebView2 header to your project.</span></span>  
    :::row:::
       :::column span="1":::
          <span data-ttu-id="5113b-143">En el `HelloWebView.cpp` archivo, copie el siguiente fragmento de código y péguelo después de la última `#include` línea.</span><span class="sxs-lookup"><span data-stu-id="5113b-143">In the `HelloWebView.cpp` file, copy the following code snippet and paste it after the last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="5113b-144">La sección include debe ser similar al siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="5113b-144">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="5113b-145">Listo para usarse y compilarse con la API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="5113b-145">Ready to use and build against the WebView2 API.</span></span>  

### <span data-ttu-id="5113b-146">Crear una aplicación de ejemplo vacía</span><span class="sxs-lookup"><span data-stu-id="5113b-146">Build your empty sample app</span></span>  

<span data-ttu-id="5113b-147">Para compilar y ejecutar la aplicación de ejemplo, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="5113b-147">To build and run the sample app, select `F5`.</span></span>  <span data-ttu-id="5113b-148">La aplicación muestra una ventana vacía.</span><span class="sxs-lookup"><span data-stu-id="5113b-148">Your app displays an empty window.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Aplicación vacía" lightbox="../media/empty-app.png":::
   <span data-ttu-id="5113b-150">Aplicación vacía</span><span class="sxs-lookup"><span data-stu-id="5113b-150">Empty app</span></span>  
:::image-end:::  

## <span data-ttu-id="5113b-151">Paso 3: Crear una sola vista web dentro de la ventana primaria</span><span class="sxs-lookup"><span data-stu-id="5113b-151">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="5113b-152">Agrega una vista web a la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="5113b-152">Add a WebView to the main window.</span></span>  

 <span data-ttu-id="5113b-153">Usa el método para configurar el entorno y localizar el `CreateCoreWebView2Environment` explorador Microsoft Edge \(Chromium\) que encienda el control.</span><span class="sxs-lookup"><span data-stu-id="5113b-153">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="5113b-154">También puede usar el método si desea especificar la ubicación del explorador, la carpeta de usuario, las marcas del explorador, entre otros, en lugar de usar `CreateCoreWebView2EnvironmentWithOptions` la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5113b-154">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="5113b-155">Una vez completado el método, ejecute el método dentro de la devolución de llamada y ejecute el `CreateCoreWebView2Environment` método para obtener la vista web `ICoreWebView2Environment::CreateCoreWebView2Controller` `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` `ICoreWebView2Controller::get_CoreWebView2` asociada.</span><span class="sxs-lookup"><span data-stu-id="5113b-155">Upon the completion of the `CreateCoreWebView2Environment` method, run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="5113b-156">En la devolución de llamada, establece algunas opciones más, cambia el tamaño de WebView para que tome el 100 % de la ventana principal y navega a Bing.</span><span class="sxs-lookup"><span data-stu-id="5113b-156">In the callback, set a few more settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="5113b-157">Copie el siguiente fragmento de código y péguelo `HelloWebView.cpp` después del comentario y antes del `// <-- WebView2 sample code starts here -->` `// <-- WebView2 sample code ends here -->` comentario.</span><span class="sxs-lookup"><span data-stu-id="5113b-157">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` comment and before the `// <-- WebView2 sample code ends here -->` comment.</span></span>  

```cpp
// Step 3 - Create a single WebView within the parent window
// Locate the browser and set up the environment for WebView
CreateCoreWebView2EnvironmentWithOptions(nullptr, nullptr, nullptr,
    Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
        [hWnd](HRESULT result, ICoreWebView2Environment* env) -> HRESULT {
        
            // Create a CoreWebView2Controller and get the associated CoreWebView2 whose parent is the main window hWnd
            env->CreateCoreWebView2Controller(hWnd, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                [hWnd](HRESULT result, ICoreWebView2Controller* controller) -> HRESULT {
                if (controller != nullptr) {
                    webviewController = controller;
                    webviewController->get_CoreWebView2(&webviewWindow);
                }
                
                // Add a few settings for the webview
                // The demo step is redundant since the values are the default settings
                ICoreWebView2Settings* Settings;
                webviewWindow->get_Settings(&Settings);
                Settings->put_IsScriptEnabled(TRUE);
                Settings->put_AreDefaultScriptDialogsEnabled(TRUE);
                Settings->put_IsWebMessageEnabled(TRUE);
                
                // Resize WebView to fit the bounds of the parent window
                RECT bounds;
                GetClientRect(hWnd, &bounds);
                webviewController->put_Bounds(bounds);
                
                // Schedule an async task to navigate to Bing
                webviewWindow->Navigate(L"https://www.bing.com/");
                
                // Step 4 - Navigation events
                
                // Step 5 - Scripting
                
                // Step 6 - Communication between host and web content
                
                return S_OK;
            }).Get());
        return S_OK;
    }).Get());
```  

### <span data-ttu-id="5113b-158">Crear una aplicación de ejemplo de Bing</span><span class="sxs-lookup"><span data-stu-id="5113b-158">Build your Bing sample app</span></span>  

<span data-ttu-id="5113b-159">Para compilar y ejecutar la aplicación, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="5113b-159">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="5113b-160">Ahora tiene una ventana WebView que muestra la página de Bing.</span><span class="sxs-lookup"><span data-stu-id="5113b-160">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Ventana de Bing" lightbox="../media/bing-window.png":::
   <span data-ttu-id="5113b-162">Ventana de Bing</span><span class="sxs-lookup"><span data-stu-id="5113b-162">Bing window</span></span>  
:::image-end:::  

## <span data-ttu-id="5113b-163">Paso 4: Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="5113b-163">Step 4 - Navigation events</span></span>  

<span data-ttu-id="5113b-164">El equipo de WebView ya ha cubierto la navegación a la dirección URL mediante `ICoreWebView2::Navigate` el método en el último paso.</span><span class="sxs-lookup"><span data-stu-id="5113b-164">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="5113b-165">Durante la navegación, WebView dispara una secuencia de eventos a los que el host puede escuchar.</span><span class="sxs-lookup"><span data-stu-id="5113b-165">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

<span data-ttu-id="5113b-166">Para obtener más información, vaya a [Eventos de navegación.][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="5113b-166">For more information, navigate to [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación" lightbox="../media/navigation-events.png":::
   <span data-ttu-id="5113b-168">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="5113b-168">Navigation events</span></span>  
:::image-end:::  

<span data-ttu-id="5113b-169">En los casos de error, uno o varios de los siguientes eventos pueden producirse en función de si la navegación continúa hacia una página web de error.</span><span class="sxs-lookup"><span data-stu-id="5113b-169">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

> [!NOTE]
> <span data-ttu-id="5113b-170">Si se produce un redireccionamiento HTTP, hay varios `NavigationStarting` eventos en una fila.</span><span class="sxs-lookup"><span data-stu-id="5113b-170">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="5113b-171">Como ejemplo de uso de los eventos, registre un controlador para el evento para cancelar las solicitudes `NavigationStarting` que no son https.</span><span class="sxs-lookup"><span data-stu-id="5113b-171">As an example of using the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="5113b-172">Copie el siguiente fragmento de código y péguelo en `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="5113b-172">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

```cpp
// register an ICoreWebView2NavigationStartingEventHandler to cancel any non-https navigation
EventRegistrationToken token;
webviewWindow->add_NavigationStarting(Callback<ICoreWebView2NavigationStartingEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2NavigationStartingEventArgs * args) -> HRESULT {
        PWSTR uri;
        args->get_Uri(&uri);
        std::wstring source(uri);
        if (source.substr(0, 5) != L"https") {
            args->put_Cancel(true);
        }
        CoTaskMemFree(uri);
        return S_OK;
    }).Get(), &token);
```  

<span data-ttu-id="5113b-173">Ahora, la aplicación no navega a ningún sitio que no sea https.</span><span class="sxs-lookup"><span data-stu-id="5113b-173">Now the app does not navigate to any non-https sites.</span></span>  <span data-ttu-id="5113b-174">Puede usar un mecanismo similar para realizar otras tareas, como restringir la navegación a su propio dominio.</span><span class="sxs-lookup"><span data-stu-id="5113b-174">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <span data-ttu-id="5113b-175">Paso 5: Scripting</span><span class="sxs-lookup"><span data-stu-id="5113b-175">Step 5 - Scripting</span></span>  

<span data-ttu-id="5113b-176">Puedes usar aplicaciones host para insertar código JavaScript en controles WebView2 en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5113b-176">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="5113b-177">Puede hacer que WebView ejecute JavaScript arbitrario o agregue scripts de inicialización.</span><span class="sxs-lookup"><span data-stu-id="5113b-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="5113b-178">El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a todos los fotogramas secundarios hasta que se quite el JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5113b-178">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="5113b-179">El JavaScript inyectado se ejecuta con intervalos específicos.</span><span class="sxs-lookup"><span data-stu-id="5113b-179">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="5113b-180">Ejecutarlo después de la creación del objeto global.</span><span class="sxs-lookup"><span data-stu-id="5113b-180">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="5113b-181">Ejecutarlo antes de ejecutar cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="5113b-181">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="5113b-182">Copie el siguiente fragmento de código y péguelo en `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="5113b-182">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

```cpp
// Schedule an async task to add initialization script that freezes the Object object
webviewWindow->AddScriptToExecuteOnDocumentCreated(L"Object.freeze(Object);", nullptr);
// Schedule an async task to get the document URL
webviewWindow->ExecuteScript(L"window.document.URL;", Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
    [](HRESULT errorCode, LPCWSTR resultObjectAsJson) -> HRESULT {
        LPCWSTR URL = resultObjectAsJson;
        //doSomethingWithURL(URL);
        return S_OK;
    }).Get());
```  

<span data-ttu-id="5113b-183">Ahora, WebView siempre debe inmovilizar el `Object` objeto y devuelve el documento de página una vez.</span><span class="sxs-lookup"><span data-stu-id="5113b-183">Now, WebView should always freeze the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="5113b-184">Las API de inserción de scripts \(y algunas otras API de WebView2\) son asincrónicas, debes usar devoluciones de llamada si el código debe ejecutarse en un orden específico.</span><span class="sxs-lookup"><span data-stu-id="5113b-184">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <span data-ttu-id="5113b-185">Paso 6: Comunicación entre contenido de host y web</span><span class="sxs-lookup"><span data-stu-id="5113b-185">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="5113b-186">El host y el contenido web también pueden comunicarse entre sí a través del `postMessage` método.</span><span class="sxs-lookup"><span data-stu-id="5113b-186">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="5113b-187">El contenido web que se ejecuta en una vista web puede publicarse en el host a través del método y el mensaje lo controla cualquier controlador de eventos registrado `window.chrome.webview.postMessage` `ICoreWebView2WebMessageReceivedEventHandler` en el host.</span><span class="sxs-lookup"><span data-stu-id="5113b-187">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="5113b-188">Del mismo modo, el host puede enviar mensajes al contenido web a través o al método, que son capturados por `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` controladores agregados desde el agente de `window.chrome.webview.addEventListener` escucha.</span><span class="sxs-lookup"><span data-stu-id="5113b-188">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="5113b-189">El mecanismo de comunicación permite que el contenido web use funcionalidades nativas pasando mensajes para pedir al host que ejecute API nativas.</span><span class="sxs-lookup"><span data-stu-id="5113b-189">The communication mechanism allows the web content to use native capabilities by passing messages to ask the host to run native APIs.</span></span>  

<span data-ttu-id="5113b-190">Como ejemplo para comprender el mecanismo, se producen los siguientes pasos al intentar generar la dirección URL del documento en WebView.</span><span class="sxs-lookup"><span data-stu-id="5113b-190">As an example to understand the mechanism, the following steps occur when you try to output the document URL in WebView.</span></span>  

1.  <span data-ttu-id="5113b-191">El host registra un controlador para devolver el mensaje recibido al contenido web</span><span class="sxs-lookup"><span data-stu-id="5113b-191">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="5113b-192">El host inserta un script en el contenido web que registra un controlador para imprimir el mensaje del host</span><span class="sxs-lookup"><span data-stu-id="5113b-192">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="5113b-193">El host inserta un script en el contenido web que publica la dirección URL en el host</span><span class="sxs-lookup"><span data-stu-id="5113b-193">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="5113b-194">El controlador del host se desencadena y devuelve el mensaje \(la dirección URL\) al contenido web</span><span class="sxs-lookup"><span data-stu-id="5113b-194">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="5113b-195">El controlador del contenido web se desencadena e imprime el mensaje desde el host \(la dirección URL\)</span><span class="sxs-lookup"><span data-stu-id="5113b-195">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  

<span data-ttu-id="5113b-196">Copie el siguiente fragmento de código y péguelo en `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="5113b-196">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

```cpp
// Set an event handler for the host to return received message back to the web content
webviewWindow->add_WebMessageReceived(Callback<ICoreWebView2WebMessageReceivedEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2WebMessageReceivedEventArgs * args) -> HRESULT {
        PWSTR message;
        args->TryGetWebMessageAsString(&message);
        // processMessage(&message);
        webview->PostWebMessageAsString(message);
        CoTaskMemFree(message);
        return S_OK;
    }).Get(), &token);

// Schedule an async task to add initialization script that
// 1) Add an listener to print message from the host
// 2) Post document URL to the host
webviewWindow->AddScriptToExecuteOnDocumentCreated(
    L"window.chrome.webview.addEventListener(\'message\', event => alert(event.data));" \
    L"window.chrome.webview.postMessage(window.document.URL);",
nullptr);
```  

### <span data-ttu-id="5113b-197">Crear una aplicación de ejemplo de dirección URL para mostrar</span><span class="sxs-lookup"><span data-stu-id="5113b-197">Build your display URL sample app</span></span>  

<span data-ttu-id="5113b-198">Para compilar y ejecutar la aplicación, seleccione `F5` .</span><span class="sxs-lookup"><span data-stu-id="5113b-198">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="5113b-199">La dirección URL aparece en una ventana emergente antes de navegar a una página web.</span><span class="sxs-lookup"><span data-stu-id="5113b-199">The URL appears in a pop-up window before navigating to a webpage.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="Url para mostrar" lightbox="../media/show-url.png":::
   <span data-ttu-id="5113b-201">Url para mostrar</span><span class="sxs-lookup"><span data-stu-id="5113b-201">Display url</span></span>  
:::image-end:::  

<span data-ttu-id="5113b-202">Enhorabuena, has creado tu primera aplicación WebView2.</span><span class="sxs-lookup"><span data-stu-id="5113b-202">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="5113b-203">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="5113b-203">Next steps</span></span>  

<span data-ttu-id="5113b-204">Muchas de las funcionalidades de WebView2 no se tratan en este artículo, la siguiente sección proporciona más recursos.</span><span class="sxs-lookup"><span data-stu-id="5113b-204">Many of the WebView2 functionalities are not covered on this article, the following section provides more resources.</span></span>  

### <span data-ttu-id="5113b-205">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5113b-205">See also</span></span>  

*   <span data-ttu-id="5113b-206">Para obtener un ejemplo completo de las funcionalidades de WebView2, vaya a la muestra [de API de WebView2.][GithubMicrosoftedgeWebview2samplesApisample]</span><span class="sxs-lookup"><span data-stu-id="5113b-206">For a comprehensive example of WebView2 capabilities, navigate to [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="5113b-207">Para obtener una aplicación de ejemplo creada con WebView2, vaya a [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span><span class="sxs-lookup"><span data-stu-id="5113b-207">For a sample app built using WebView2, navigate to [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="5113b-208">Para obtener información detallada sobre la API de WebView2, vaya a la [referencia de la API.][Webview2ReferenceWin32]</span><span class="sxs-lookup"><span data-stu-id="5113b-208">For detailed information about the WebView2 API, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <span data-ttu-id="5113b-209">Introducción al equipo de Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="5113b-209">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Desarrollador de Microsoft Edge"  

[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++ Reference | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegación | Microsoft Docs"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Biblioteca de plantillas C++ de Windows Runtime (WRL) | Microsoft Docs"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Walkthrough: Create a traditional Windows Desktop application (C++) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser - MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "Ejemplo de API de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Bibliotecas de implementación de Windows (WIL): microsoft/wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador de WebView2"  

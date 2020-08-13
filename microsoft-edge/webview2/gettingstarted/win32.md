---
description: Hospedar contenido web en la aplicación Win32 con el control de WebView 2 de Microsoft Edge
title: Introducción a WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: ec5144f911d5bf00f141d1e8e53718154f1cbb24
ms.sourcegitcommit: 4bc904c5d54347185f275bd76441975be471c320
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/12/2020
ms.locfileid: "10926487"
---
# <span data-ttu-id="32d0b-104">Introducción a WebView2 (vista previa para desarrolladores)</span><span class="sxs-lookup"><span data-stu-id="32d0b-104">Getting started with WebView2 (developer preview)</span></span>  

<span data-ttu-id="32d0b-105">El siguiente contenido le muestra las funciones más comunes de [WebView2 (Developer Preview)][Webview2Index] y proporciona un punto de partida para crear su primera aplicación de WebView2.</span><span class="sxs-lookup"><span data-stu-id="32d0b-105">The following content walks you through the commonly used functionalities of [WebView2 (developer preview)][Webview2Index] and provides a starting  point for creating your first WebView2 app.</span></span>  <span data-ttu-id="32d0b-106">Para obtener más información sobre las API de WebView2 individuales, consulta referencia de la [API][Webview2ReferenceWin3209538].</span><span class="sxs-lookup"><span data-stu-id="32d0b-106">For more information about individual WebView2 APIs, see [API reference][Webview2ReferenceWin3209538].</span></span>  

## <span data-ttu-id="32d0b-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="32d0b-107">Prerequisites</span></span>  

*   <span data-ttu-id="32d0b-108">[Microsoft Edge (cromo)][MicrosoftedgeinsiderDownload] instalado en el SO compatible \ (actualmente Windows 10, Windows 8,1 y Windows 7 \).</span><span class="sxs-lookup"><span data-stu-id="32d0b-108">[Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="32d0b-109">El equipo de WebView recomienda usar el canal Canarias y la versión mínima requerida es 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="32d0b-109">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="32d0b-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 o posterior con compatibilidad con C++ instalado.</span><span class="sxs-lookup"><span data-stu-id="32d0b-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  

## <span data-ttu-id="32d0b-111">Paso 1: crear una sola aplicación Win32 de ventana</span><span class="sxs-lookup"><span data-stu-id="32d0b-111">Step 1 - Create a single window win32 app</span></span>  

<span data-ttu-id="32d0b-112">Empiece con un proyecto de escritorio básico que contenga una única ventana principal.</span><span class="sxs-lookup"><span data-stu-id="32d0b-112">Start with a basic desktop project containing a single main window.</span></span>  <span data-ttu-id="32d0b-113">Para centrar mejor el tutorial, está usando código de ejemplo modificado de [Tutorial: crear una aplicación de escritorio de Windows tradicional (C++)][CppWindowsWalkthroughCreatingDesktopApplication] para la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="32d0b-113">To better focus the walkthrough, you are using modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="32d0b-114">Para descargar el ejemplo modificado y empezar, consulta [ejemplos de WebView2][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="32d0b-114">To download the modified sample and get started, see [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

<span data-ttu-id="32d0b-115">En Visual Studio, Abra `WebView2GettingStarted.sln` .</span><span class="sxs-lookup"><span data-stu-id="32d0b-115">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  <span data-ttu-id="32d0b-116">Si está usando una versión anterior de Visual Studio, mantenga el puntero sobre el proyecto **WebView2GettingStarted** , abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="32d0b-116">If you are using an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and select **Properties**.</span></span>  <span data-ttu-id="32d0b-117">En **propiedades de configuración**  >  **General**, modifique la **versión del SDK de Windows** y el conjunto de herramientas de **plataforma** para usar el SDK de Win10 y el conjunto de herramientas de Visual Studio \ (vs Toolset \) que tiene a su disposición.</span><span class="sxs-lookup"><span data-stu-id="32d0b-117">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset \(VS toolset\) available to you.</span></span>  

:::image type="complex" source="../media/tool-version.png" alt-text="Versión de la herramienta":::
   <span data-ttu-id="32d0b-119">Versión de la herramienta</span><span class="sxs-lookup"><span data-stu-id="32d0b-119">Tool version</span></span>  
:::image-end:::  

<span data-ttu-id="32d0b-120">Visual Studio puede mostrar algunos errores porque falta el archivo de encabezado WebView2, que debería desaparecer después de completar el paso 2.</span><span class="sxs-lookup"><span data-stu-id="32d0b-120">Visual Studio may show some errors due to missing WebView2 header file, which should go away after Step 2 is completed.</span></span>  

## <span data-ttu-id="32d0b-121">Paso 2: instalar el SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="32d0b-121">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="32d0b-122">Agregue el SDK de WebView2 al proyecto.</span><span class="sxs-lookup"><span data-stu-id="32d0b-122">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="32d0b-123">Para la versión preliminar de desarrollador, puedes instalar el SDK de Win32 con Nuget.</span><span class="sxs-lookup"><span data-stu-id="32d0b-123">For the developer preview, you may install the Win32 SDK using Nuget.</span></span>  

1.  <span data-ttu-id="32d0b-124">Mantenga el puntero sobre el proyecto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **administrar paquetes Nuget**.</span><span class="sxs-lookup"><span data-stu-id="32d0b-124">Hover on the project, open the contextual menu \(right-click\), and select **Manage Nuget Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Administrar paquetes Nuget":::
       <span data-ttu-id="32d0b-126">Administrar paquetes Nuget</span><span class="sxs-lookup"><span data-stu-id="32d0b-126">Manage Nuget packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="32d0b-127">Instale la biblioteca de implementación de Windows.</span><span class="sxs-lookup"><span data-stu-id="32d0b-127">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="32d0b-128">Escriba `Microsoft.Windows.ImplementationLibrary` en la barra de búsqueda, seleccione **Microsoft. Windows. ImplementationLibrary** de los resultados y seleccione **instalar** en la ventana de la derecha.</span><span class="sxs-lookup"><span data-stu-id="32d0b-128">Enter `Microsoft.Windows.ImplementationLibrary` in the search bar, select **Microsoft.Windows.ImplementationLibrary** from the results, and select **Install** in the right-hand side window.</span></span>  <span data-ttu-id="32d0b-129">Nuget descarga el SDK en tu equipo.</span><span class="sxs-lookup"><span data-stu-id="32d0b-129">Nuget downloads the SDK to your machine.</span></span>  
        
        > [!NOTE] 
        > <span data-ttu-id="32d0b-130">La biblioteca de [implementación de Windows][GithubMicrosoftWilMain] y la biblioteca de plantillas de [C++ de Windows Runtime][CppCxWrlTemplateLibraryVS2019] son opcionales y se han agregado para facilitar el trabajo con com.</span><span class="sxs-lookup"><span data-stu-id="32d0b-130">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and were added to make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Biblioteca de implementación de Windows":::
           <span data-ttu-id="32d0b-132">Biblioteca de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="32d0b-132">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="32d0b-133">Instale el SDK de WebView2.</span><span class="sxs-lookup"><span data-stu-id="32d0b-133">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="32d0b-134">Escriba `Microsoft.Web.WebView2` en la barra de búsqueda, seleccione **Microsoft. Web. WebView2** de los resultados y seleccione **instalar** en la ventana de la derecha.</span><span class="sxs-lookup"><span data-stu-id="32d0b-134">Enter `Microsoft.Web.WebView2` in the search bar, select **Microsoft.Web.WebView2** from the results, and select **Install** in the right-hand side window.</span></span>  <span data-ttu-id="32d0b-135">Nuget descarga el SDK en tu equipo.</span><span class="sxs-lookup"><span data-stu-id="32d0b-135">Nuget downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="Nuget":::
           <span data-ttu-id="32d0b-137">Nuget</span><span class="sxs-lookup"><span data-stu-id="32d0b-137">Nuget</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="32d0b-138">Agregue el encabezado WebView2 al proyecto.</span><span class="sxs-lookup"><span data-stu-id="32d0b-138">Add WebView2 header to your project.</span></span>  
    :::row:::
       :::column span="1":::
          <span data-ttu-id="32d0b-139">Abra `HelloWebView.cpp` , copie el siguiente fragmento de código y péguelo `HelloWebView.cpp` después de la última `#include` línea.</span><span class="sxs-lookup"><span data-stu-id="32d0b-139">Open `HelloWebView.cpp`, copy the following code snippet and paste into `HelloWebView.cpp` after last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="32d0b-140">La sección de inclusión debe tener un aspecto similar al siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="32d0b-140">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="32d0b-141">Estás listo para usar y compilar en la API de WebView2.</span><span class="sxs-lookup"><span data-stu-id="32d0b-141">You are all set to use and build against the WebView2 API.</span></span>  

### <span data-ttu-id="32d0b-142">Crear la aplicación de ejemplo vacía</span><span class="sxs-lookup"><span data-stu-id="32d0b-142">Build your empty sample app</span></span>  

<span data-ttu-id="32d0b-143">Pulse `F5` para compilar y ejecutar la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="32d0b-143">Press `F5` to build and run the sample app.</span></span>  <span data-ttu-id="32d0b-144">Debería ver una aplicación que muestra una ventana vacía.</span><span class="sxs-lookup"><span data-stu-id="32d0b-144">You should see an app displaying an empty window.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Aplicación vacía":::
   <span data-ttu-id="32d0b-146">Aplicación vacía</span><span class="sxs-lookup"><span data-stu-id="32d0b-146">Empty app</span></span>  
:::image-end:::  

## <span data-ttu-id="32d0b-147">Paso 3: crear un único WebView en la ventana principal</span><span class="sxs-lookup"><span data-stu-id="32d0b-147">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="32d0b-148">Agregue una vista previa a la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="32d0b-148">Add a WebView to the main window.</span></span>  <span data-ttu-id="32d0b-149">Use el `CreateCoreWebView2Environment` método para configurar el entorno y busque el explorador Microsoft Edge \ (cromo \) encendido del control.</span><span class="sxs-lookup"><span data-stu-id="32d0b-149">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="32d0b-150">También puede usar el `CreateCoreWebView2EnvironmentWithOptions` método si desea especificar la ubicación del explorador, la carpeta de usuario, las marcas del explorador, etc., en lugar de usar la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="32d0b-150">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="32d0b-151">Una vez finalizado el `CreateCoreWebView2Environment` método, podrá ejecutar el `ICoreWebView2Environment::CreateCoreWebView2Controller` método dentro de la devolución de `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` llamada y ejecutar el `ICoreWebView2Controller::get_CoreWebView2` método para obtener la vista previa asociada.</span><span class="sxs-lookup"><span data-stu-id="32d0b-151">Upon the completion of the `CreateCoreWebView2Environment` method, you are able to run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="32d0b-152">En la devolución de llamada, establezca algunas opciones de configuración adicionales, cambie el tamaño de la vista de sitio para que tome el 100% de la ventana primaria y vaya a Bing.</span><span class="sxs-lookup"><span data-stu-id="32d0b-152">In the callback, set a few additional settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="32d0b-153">Copie el siguiente fragmento de código y péguelo `HelloWebView.cpp` después de la `// <-- WebView2 sample code starts here -->` Nota y antes de la `// <-- WebView2 sample code ends here -->` Nota.</span><span class="sxs-lookup"><span data-stu-id="32d0b-153">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` note and before the `// <-- WebView2 sample code ends here -->` note.</span></span>  

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


### <span data-ttu-id="32d0b-154">Crear la aplicación de ejemplo de Bing</span><span class="sxs-lookup"><span data-stu-id="32d0b-154">Build your Bing sample app</span></span>  

<span data-ttu-id="32d0b-155">Pulse `F5` para compilar y ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32d0b-155">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="32d0b-156">Ahora tiene una ventana de vista Web que muestra la página de Bing.</span><span class="sxs-lookup"><span data-stu-id="32d0b-156">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Ventana de Bing":::
   <span data-ttu-id="32d0b-158">Ventana de Bing</span><span class="sxs-lookup"><span data-stu-id="32d0b-158">Bing window</span></span>  
:::image-end:::  

## <span data-ttu-id="32d0b-159">Paso 4: eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="32d0b-159">Step 4 - Navigation events</span></span>  

<span data-ttu-id="32d0b-160">El equipo de WebView ya cubre la navegación a la dirección URL con el `ICoreWebView2::Navigate` método del último paso.</span><span class="sxs-lookup"><span data-stu-id="32d0b-160">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="32d0b-161">Durante la navegación, WebView desencadena una secuencia de eventos a los que puede escuchar el host.</span><span class="sxs-lookup"><span data-stu-id="32d0b-161">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

<span data-ttu-id="32d0b-162">Para obtener más información, vea [eventos de navegación][Webview2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="32d0b-162">For more information, see [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación":::
   <span data-ttu-id="32d0b-164">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="32d0b-164">Navigation events</span></span>  
:::image-end:::  

<span data-ttu-id="32d0b-165">En casos de error, pueden producirse uno o varios de los siguientes eventos dependiendo de si la navegación continúa en una página de error.</span><span class="sxs-lookup"><span data-stu-id="32d0b-165">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

<span data-ttu-id="32d0b-166">En el caso de una redirección HTTP, hay varios `NavigationStarting` eventos en una fila.</span><span class="sxs-lookup"><span data-stu-id="32d0b-166">In case of an HTTP redirect, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="32d0b-167">Como ejemplo de uso de los eventos, registra un controlador para el `NavigationStarting` evento y cancela las solicitudes que no sean https.</span><span class="sxs-lookup"><span data-stu-id="32d0b-167">As an example of utilizing the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="32d0b-168">Copie el siguiente fragmento de código y péguelo en él `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="32d0b-168">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="32d0b-169">Ahora la aplicación no está navegando a ningún sitio que no sea HTTPS.</span><span class="sxs-lookup"><span data-stu-id="32d0b-169">Now the app is not navigating to any non-https sites.</span></span>  <span data-ttu-id="32d0b-170">Puede usar un mecanismo similar para realizar otras tareas, como restringir la navegación a dentro de su propio dominio.</span><span class="sxs-lookup"><span data-stu-id="32d0b-170">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <span data-ttu-id="32d0b-171">Paso 5: scripting</span><span class="sxs-lookup"><span data-stu-id="32d0b-171">Step 5 - Scripting</span></span>  

<span data-ttu-id="32d0b-172">La aplicación de hospedaje también puede inyectar JavaScript en WebView.</span><span class="sxs-lookup"><span data-stu-id="32d0b-172">The hosting app may also inject JavaScript into WebView.</span></span>  <span data-ttu-id="32d0b-173">Puede usar la vista previa de tareas para ejecutar JavaScript arbitrario o agregar scripts de inicialización.</span><span class="sxs-lookup"><span data-stu-id="32d0b-173">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="32d0b-174">Los scripts de inicialización agregados se aplican a todos los futuros documentos de nivel superior y navegación de Marcos secundarios hasta que se eliminan y se ejecutan después de que se haya creado el objeto global y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="32d0b-174">Added initialization scripts apply to all future top level document and child frame navigation until removed, and run after the global object has been created and before any other script included by the HTML document is run.</span></span>  

<span data-ttu-id="32d0b-175">Copie el siguiente fragmento de código y péguelo en él `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="32d0b-175">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="32d0b-176">Ahora WebView debería inmovilizar siempre el `Object` objeto y devuelve el documento de página una vez.</span><span class="sxs-lookup"><span data-stu-id="32d0b-176">Now WebView should always freezes the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="32d0b-177">Las API de inyección de script \ (y otras API de WebView2 \) son asincrónicas, por lo que debe usar devoluciones de llamada si el código debe ejecutarse en un orden específico.</span><span class="sxs-lookup"><span data-stu-id="32d0b-177">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <span data-ttu-id="32d0b-178">Paso 6: comunicación entre el host y el contenido web</span><span class="sxs-lookup"><span data-stu-id="32d0b-178">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="32d0b-179">El host y el contenido web también pueden comunicarse con ellos a través del `postMessage` método.</span><span class="sxs-lookup"><span data-stu-id="32d0b-179">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="32d0b-180">El contenido web que se ejecuta en una vista Web puede publicarse en el host mediante el `window.chrome.webview.postMessage` método y cualquier otro registro del `ICoreWebView2WebMessageReceivedEventHandler` controlador de eventos registrado en el host controla el mensaje.</span><span class="sxs-lookup"><span data-stu-id="32d0b-180">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="32d0b-181">Del mismo modo, el anfitrión puede enviar un mensaje a través de la web mediante `ICoreWebView2::PostWebMessageAsString` o `ICoreWebView2::PostWebMessageAsJSON` método, que los controladores han agregado desde la `window.chrome.webview.addEventListener` escucha.</span><span class="sxs-lookup"><span data-stu-id="32d0b-181">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="32d0b-182">El mecanismo de comunicación permite que el contenido web use capacidades nativas al pasar mensajes para solicitar al host que llame a las API nativas.</span><span class="sxs-lookup"><span data-stu-id="32d0b-182">The communication mechanism allows the web content to utilize native capabilities by passing messages to ask the host to call native APIs.</span></span>  

<span data-ttu-id="32d0b-183">Como ejemplo para comprender el mecanismo, los pasos siguientes se producen al intentar imprimir la dirección URL del documento en WebView.</span><span class="sxs-lookup"><span data-stu-id="32d0b-183">As an example to understand the mechanism, the following steps occur when you try printing out the document URL in WebView.</span></span>  

1.  <span data-ttu-id="32d0b-184">El anfitrión registra un controlador para devolver el mensaje recibido al contenido web</span><span class="sxs-lookup"><span data-stu-id="32d0b-184">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="32d0b-185">El anfitrión inyecta un script en el contenido web que registra un controlador para imprimir el mensaje desde el host</span><span class="sxs-lookup"><span data-stu-id="32d0b-185">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="32d0b-186">El anfitrión inyecta un script en el contenido web que publica la dirección URL en el host.</span><span class="sxs-lookup"><span data-stu-id="32d0b-186">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="32d0b-187">El controlador del host se desencadena y devuelve el mensaje \ (la dirección URL \) en el contenido Web.</span><span class="sxs-lookup"><span data-stu-id="32d0b-187">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="32d0b-188">El controlador del contenido web se desencadena e imprime un mensaje desde el host \ (la dirección URL \)</span><span class="sxs-lookup"><span data-stu-id="32d0b-188">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  

<span data-ttu-id="32d0b-189">Copie el siguiente fragmento de código y péguelo en él `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="32d0b-189">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>    

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

### <span data-ttu-id="32d0b-190">Crear la aplicación Mostrar URL de muestra</span><span class="sxs-lookup"><span data-stu-id="32d0b-190">Build your show URL sample app</span></span>  

<span data-ttu-id="32d0b-191">Pulse `F5` para compilar y ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32d0b-191">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="32d0b-192">Debería ver la dirección URL en una ventana emergente antes de navegar a una página.</span><span class="sxs-lookup"><span data-stu-id="32d0b-192">You should see the URL in a pop-up window prior to navigating to a page.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="Mostrar URL":::
   <span data-ttu-id="32d0b-194">Mostrar URL</span><span class="sxs-lookup"><span data-stu-id="32d0b-194">Show url</span></span>  
:::image-end:::  

<span data-ttu-id="32d0b-195">¡ Enhorabuena! ¡ acabas de crear tu primera WebView2 aplicación!</span><span class="sxs-lookup"><span data-stu-id="32d0b-195">Congratulations, you just built your first WebView2 app!</span></span>  

## <span data-ttu-id="32d0b-196">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="32d0b-196">Next steps</span></span>  

<span data-ttu-id="32d0b-197">Muchas de las funcionalidades de WebView2 que no se cubren en esta página, la siguiente sección proporcionaba recursos adicionales.</span><span class="sxs-lookup"><span data-stu-id="32d0b-197">Many of the WebView2 functionalities that are not covered on this page, the following section provided additional resources.</span></span>  

### <span data-ttu-id="32d0b-198">Consulte también</span><span class="sxs-lookup"><span data-stu-id="32d0b-198">See also</span></span>  

*   <span data-ttu-id="32d0b-199">Para obtener un ejemplo completo de las capacidades de WebView2, consulta la [muestra de API de WebView2][GithubMicrosoftedgeWebview2samplesApisample].</span><span class="sxs-lookup"><span data-stu-id="32d0b-199">For a comprehensive example of WebView2 capabilities, see [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="32d0b-200">Para obtener una aplicación de muestra creada con WebView2, consulte [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span><span class="sxs-lookup"><span data-stu-id="32d0b-200">For a sample application built using WebView2, see [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="32d0b-201">Para obtener información detallada sobre la API de WebView2, consulta referencia de la [API][Webview2ReferenceWin3209538].</span><span class="sxs-lookup"><span data-stu-id="32d0b-201">For detailed information about the WebView2 API, see [API reference][Webview2ReferenceWin3209538].</span></span>  

## <span data-ttu-id="32d0b-202">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="32d0b-202">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegación | Microsoft docs"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019 "Biblioteca de plantillas C++ de Windows en tiempo de ejecución (WRL) | Microsoft docs"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019 "Tutorial: crear una aplicación de escritorio de Windows tradicional (C++) | Microsoft docs"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser-MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "Ejemplo de API de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Bibliotecas de implementación de Windows (superservicio)-Microsoft/| GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar los canales de Insider de Microsoft Edge"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

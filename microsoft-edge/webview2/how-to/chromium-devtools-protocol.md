---
description: Obtenga información sobre cómo usar el protocolo DevTools de Chrome en las aplicaciones de WebView2 con el paquete Microsoft Edge WebView2 Chromium protocolo DevTools NuGet de desarrollo
title: Usar el protocolo DevTools de Chrome en WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Chrome DevTools Protocol
ms.openlocfilehash: cd59bc0d177d17680222fcff8452c2cf8d56b195
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536200"
---
# <a name="use-chromium-devtools-protocol-in-webview2"></a><span data-ttu-id="8dc2d-104">Usar el protocolo Chromium DevTools en WebView2</span><span class="sxs-lookup"><span data-stu-id="8dc2d-104">Use Chromium DevTools Protocol in WebView2</span></span>  

<span data-ttu-id="8dc2d-105">El [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol] proporciona API para instrumentar, inspeccionar, depurar y perfilar exploradores basados Chromium web.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-105">The [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol] provides APIs to instrument, inspect, debug, and profile Chromium-based browsers.</span></span>  <span data-ttu-id="8dc2d-106">El Chromium DevTools protocol es la base para Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-106">The Chromium DevTools Protocol is the foundation for the Microsoft Edge \(Chromium\) DevTools.</span></span>  <span data-ttu-id="8dc2d-107">Use el Chromium de DevTools para las características que no se implementan en la plataforma WebView2.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-107">Use the Chromium DevTools Protocol for features that aren't implemented in the WebView2 platform.</span></span>  <span data-ttu-id="8dc2d-108">Para obtener más información acerca de Chromium funcionalidad del Protocolo de DevTools, vaya [a Chromium protocolo DevTools][GitHubChromedevtoolsDevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="8dc2d-108">For more information about the Chromium DevTools Protocol functionality, navigate to [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol].</span></span>  

> [!CAUTION]
> <span data-ttu-id="8dc2d-109">El Microsoft Edge WebView2 no mantiene ni admite el Chromium DevTools Protocol.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-109">The Microsoft Edge WebView2 team does not maintain or support the Chromium DevTools Protocol.</span></span>  <span data-ttu-id="8dc2d-110">El Chromium de DevTools se mantiene mediante el proyecto de código Chromium abierto.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-110">The Chromium DevTools Protocol is maintained by the open source Chromium project.</span></span>  
> 
> <span data-ttu-id="8dc2d-111">Para enviar sugerencias sobre las futuras características de la plataforma WebView2, vaya a Comentarios de [WebView][GithubMicrosoftedgeWebview2feedback] y envíe un problema.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-111">To send your suggestions for future WebView2 platform features, navigate to [WebView Feedback][GithubMicrosoftedgeWebview2feedback] and submit an issue.</span></span>  

<span data-ttu-id="8dc2d-112">Para usar la API Chromium protocolo DevTools en WebView2, use cualquiera de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-112">To use the Chromium DevTools Protocol API in WebView2, use either of the following actions.</span></span>  

*   <span data-ttu-id="8dc2d-113">Instale y use el paquete [de microsoft.Web.WebView2.DevToolsProtocolExtension (versión preliminar)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet paquete \(.NET\).</span><span class="sxs-lookup"><span data-stu-id="8dc2d-113">Install and use the [Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet package \(.NET\).</span></span>  
*   <span data-ttu-id="8dc2d-114">Ejecute uno de los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-114">Run one of the following methods.</span></span>  
    *   <span data-ttu-id="8dc2d-115">.NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]</span><span class="sxs-lookup"><span data-stu-id="8dc2d-115">.NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]</span></span>  
    *   <span data-ttu-id="8dc2d-116">Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]</span><span class="sxs-lookup"><span data-stu-id="8dc2d-116">Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]</span></span>  
    
## <a name="use-devtoolsprotocolhelper-preview"></a><span data-ttu-id="8dc2d-117">Usar DevToolsProtocolHelper (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="8dc2d-117">Use DevToolsProtocolHelper (Preview)</span></span>

> [!NOTE]
> <span data-ttu-id="8dc2d-118">El [paquete DevToolsProtocolExtension de Microsoft.Web.WebView2.DevToolsProtocolExtension][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet se encuentra actualmente en versión preliminar técnica.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-118">The [Microsoft.Web.WebView2.DevToolsProtocolExtension][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet package is currently in technical preview.</span></span>  <span data-ttu-id="8dc2d-119">Mientras esté en versión preliminar, no use el paquete en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-119">While in preview, refrain from using the package in production apps.</span></span>

<span data-ttu-id="8dc2d-120">[Microsoft.Web.WebView2.DevToolsProtocolExtension (versión preliminar)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] es un paquete de NuGet creado por el equipo de WebView2 que proporciona un fácil acceso Chromium características del protocolo DevTools.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-120">[Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] is a NuGet package created by the WebView2 team that provides easy access to Chromium DevTools Protocol features.</span></span>  <span data-ttu-id="8dc2d-121">En los ejemplos siguientes se describe cómo usar la funcionalidad de geolocalización en Chromium protocolo DevTools en el control WebView2.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-121">The following examples describe how to use the geolocation functionality in Chromium DevTools Protocol in your WebView2 control.</span></span>  <span data-ttu-id="8dc2d-122">Puede seguir un patrón similar para usar otras Chromium de protocolo DevTools.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-122">You may follow a similar pattern to use other Chromium DevTools Protocol features.</span></span>  

## <a name="step-1-create-a-webpage-to-find-your-geolocation"></a><span data-ttu-id="8dc2d-123">Paso 1: Crear una página web para buscar la geolocalización</span><span class="sxs-lookup"><span data-stu-id="8dc2d-123">Step 1: Create a webpage to find your geolocation</span></span>  

<span data-ttu-id="8dc2d-124">Para crear una `HTML file` para buscar la geolocalización, complete siguiendo las acciones.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-124">To create an `HTML file` to find your geolocation, complete following the actions.</span></span>  

1.  <span data-ttu-id="8dc2d-125">Abra Visual Studio Code \(o un IDE de su elección\).</span><span class="sxs-lookup"><span data-stu-id="8dc2d-125">Open Visual Studio Code \(or an IDE of your choice\).</span></span>  
1.  <span data-ttu-id="8dc2d-126">Cree un archivo `.html` nuevo.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-126">Create a new `.html` file.</span></span>  
1.  <span data-ttu-id="8dc2d-127">Copie y pegue el siguiente fragmento de código en el nuevo `.html` archivo.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-127">Copy and paste the following code snippet in your new `.html` file.</span></span>  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>Geolocation Finder</title>
    </head>
    <body>
        <button id="display">Display Location</button>
        <div id="message"></div>
    </body>
    
    <script>
        const btn = document.getElementById('display');
        // Find the user location.
        btn.addEventListener('click', function () {
            navigator.geolocation.getCurrentPosition(onSuccess, onError);
        });
        
        // Update message to display the latitude and longitude coordinates.
        function onSuccess(position) {
            const {latitude, longitude} = position.coords;
            message.textContent = `Your location: (${latitude},${longitude})`;
        }
        
        function onError() {
            message.textContent = `Operation Failed`;
        }
    </script>
    </html>
    ```  
    
1.  <span data-ttu-id="8dc2d-128">Guarde el `.html` archivo con el nombre de archivo `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="8dc2d-128">Save the `.html` file with the filename `geolocation.html`.</span></span>  
1.  <span data-ttu-id="8dc2d-129">Abra Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-129">Open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="8dc2d-130">Abre el archivo `geolocation.html`.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-130">Open the `geolocation.html` file.</span></span>  
1.  <span data-ttu-id="8dc2d-131">Para mostrar las coordenadas de latitud y longitud, elija el **botón Mostrar** ubicación.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-131">To display your latitude and longitude coordinates, choose the **Display Location** button.</span></span>  <span data-ttu-id="8dc2d-132">Para comprobar y comparar la geolocalización, copie y pegue las coordenadas en [https://www.bing.com/maps][BingMaps] .</span><span class="sxs-lookup"><span data-stu-id="8dc2d-132">To verify and compare your geolocation, copy and paste your coordinates in [https://www.bing.com/maps][BingMaps].</span></span>  
    
    :::image type="complex" source="./media/geolocater-browser.png" alt-text="Mostrar las coordenadas de geolocalización del usuario en Microsoft Edge" lightbox="./media/geolocater-browser.png":::
       <span data-ttu-id="8dc2d-134">Mostrar las coordenadas de geolocalización del usuario en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8dc2d-134">Display the geolocation coordinates of the user in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="step-2-display-geolocationhtml-in-a-webview2"></a><span data-ttu-id="8dc2d-135">Paso 2: Mostrar geolocation.html en un WebView2</span><span class="sxs-lookup"><span data-stu-id="8dc2d-135">Step 2: Display geolocation.html in a WebView2</span></span>  

1.  <span data-ttu-id="8dc2d-136">Para crear una aplicación WebView2, usa cualquiera de las siguientes guías de introducción o ejemplos de WebView2.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-136">To create a WebView2 app, use either of the following get started guides or WebView2 samples.</span></span>  
    *   [<span data-ttu-id="8dc2d-137">Introducción webView2 en Windows forms</span><span class="sxs-lookup"><span data-stu-id="8dc2d-137">Get Started with WebView2 in Windows Forms</span></span>][Webview2GetStartedWinforms]  
    *   [<span data-ttu-id="8dc2d-138">Introducción webView2 en WPF</span><span class="sxs-lookup"><span data-stu-id="8dc2d-138">Get Started with WebView2 in WPF</span></span>][Webview2GetStartedWpf]  
    *   [<span data-ttu-id="8dc2d-139">Ejemplos de WebView2</span><span class="sxs-lookup"><span data-stu-id="8dc2d-139">WebView2 samples</span></span>][GithubMicrosoftedgeWebview2samples]  
        
1.  <span data-ttu-id="8dc2d-140">Establezca la navegación inicial del control WebView2 en `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="8dc2d-140">Set the initial navigation of the WebView2 control to `geolocation.html`.</span></span>  
    
    ```csharp
    webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    ```  
    
1.  <span data-ttu-id="8dc2d-141">Asegúrate de `geolocation.html` que el archivo se muestre en la aplicación de control WebView2.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-141">Ensure the `geolocation.html` file displays in your WebView2 control app.</span></span>  
    
    :::image type="complex" source="./media/initial-geolocate.png" alt-text="Mostrar el geolocater.html en la aplicación de control WebView2" lightbox="./media/initial-geolocate.png":::
       <span data-ttu-id="8dc2d-143">Mostrar el `geolocation.html` archivo en la aplicación de control WebView2</span><span class="sxs-lookup"><span data-stu-id="8dc2d-143">Display the `geolocation.html` file in your WebView2 control app</span></span>  
    :::image-end:::  
    
## <a name="step-3-install-the-devtoolsprotocolhelper-nuget-package"></a><span data-ttu-id="8dc2d-144">Paso 3: Instalar el paquete de NuGet DevToolsProtocolHelper</span><span class="sxs-lookup"><span data-stu-id="8dc2d-144">Step 3: Install the DevToolsProtocolHelper NuGet package</span></span>  

<span data-ttu-id="8dc2d-145">Use NuGet para descargar `Microsoft.Web.WebView2.DevToolsProtocolExtension` .</span><span class="sxs-lookup"><span data-stu-id="8dc2d-145">Use NuGet to download `Microsoft.Web.WebView2.DevToolsProtocolExtension`.</span></span>  <span data-ttu-id="8dc2d-146">Para instalar el paquete, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-146">To install the package, complete the following actions.</span></span>  

1.  <span data-ttu-id="8dc2d-147">Elija **Project**  >  **Manage NuGet Packages**  >  **Browse**.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-147">Choose **Project** > **Manage NuGet Packages** > **Browse**.</span></span>  
1.  <span data-ttu-id="8dc2d-148">Escriba `Microsoft.Web.WebView2.DevToolsProtocolExtension` y elija **Microsoft.Web.WebView2.DevToolsProtocolExtension**  >  **Install**.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-148">Type `Microsoft.Web.WebView2.DevToolsProtocolExtension` and choose **Microsoft.Web.WebView2.DevToolsProtocolExtension** > **Install**.</span></span>   
    
:::image type="complex" source="./media/cdp-nuget.png" alt-text="Asegúrese de que Microsoft.Web.WebView2.DevToolsProtocolExtension se muestra en el Visual Studio NuGet Administrador de paquetes" lightbox="./media/cdp-nuget.png":::
   <span data-ttu-id="8dc2d-150">Asegúrese **de que Microsoft.Web.WebView2.DevToolsProtocolExtension** se muestra en el Visual Studio NuGet Administrador de paquetes</span><span class="sxs-lookup"><span data-stu-id="8dc2d-150">Ensure **Microsoft.Web.WebView2.DevToolsProtocolExtension** displays in the Visual Studio NuGet Package Manager</span></span>  
:::image-end:::    

## <a name="step-4-use-devtools-protocol-helper"></a><span data-ttu-id="8dc2d-151">Paso 4: Usar devTools Protocol Helper</span><span class="sxs-lookup"><span data-stu-id="8dc2d-151">Step 4: Use DevTools Protocol Helper</span></span>  

1.  <span data-ttu-id="8dc2d-152">Agregue el `DevToolsProtocolExtension` espacio de nombres al proyecto.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-152">Add the `DevToolsProtocolExtension` namespace to your project.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    using Microsoft.Web.WebView2.Core.DevToolsProtocolExtension;
    ```  
    
1.  <span data-ttu-id="8dc2d-153">Cree una instancia del `DevToolsProtocolHelper` objeto y navegue a `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="8dc2d-153">Instantiate the `DevToolsProtocolHelper` object and navigate to `geolocation.html`.</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webView.CoreWebView2.GetDevToolsProtocolHelper(); 
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    }
    ```  
    
1.  <span data-ttu-id="8dc2d-154">Ejecute el [método setGeoLocationOverrideAsync.][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]</span><span class="sxs-lookup"><span data-stu-id="8dc2d-154">Run the [setGeoLocationOverrideAsync][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride] method.</span></span>  <span data-ttu-id="8dc2d-155">Para obtener más información, vaya [a setGeolocationOverride][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride].</span><span class="sxs-lookup"><span data-stu-id="8dc2d-155">For more information, navigate to [setGeolocationOverride][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride].</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webview.CoreWebView2.GetDevToolsProtocolHelper();
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
        
        // Latitude and longitude for Paris, France.
        double latitude = 48.857024082572565;  
        double longitude = 2.3161581601457386;  
        double accuracy = 1;
        await helper.Emulation.setGeolocationOverrideAsync(latitude, longitude, accuracy);
        
    }
    ```  
    
1.  <span data-ttu-id="8dc2d-156">Ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-156">Run your app.</span></span>  
1.  <span data-ttu-id="8dc2d-157">Para mostrar las coordenadas de París, Francia, elija el botón **Mostrar** ubicación.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-157">To display the coordinates of Paris, France, choose the **Display Location** button.</span></span>  
    
    :::image type="complex" source="./media/final-location-cdp.png" alt-text="Mostrar el .html en un control WebView2 con las coordenadas de París" lightbox="./media/final-location-cdp.png":::
       <span data-ttu-id="8dc2d-159">Mostrar el `.html` archivo en un control WebView2 con las coordenadas de París</span><span class="sxs-lookup"><span data-stu-id="8dc2d-159">Display the `.html` file in a WebView2 control with the coordinates for Paris</span></span>  
    :::image-end:::  
    
## <a name="file-a-chromium-devtools-protocol-bug"></a><span data-ttu-id="8dc2d-160">Archivo de un Chromium de protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="8dc2d-160">File a Chromium DevTools Protocol bug</span></span>  

<span data-ttu-id="8dc2d-161">El equipo de WebView2 no es propietario del Chromium DevTools Protocol.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-161">The WebView2 team doesn't own the Chromium DevTools Protocol.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="8dc2d-162">Dirija los comentarios y los errores al repositorio Chromium problemas.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-162">Direct feedback and bugs to the Chromium Issues repo.</span></span>  

<span data-ttu-id="8dc2d-163">Para presentar un error Chromium o un problema del Protocolo DevTools, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-163">To file a Chromium DevTools Protocol bug or issue, complete the following actions.</span></span>  

1.  <span data-ttu-id="8dc2d-164">Archivo de un [informe de errores][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform].</span><span class="sxs-lookup"><span data-stu-id="8dc2d-164">File a [bug report][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform].</span></span>  
1.  <span data-ttu-id="8dc2d-165">Vaya a [Comentarios de WebView][GithubMicrosoftedgeWebview2feedback] y abra un nuevo problema.</span><span class="sxs-lookup"><span data-stu-id="8dc2d-165">Navigate to [WebView Feedback][GithubMicrosoftedgeWebview2feedback] and open a new issue.</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="8dc2d-166">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8dc2d-166">See also</span></span>  

*   [<span data-ttu-id="8dc2d-167">Ejemplos de WebView2</span><span class="sxs-lookup"><span data-stu-id="8dc2d-167">WebView2 samples</span></span>][GithubMicrosoftedgeWebview2samples]  
    
 <!-- links -->  

[Webview2GetStartedWinforms]: /microsoft-edge/webview2/get-started/winforms "Introducción a WebView2 en Windows Forms | Microsoft Docs"  
[Webview2GetStartedWpf]: /microsoft-edge/webview2/get-started/wpf "Introducción a WebView2 en WPF | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]: /dotnet/api/microsoft.web.webview2.core.corewebview2.getdevtoolsprotocoleventreceiver?view=webview2-dotnet-1.0.774.44&preserve-view=true "Método CoreWebView2.GetDevToolsProtocolEventReceiver(String) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString]: /dotnet/api/microsoft.web.webview2.core.corewebview2.calldevtoolsprotocolmethodasync?view=webview2-dotnet-1.0.774.44&preserve-view=true#Microsoft_Web_WebView2_Core_CoreWebView2_CallDevToolsProtocolMethodAsync_System_String_System_String_ "Método CoreWebView2.CallDevToolsProtocolMethodAsync(String, String) | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-1.0.774.44&preserve-view=true#calldevtoolsprotocolmethod "CallDevToolsProtocolMethod: interfaz ICoreWebView2 | Microsoft Docs"  
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-1.0.774.44&preserve-view=true "interfaz ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs"  

[BingMaps]: https://www.bing.com/maps "mapas de Bing"  

[GitHubChromedevtoolsDevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Protocolo Chrome DevTools | GitHub"  
[GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]: https://chromedevtools.github.io/devtools-protocol/tot/Emulation/#method-setGeolocationOverride "Emulation.setGeolocationOverride- Chrome DevTools Protocol | GitHub"  

[GithubMicrosoftedgeWebview2feedback]: https://github.com/MicrosoftEdge/WebView2Feedback "Comentarios de WebView | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2 | GitHub"  

[ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]: https://bugs.chromium.org/p/chromium/issues/entry?components=Platform%3EDevTools%3EPlatform "Informe de errores | Chromium Errores"  

[NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension]: https://www.nuget.org/packages/Microsoft.Web.WebView2.DevToolsProtocolExtension "Microsoft.Web.WebView2.DevToolsProtocolExtension | NuGet Galería de QA"  

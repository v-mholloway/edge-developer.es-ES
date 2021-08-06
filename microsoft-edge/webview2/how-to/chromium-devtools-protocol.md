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
ms.openlocfilehash: 16504587d70be184760627ac224cf8a12f0f7e024cba7c729ac23cb6734bad36
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11803201"
---
# <a name="use-chromium-devtools-protocol-in-webview2"></a>Usar el protocolo DevTools de Chromium en WebView2  

El [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol] proporciona API para instrumentar, inspeccionar, depurar y perfilar exploradores basados Chromium web.  El Chromium DevTools protocol es la base para Microsoft Edge \(Chromium\) DevTools.  Use el Chromium de DevTools para las características que no se implementan en la plataforma WebView2.  Para obtener más información acerca de Chromium funcionalidad del Protocolo de DevTools, vaya [a Chromium protocolo DevTools][GitHubChromedevtoolsDevtoolsProtocol].  

> [!CAUTION]
> El Microsoft Edge WebView2 no mantiene ni admite el Chromium DevTools Protocol.  El Chromium de DevTools se mantiene mediante el proyecto de código Chromium abierto.  
> 
> Para enviar sugerencias sobre las futuras características de la plataforma WebView2, vaya a Comentarios de [WebView][GithubMicrosoftedgeWebview2feedback] y envíe un problema.  

Para usar la API Chromium protocolo DevTools en WebView2, use cualquiera de las siguientes acciones.  

*   Instale y use el paquete [de microsoft.Web.WebView2.DevToolsProtocolExtension (versión preliminar)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet paquete \(.NET\).  
*   Ejecute uno de los métodos siguientes.  
    *   .NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]  
    *   Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]  
    
## <a name="use-devtoolsprotocolhelper-preview"></a>Usar DevToolsProtocolHelper (versión preliminar)

> [!NOTE]
> El [paquete DevToolsProtocolExtension de Microsoft.Web.WebView2.DevToolsProtocolExtension][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet se encuentra actualmente en versión preliminar técnica.  Mientras esté en versión preliminar, no use el paquete en aplicaciones de producción.

[Microsoft.Web.WebView2.DevToolsProtocolExtension (versión preliminar)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] es un paquete de NuGet creado por el equipo de WebView2 que proporciona un fácil acceso Chromium características del protocolo DevTools.  En los ejemplos siguientes se describe cómo usar la funcionalidad de geolocalización en Chromium protocolo DevTools en el control WebView2.  Puede seguir un patrón similar para usar otras Chromium de protocolo DevTools.  

## <a name="step-1-create-a-webpage-to-find-your-geolocation"></a>Paso 1: Crear una página web para buscar la geolocalización  

Para crear una `HTML file` para buscar la geolocalización, complete siguiendo las acciones.  

1.  Abra Visual Studio Code \(o un IDE de su elección\).  
1.  Cree un archivo `.html` nuevo.  
1.  Copie y pegue el siguiente fragmento de código en el nuevo `.html` archivo.  
    
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
    
1.  Guarde el `.html` archivo con el nombre de archivo `geolocation.html` .  
1.  Abra Microsoft Edge.  
1.  Abre el archivo `geolocation.html`.  
1.  Para mostrar las coordenadas de latitud y longitud, elija el **botón Mostrar** ubicación.  Para comprobar y comparar la geolocalización, copie y pegue las coordenadas en [https://www.bing.com/maps][BingMaps] .  
    
    :::image type="complex" source="./media/geolocater-browser.png" alt-text="Mostrar las coordenadas de geolocalización del usuario en Microsoft Edge" lightbox="./media/geolocater-browser.png":::
       Mostrar las coordenadas de geolocalización del usuario en Microsoft Edge  
    :::image-end:::  
    
## <a name="step-2-display-geolocationhtml-in-a-webview2"></a>Paso 2: Mostrar geolocation.html en un WebView2  

1.  Para crear una aplicación WebView2, usa cualquiera de las siguientes guías de introducción o ejemplos de WebView2.  
    *   [Introducción webView2 en Windows forms][Webview2GetStartedWinforms]  
    *   [Introducción webView2 en WPF][Webview2GetStartedWpf]  
    *   [Ejemplos de WebView2][GithubMicrosoftedgeWebview2samples]  
        
1.  Establezca la navegación inicial del control WebView2 en `geolocation.html` .  
    
    ```csharp
    webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    ```  
    
1.  Asegúrate de `geolocation.html` que el archivo se muestre en la aplicación de control WebView2.  
    
    :::image type="complex" source="./media/initial-geolocate.png" alt-text="Mostrar el geolocater.html en la aplicación de control WebView2" lightbox="./media/initial-geolocate.png":::
       Mostrar el `geolocation.html` archivo en la aplicación de control WebView2  
    :::image-end:::  
    
## <a name="step-3-install-the-devtoolsprotocolhelper-nuget-package"></a>Paso 3: Instalar el paquete de NuGet DevToolsProtocolHelper  

Use NuGet para descargar `Microsoft.Web.WebView2.DevToolsProtocolExtension` .  Para instalar el paquete, complete las siguientes acciones.  

1.  Elija **Project**  >  **Manage NuGet Packages**  >  **Browse**.  
1.  Escriba `Microsoft.Web.WebView2.DevToolsProtocolExtension` y elija **Microsoft.Web.WebView2.DevToolsProtocolExtension**  >  **Install**.   
    
:::image type="complex" source="./media/cdp-nuget.png" alt-text="Asegúrese de que Microsoft.Web.WebView2.DevToolsProtocolExtension se muestra en el Visual Studio NuGet Administrador de paquetes" lightbox="./media/cdp-nuget.png":::
   Asegúrese **de que Microsoft.Web.WebView2.DevToolsProtocolExtension** se muestra en el Visual Studio NuGet Administrador de paquetes  
:::image-end:::    

## <a name="step-4-use-devtools-protocol-helper"></a>Paso 4: Usar devTools Protocol Helper  

1.  Agregue el `DevToolsProtocolExtension` espacio de nombres al proyecto.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    using Microsoft.Web.WebView2.Core.DevToolsProtocolExtension;
    ```  
    
1.  Cree una instancia del `DevToolsProtocolHelper` objeto y navegue a `geolocation.html` .  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webView.CoreWebView2.GetDevToolsProtocolHelper(); 
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    }
    ```  
    
1.  Ejecute el [método setGeoLocationOverrideAsync.][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]  Para obtener más información, vaya [a setGeolocationOverride][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride].  
    
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
    
1.  Ejecuta la aplicación.  
1.  Para mostrar las coordenadas de París, Francia, elija el botón **Mostrar** ubicación.  
    
    :::image type="complex" source="./media/final-location-cdp.png" alt-text="Mostrar el .html en un control WebView2 con las coordenadas de París" lightbox="./media/final-location-cdp.png":::
       Mostrar el `.html` archivo en un control WebView2 con las coordenadas de París  
    :::image-end:::  
    
## <a name="file-a-chromium-devtools-protocol-bug"></a>Archivo de un Chromium de protocolo DevTools  

El equipo de WebView2 no es propietario del Chromium DevTools Protocol.  

> [!IMPORTANT]
> Dirija los comentarios y los errores al repositorio Chromium problemas.  

Para presentar un error Chromium o un problema del Protocolo DevTools, complete las siguientes acciones.  

1.  Archivo de un [informe de errores][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform].  
1.  Vaya a [Comentarios de WebView][GithubMicrosoftedgeWebview2feedback] y abra un nuevo problema.  
    
## <a name="see-also"></a>Consulte también  

*   [Ejemplos de WebView2][GithubMicrosoftedgeWebview2samples]  
    
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

---
description: Aprende a usar el protocolo Chrome DevTools en tus aplicaciones webView2 con el paquete NuGet del protocolo DevTools de Chromium de Microsoft Edge WebView2
title: Usar el protocolo DevTools de Chrome en WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Chrome DevTools Protocol
ms.openlocfilehash: 0f7a2dd4bb3b1621e854cd4c0c5410e64d3c03ff
ms.sourcegitcommit: 0ef5bb3933cde8a466f2931b824f07b4995cfe5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "11409331"
---
# <a name="use-chromium-devtools-protocol-in-webview2"></a>Usar el protocolo Chromium DevTools en WebView2  

El [protocolo Chromium DevTools][GitHubChromedevtoolsDevtoolsProtocol] proporciona API para instrumentar, inspeccionar, depurar y perfilar exploradores basados en Chromium.  El protocolo Chromium DevTools es la base de Microsoft Edge \(Chromium\) DevTools.  Use el protocolo Chromium DevTools para las características que no se implementan en la plataforma WebView2.  Para obtener más información acerca de la funcionalidad del protocolo Chromium DevTools, vaya a [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol].  

> [!CAUTION]
> El equipo de WebView2 de Microsoft Edge no mantiene ni admite el protocolo Chromium DevTools.  El protocolo Chromium DevTools se mantiene mediante el proyecto chromium de código abierto.  
> 
> Para enviar sugerencias sobre las futuras características de la plataforma WebView2, vaya a Comentarios de [WebView][GithubMicrosoftedgeWebview2feedback] y envíe un problema.  

Para usar la API del protocolo DevTools de Chromium en WebView2, use cualquiera de las siguientes acciones.  

*   Instale y use el [paquete NuGet Microsoft.Web.WebView2.DevToolsProtocolExtension (versión preliminar)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] \(.NET\).  
*   Ejecute uno de los métodos siguientes.  
    *   .NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]  
    *   Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]  
    
## <a name="use-devtoolsprotocolhelper-preview"></a>Usar DevToolsProtocolHelper (versión preliminar)

> [!NOTE]
> El [paquete NuGet Microsoft.Web.WebView2.DevToolsProtocolExtension][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] se encuentra actualmente en versión preliminar técnica.  Mientras esté en versión preliminar, no use el paquete en aplicaciones de producción.

[Microsoft.Web.WebView2.DevToolsProtocolExtension (versión preliminar)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] es un paquete NuGet creado por el equipo de WebView2 que proporciona un fácil acceso a las características del protocolo Chromium DevTools.  En los ejemplos siguientes se describe cómo usar la funcionalidad de geolocalización en el protocolo Chromium DevTools en el control WebView2.  Puede seguir un patrón similar para usar otras características del protocolo Chromium DevTools.  

## <a name="step-1-create-a-webpage-to-find-your-geolocation"></a>Paso 1: Crear una página web para buscar la geolocalización  

Para crear una `HTML file` para buscar la geolocalización, complete siguiendo las acciones.  

1.  Abra Visual Studio \(o un IDE de su elección\).  
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

1.  Para crear una aplicación WebView2, use cualquiera de las siguientes guías de introducción o ejemplos de WebView2.  
    *   [Introducción a WebView2 en Windows Forms][Webview2GettingstartedWinforms]  
    *   [Introducción a WebView2 en WPF][Webview2GettingstartedWpf]  
    *   [Ejemplos de WebView2][GithubMicrosoftedgeWebview2samples]  
        
1.  Establezca la navegación inicial del control WebView2 en `geolocation.html` .  
    
    ```csharp
    webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    ```  
    
1.  Asegúrate de `geolocation.html` que el archivo se muestre en la aplicación de control WebView2.  
    
    :::image type="complex" source="./media/initial-geolocate.png" alt-text="Mostrar el geolocater.html en la aplicación de control WebView2" lightbox="./media/initial-geolocate.png":::
       Mostrar el `geolocation.html` archivo en la aplicación de control WebView2  
    :::image-end:::  
    
## <a name="step-3-install-the-devtoolsprotocolhelper-nuget-package"></a>Paso 3: Instalar el paquete NuGet DevToolsProtocolHelper  

Use NuGet para descargar `Microsoft.Web.WebView2.DevToolsProtocolExtension` .  Para instalar el paquete, complete las siguientes acciones.  

1.  Elija **Project**  >  **Manage NuGet Packages**  >  **Browse**.  
1.  Escriba `Microsoft.Web.WebView2.DevToolsProtocolExtension` y elija **Microsoft.Web.WebView2.DevToolsProtocolExtension**  >  **Install**.   
    
:::image type="complex" source="./media/cdpnuget.png" alt-text="Asegúrese de que Microsoft.Web.WebView2.DevToolsProtocolExtension se muestra en el Visual Studio NuGet Administrador de paquetes" lightbox="./media/cdpnuget.png":::
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
    
    :::image type="complex" source="./media/finallocation-cdp.png" alt-text="Mostrar el archivo .html en un control WebView2 con las coordenadas de París" lightbox="./media/finallocation-cdp.png":::
       Mostrar el `.html` archivo en un control WebView2 con las coordenadas de París  
    :::image-end:::  
    
## <a name="file-a-chromium-devtools-protocol-bug"></a>Archivo de un error del protocolo Chromium DevTools  

El equipo de WebView2 no es propietario del protocolo Chromium DevTools.  

> [!IMPORTANT]
> Dirija los comentarios y los errores al repositorio de problemas de Chromium.  

Para presentar un error o un problema del Protocolo DevTools de Chromium, complete las siguientes acciones.  

1.  Archivo de un [informe de errores][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform].  
1.  Vaya a [Comentarios de WebView][GithubMicrosoftedgeWebview2feedback] y abra un nuevo problema.  
    
## <a name="see-also"></a>Consulte también  

*   [Ejemplos de WebView2][GithubMicrosoftedgeWebview2samples]  
    
 <!-- links -->  

[Webview2GettingstartedWinforms]: /microsoft-edge/webview2/gettingstarted/winforms "Introducción a WebView2 en Windows Forms | Microsoft Docs"  
[Webview2GettingstartedWpf]: /microsoft-edge/webview2/gettingstarted/wpf "Introducción a WebView2 en WPF | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]: /dotnet/api/microsoft.web.webview2.core.corewebview2.getdevtoolsprotocoleventreceiver?view=webview2-dotnet-1.0.774.44&preserve-view=true "Método CoreWebView2.GetDevToolsProtocolEventReceiver(String) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString]: /dotnet/api/microsoft.web.webview2.core.corewebview2.calldevtoolsprotocolmethodasync?view=webview2-dotnet-1.0.774.44&preserve-view=true#Microsoft_Web_WebView2_Core_CoreWebView2_CallDevToolsProtocolMethodAsync_System_String_System_String_ "Método CoreWebView2.CallDevToolsProtocolMethodAsync(String, String) | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-1.0.774.44&preserve-view=true#calldevtoolsprotocolmethod "CallDevToolsProtocolMethod: interfaz ICoreWebView2 | Microsoft Docs"  
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-1.0.774.44&preserve-view=true "interfaz ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs"  

[BingMaps]: https://www.bing.com/maps "Mapas de Bing"  

[GitHubChromedevtoolsDevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Protocolo Chrome DevTools | GitHub"  
[GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]: https://chromedevtools.github.io/devtools-protocol/tot/Emulation/#method-setGeolocationOverride "Emulation.setGeolocationOverride- Chrome DevTools Protocol | GitHub"  

[GithubMicrosoftedgeWebview2feedback]: https://github.com/MicrosoftEdge/WebView2Feedback "Comentarios de WebView | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2 | GitHub"  

[ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]: https://bugs.chromium.org/p/chromium/issues/entry?components=Platform%3EDevTools%3EPlatform "Informe de errores | Errores de Chromium"  

[NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension]: https://int.nugettest.org/packages/Microsoft.Web.WebView2.DevToolsProtocolExtension "Microsoft.Web.WebView2.DevToolsProtocolExtension | Galería nuGet QA"  

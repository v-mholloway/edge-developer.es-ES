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
# Introducción a WebView2  

En este artículo, empieza a crear tu primera aplicación WebView2 y obtén información sobre las características principales [de WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Para obtener más información acerca de las API webView2 individuales, vaya a la [referencia de la API.][Webview2ReferenceWin32]  

## Requisitos previos  

Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar.  

*   [WebView2 Runtime][Webview2Installer] o cualquier canal no estable de [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado en el sistema operativo compatible \(actualmente Windows 10, Windows 8.1 y Windows 7\).  
    
    > [!NOTE]
    > El equipo de WebView recomienda usar el canal Canary y la versión mínima necesaria es 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2015 o posterior con compatibilidad con C++ instalada.  
    
## Paso 1: Crear una aplicación de una sola ventana  

Comience con un proyecto de escritorio básico que contenga una sola ventana principal.  

> [!IMPORTANT]
> Para centrar mejor el tutorial, usa código de ejemplo modificado de [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.  Para descargar el ejemplo modificado y empezar a trabajar, vaya a [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].  

1.  En Visual Studio, abra `WebView2GettingStarted.sln` .  
    Si usa una versión anterior de Visual Studio, mantenga el puntero sobre el proyecto **WebView2GettingStarted,** abra el menú contextual \(haga clic con el botón secundario\) y elija **Propiedades**.  En **Propiedades de configuración**general, modifica la versión de Windows SDK y el conjunto de herramientas de plataforma para usar el SDK de Win10 y Visual Studio herramientas disponibles para  >  **** ti. **** ****  

:::image type="complex" source="../media/tool-version.png" alt-text="Versión de la herramienta" lightbox="../media/tool-version.png":::
   Versión de la herramienta  
:::image-end:::  

Visual Studio pueden mostrar errores, porque al proyecto le falta el archivo de encabezado WebView2.  Los errores deben corregirse después [del paso 2.](#step-2---install-webview2-sdk)  

## Paso 2: Instalar el SDK de WebView2  

Agregue el SDK de WebView2 al proyecto.  Usa NuGet para instalar el SDK de Win32.  

1.  Mantenga el puntero sobre el proyecto, abra el menú contextual \(right-click\) y elija **Administrar paquetes NuGet**.  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Administrar paquetes NuGet" lightbox="../media/manage-nuget-packages.png":::
       Administrar paquetes NuGet  
    :::image-end:::  
    
1.  Instala la biblioteca de implementación de Windows.  
    1.  En la barra de búsqueda, `Microsoft.Windows.ImplementationLibrary` escriba > **Microsoft.Windows.ImplementationLibrary**.  
    1.  En la ventana del lado derecho, elija **Instalar**.  NuGet descarga la biblioteca en el equipo.  
        
        > [!NOTE]
        > La [biblioteca de implementación de Windows][GithubMicrosoftWilMain] y la biblioteca de plantillas [C++][CppCxWrlTemplateLibraryVS2019] de Windows Runtime son opcionales y facilitan el trabajo con COM para el ejemplo.  
        
        :::image type="complex" source="../media/wil.png" alt-text="Biblioteca de implementación de Windows" lightbox="../media/wil.png":::
           Biblioteca de implementación de Windows  
        :::image-end:::  
        
1.  Instale el SDK de WebView2.  
    1.  En la barra de búsqueda, `Microsoft.Web.WebView2` escriba > **seleccione Microsoft.Web.WebView2**.  
    1.  En la ventana del lado derecho, elija **Instalar**.  NuGet descarga el SDK en el equipo.  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet Administrador de paquetes" lightbox="../media/nuget.png":::
           NuGet Administrador de paquetes
        :::image-end:::  
        
1.  Agregue el encabezado WebView2 al proyecto.  
    :::row:::
       :::column span="1":::
          En el `HelloWebView.cpp` archivo, copie el siguiente fragmento de código y péguelo después de la última `#include` línea.  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          La sección include debe ser similar al siguiente fragmento de código.  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
Listo para usarse y compilarse con la API de WebView2.  

### Crear una aplicación de ejemplo vacía  

Para compilar y ejecutar la aplicación de ejemplo, seleccione `F5` .  La aplicación muestra una ventana vacía.  

:::image type="complex" source="../media/empty-app.png" alt-text="Aplicación vacía" lightbox="../media/empty-app.png":::
   Aplicación vacía  
:::image-end:::  

## Paso 3: Crear una sola vista web dentro de la ventana primaria  

Agrega una vista web a la ventana principal.  

 Usa el método para configurar el entorno y localizar el `CreateCoreWebView2Environment` explorador Microsoft Edge \(Chromium\) que encienda el control.  También puede usar el método si desea especificar la ubicación del explorador, la carpeta de usuario, las marcas del explorador, entre otros, en lugar de usar `CreateCoreWebView2EnvironmentWithOptions` la configuración predeterminada.  Una vez completado el método, ejecute el método dentro de la devolución de llamada y ejecute el `CreateCoreWebView2Environment` método para obtener la vista web `ICoreWebView2Environment::CreateCoreWebView2Controller` `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` `ICoreWebView2Controller::get_CoreWebView2` asociada.  

En la devolución de llamada, establece algunas opciones más, cambia el tamaño de WebView para que tome el 100 % de la ventana principal y navega a Bing.  

Copie el siguiente fragmento de código y péguelo `HelloWebView.cpp` después del comentario y antes del `// <-- WebView2 sample code starts here -->` `// <-- WebView2 sample code ends here -->` comentario.  

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

### Crear una aplicación de ejemplo de Bing  

Para compilar y ejecutar la aplicación, seleccione `F5` .  Ahora tiene una ventana WebView que muestra la página de Bing.  

:::image type="complex" source="../media/bing-window.png" alt-text="Ventana de Bing" lightbox="../media/bing-window.png":::
   Ventana de Bing  
:::image-end:::  

## Paso 4: Eventos de navegación  

El equipo de WebView ya ha cubierto la navegación a la dirección URL mediante `ICoreWebView2::Navigate` el método en el último paso.  Durante la navegación, WebView dispara una secuencia de eventos a los que el host puede escuchar.  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

Para obtener más información, vaya a [Eventos de navegación.][Webview2ConceptsNavigationEvents]  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación" lightbox="../media/navigation-events.png":::
   Eventos de navegación  
:::image-end:::  

En los casos de error, uno o varios de los siguientes eventos pueden producirse en función de si la navegación continúa hacia una página web de error.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

> [!NOTE]
> Si se produce un redireccionamiento HTTP, hay varios `NavigationStarting` eventos en una fila.  

Como ejemplo de uso de los eventos, registre un controlador para el evento para cancelar las solicitudes `NavigationStarting` que no son https.  Copie el siguiente fragmento de código y péguelo en `HelloWebView.cpp` .  

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

Ahora, la aplicación no navega a ningún sitio que no sea https.  Puede usar un mecanismo similar para realizar otras tareas, como restringir la navegación a su propio dominio.  

## Paso 5: Scripting  

Puedes usar aplicaciones host para insertar código JavaScript en controles WebView2 en tiempo de ejecución.  Puede hacer que WebView ejecute JavaScript arbitrario o agregue scripts de inicialización.  El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a todos los fotogramas secundarios hasta que se quite el JavaScript.  El JavaScript inyectado se ejecuta con intervalos específicos.  

*   Ejecutarlo después de la creación del objeto global.  
*   Ejecutarlo antes de ejecutar cualquier otro script incluido en el documento HTML.  

Copie el siguiente fragmento de código y péguelo en `HelloWebView.cpp` .  

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

Ahora, WebView siempre debe inmovilizar el `Object` objeto y devuelve el documento de página una vez.  

> [!NOTE] 
> Las API de inserción de scripts \(y algunas otras API de WebView2\) son asincrónicas, debes usar devoluciones de llamada si el código debe ejecutarse en un orden específico.  

## Paso 6: Comunicación entre contenido de host y web  

El host y el contenido web también pueden comunicarse entre sí a través del `postMessage` método.  El contenido web que se ejecuta en una vista web puede publicarse en el host a través del método y el mensaje lo controla cualquier controlador de eventos registrado `window.chrome.webview.postMessage` `ICoreWebView2WebMessageReceivedEventHandler` en el host.  Del mismo modo, el host puede enviar mensajes al contenido web a través o al método, que son capturados por `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` controladores agregados desde el agente de `window.chrome.webview.addEventListener` escucha.  El mecanismo de comunicación permite que el contenido web use funcionalidades nativas pasando mensajes para pedir al host que ejecute API nativas.  

Como ejemplo para comprender el mecanismo, se producen los siguientes pasos al intentar generar la dirección URL del documento en WebView.  

1.  El host registra un controlador para devolver el mensaje recibido al contenido web  
1.  El host inserta un script en el contenido web que registra un controlador para imprimir el mensaje del host  
1.  El host inserta un script en el contenido web que publica la dirección URL en el host  
1.  El controlador del host se desencadena y devuelve el mensaje \(la dirección URL\) al contenido web  
1.  El controlador del contenido web se desencadena e imprime el mensaje desde el host \(la dirección URL\)  

Copie el siguiente fragmento de código y péguelo en `HelloWebView.cpp` .  

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

### Crear una aplicación de ejemplo de dirección URL para mostrar  

Para compilar y ejecutar la aplicación, seleccione `F5` .  La dirección URL aparece en una ventana emergente antes de navegar a una página web.  

:::image type="complex" source="../media/show-url.png" alt-text="Url para mostrar" lightbox="../media/show-url.png":::
   Url para mostrar  
:::image-end:::  

Enhorabuena, has creado tu primera aplicación WebView2.  

## Pasos siguientes  

Muchas de las funcionalidades de WebView2 no se tratan en este artículo, la siguiente sección proporciona más recursos.  

### Consulte también  

*   Para obtener un ejemplo completo de las funcionalidades de WebView2, vaya a la muestra [de API de WebView2.][GithubMicrosoftedgeWebview2samplesApisample]  
*   Para obtener una aplicación de ejemplo creada con WebView2, vaya a [WebView2Browser][GithubMicrosoftedgeWebview2browser].  
*   Para obtener información detallada sobre la API de WebView2, vaya a la [referencia de la API.][Webview2ReferenceWin32]  

## Introducción al equipo de Microsoft Edge WebView  

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

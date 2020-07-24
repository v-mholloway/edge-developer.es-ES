---
description: Hospedar contenido web en la aplicación Win32 con el control de WebView 2 de Microsoft Edge
title: Introducción a WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/07/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 7e35dc6ab84a32cfa7e020fa34ddfaa63818eda1
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895521"
---
# Introducción a WebView2 (vista previa para desarrolladores)  

El siguiente contenido le muestra las funciones más comunes de [WebView2 (Developer Preview)][Webview2Index] y proporciona un punto de partida para crear su primera aplicación de WebView2.  Para obtener más información sobre las API de WebView2 individuales, consulta referencia de la [API][Webview2ReferenceWin3209538].  

## Requisitos previos  

*   [Microsoft Edge (cromo)][MicrosoftedgeinsiderDownload] instalado en el SO compatible \ (actualmente Windows 10, Windows 8,1 y Windows 7 \).  
    
    > [!NOTE]
    > El equipo de WebView recomienda usar el canal Canarias y la versión mínima requerida es 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2015 o posterior con compatibilidad con C++ instalado.  

## Paso 1: crear una sola aplicación Win32 de ventana  

Empiece con un proyecto de escritorio básico que contenga una única ventana principal.  Para centrar mejor el tutorial, está usando código de ejemplo modificado de [Tutorial: crear una aplicación de escritorio de Windows tradicional (C++)][CppWindowsWalkthroughCreatingDesktopApplication] para la aplicación de ejemplo.  Para descargar el ejemplo modificado y empezar, consulta [ejemplos de WebView2][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].  

En Visual Studio, Abra `WebView2GettingStarted.sln` .  Si está usando una versión anterior de Visual Studio, mantenga el puntero sobre el proyecto **WebView2GettingStarted** , abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **propiedades**.  En **propiedades de configuración**  >  **General**, modifique la **versión del SDK de Windows** y el conjunto de herramientas de **plataforma** para usar el SDK de Win10 y el conjunto de herramientas de Visual Studio \ (vs Toolset \) que tiene a su disposición.  

:::image type="complex" source="../media/tool-version.png" alt-text="Versión de la herramienta":::
   Versión de la herramienta  
:::image-end:::  

Visual Studio puede mostrar algunos errores porque falta el archivo de encabezado WebView2, que debería desaparecer después de completar el paso 2.  

## Paso 2: instalar el SDK de WebView2  

Agregue el SDK de WebView2 al proyecto.  Para la versión preliminar de desarrollador, puedes instalar el SDK de Win32 con Nuget.  

1.  Mantenga el puntero sobre el proyecto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **administrar paquetes Nuget**.  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Administrar paquetes Nuget":::
       Administrar paquetes Nuget  
    :::image-end:::  
    
1.  Instale la biblioteca de implementación de Windows.  
    1.  Escriba `Microsoft.Windows.ImplementationLibrary` en la barra de búsqueda, seleccione **Microsoft. Windows. ImplementationLibrary** de los resultados y seleccione **instalar** en la ventana de la derecha.  Nuget descarga el SDK en tu equipo.  
        
        > [!NOTE] 
        > La biblioteca de [implementación de Windows][GithubMicrosoftWilMain] y la biblioteca de plantillas de [C++ de Windows Runtime][CppCxWrlTemplateLibraryVS2019] son opcionales y se han agregado para facilitar el trabajo con com.  
        
        :::image type="complex" source="../media/wil.png" alt-text="Biblioteca de implementación de Windows":::
           Biblioteca de implementación de Windows  
        :::image-end:::  
        
1.  Instale el SDK de WebView2.  
    1.  Escriba `Microsoft.Web.WebView2` en la barra de búsqueda, seleccione **Microsoft. Web. WebView2** de los resultados y seleccione **instalar** en la ventana de la derecha.  Nuget descarga el SDK en tu equipo.  
        
        :::image type="complex" source="../media/nuget.png" alt-text="Nuget":::
           Nuget
        :::image-end:::  
        
1.  Agregue el encabezado WebView2 al proyecto.  
    :::row:::
       :::column span="1":::
          Abra `HelloWebView.cpp` , copie el siguiente fragmento de código y péguelo `HelloWebView.cpp` después de la última `#include` línea.  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          La sección de inclusión debe tener un aspecto similar al siguiente fragmento de código.  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
Estás listo para usar y compilar en la API de WebView2.  

### Crear la aplicación de ejemplo vacía  

Pulse `F5` para compilar y ejecutar la aplicación de ejemplo.  Debería ver una aplicación que muestra una ventana vacía.  

:::image type="complex" source="../media/empty-app.png" alt-text="Aplicación vacía":::
   Aplicación vacía  
:::image-end:::  

## Paso 3: crear un único WebView en la ventana principal  

Agregue una vista previa a la ventana principal.  Use el `CreateCoreWebView2Environment` método para configurar el entorno y busque el explorador Microsoft Edge \ (cromo \) encendido del control.  También puede usar el `CreateCoreWebView2EnvironmentWithOptions` método si desea especificar la ubicación del explorador, la carpeta de usuario, las marcas del explorador, etc., en lugar de usar la configuración predeterminada.  Una vez finalizado el `CreateCoreWebView2Environment` método, podrá ejecutar el `ICoreWebView2Environment::CreateCoreWebView2Controller` método dentro de la devolución de `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` llamada y ejecutar el `ICoreWebView2Controller::get_CoreWebView2` método para obtener la vista previa asociada.  

En la devolución de llamada, establezca algunas opciones de configuración adicionales, cambie el tamaño de la vista de sitio para que tome el 100% de la ventana primaria y vaya a Bing.  

Copie el siguiente fragmento de código y péguelo `HelloWebView.cpp` después de la `// <-- WebView2 sample code starts here -->` Nota y antes de la `// <-- WebView2 sample code ends here -->` Nota.  

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


### Crear la aplicación de ejemplo de Bing  

Pulse `F5` para compilar y ejecutar la aplicación.  Ahora tiene una ventana de vista Web que muestra la página de Bing.  

:::image type="complex" source="../media/bing-window.png" alt-text="Ventana de Bing":::
   Ventana de Bing  
:::image-end:::  

## Paso 4: eventos de navegación  

El equipo de WebView ya cubre la navegación a la dirección URL con el `ICoreWebView2::Navigate` método del último paso.  Durante la navegación, WebView desencadena una secuencia de eventos a los que puede escuchar el host.  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

Para obtener más información, vea [eventos de navegación][Webview2ConceptsNavigationEvents].  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación":::
   Eventos de navegación  
:::image-end:::  

En casos de error, pueden producirse uno o varios de los siguientes eventos dependiendo de si la navegación continúa en una página de error.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

En el caso de una redirección HTTP, hay varios `NavigationStarting` eventos en una fila.  

Como ejemplo de uso de los eventos, registra un controlador para el `NavigationStarting` evento y cancela las solicitudes que no sean https.  Copie el siguiente fragmento de código y péguelo en él `HelloWebView.cpp` .  

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

Ahora la aplicación no está navegando a ningún sitio que no sea HTTPS.  Puede usar un mecanismo similar para realizar otras tareas, como restringir la navegación a dentro de su propio dominio.  

## Paso 5: scripting  

La aplicación de hospedaje también puede inyectar JavaScript en WebView.  Puede usar la vista previa de tareas para ejecutar JavaScript arbitrario o agregar scripts de inicialización.  Los scripts de inicialización agregados se aplican a todos los futuros documentos de nivel superior y navegación de Marcos secundarios hasta que se eliminan y se ejecutan después de que se haya creado el objeto global y antes de que se ejecute cualquier otro script incluido en el documento HTML.  

Copie el siguiente fragmento de código y péguelo en él `HelloWebView.cpp` .  

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

Ahora WebView debería inmovilizar siempre el `Object` objeto y devuelve el documento de página una vez.  

> [!NOTE] 
> Las API de inyección de script \ (y otras API de WebView2 \) son asincrónicas, por lo que debe usar devoluciones de llamada si el código debe ejecutarse en un orden específico.  

## Paso 6: comunicación entre el host y el contenido web  

El host y el contenido web también pueden comunicarse con ellos a través del `postMessage` método.  El contenido web que se ejecuta en una vista Web puede publicarse en el host mediante el `window.chrome.webview.postMessage` método y cualquier otro registro del `ICoreWebView2WebMessageReceivedEventHandler` controlador de eventos registrado en el host controla el mensaje.  Del mismo modo, el anfitrión puede enviar un mensaje a través de la web mediante `ICoreWebView2::PostWebMessageAsString` o `ICoreWebView2::PostWebMessageAsJSON` método, que los controladores han agregado desde la `window.chrome.webview.addEventListener` escucha.  El mecanismo de comunicación permite que el contenido web use capacidades nativas al pasar mensajes para solicitar al host que llame a las API nativas.  

Como ejemplo para comprender el mecanismo, los pasos siguientes se producen al intentar imprimir la dirección URL del documento en WebView.  

1.  El anfitrión registra un controlador para devolver el mensaje recibido al contenido web  
1.  El anfitrión inyecta un script en el contenido web que registra un controlador para imprimir el mensaje desde el host  
1.  El anfitrión inyecta un script en el contenido web que publica la dirección URL en el host.  
1.  El controlador del host se desencadena y devuelve el mensaje \ (la dirección URL \) en el contenido Web.  
1.  El controlador del contenido web se desencadena e imprime un mensaje desde el host \ (la dirección URL \)  

Copie el siguiente fragmento de código y péguelo en él `HelloWebView.cpp` .    

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

### Crear la aplicación Mostrar URL de muestra  

Pulse `F5` para compilar y ejecutar la aplicación.  Debería ver la dirección URL en una ventana emergente antes de navegar a una página.  

:::image type="complex" source="../media/show-url.png" alt-text="Mostrar URL":::
   Mostrar URL  
:::image-end:::  

¡ Enhorabuena! ¡ acabas de crear tu primera WebView2 aplicación!  

## Pasos siguientes  

Muchas de las funcionalidades de WebView2 que no se cubren en esta página, la siguiente sección proporcionaba recursos adicionales.  

### Consulte también  

*   Para obtener un ejemplo completo de las capacidades de WebView2, consulta la [muestra de API de WebView2][GithubMicrosoftedgeWebview2samplesApisample].  
*   Para obtener una aplicación de muestra creada con WebView2, consulte [WebView2Browser][GithubMicrosoftedgeWebview2browser].  
*   Para obtener información detallada sobre la API de WebView2, consulta referencia de la [API][Webview2ReferenceWin3209538].  

## Ponerse en contacto con el equipo de WebView2  

Ayuda a crear una experiencia WebView2 más rica compartiendo tus comentarios.  Visite el [repositorio de comentarios][GithubMicrosoftedgeWebviewfeedback] de github para enviar solicitudes de características o informes de errores o buscar problemas conocidos.  

<!-- links -->  

[Webview2Index]: ../index.md "Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegación | Microsoft docs"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019 "Biblioteca de plantillas C++ de Windows en tiempo de ejecución (WRL) | Microsoft docs"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019 "Tutorial: crear una aplicación de escritorio de Windows tradicional (C++) | Microsoft docs"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser-MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample "Ejemplo de API de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Bibliotecas de implementación de Windows (superservicio)-Microsoft/| GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar los canales de Insider de Microsoft Edge"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

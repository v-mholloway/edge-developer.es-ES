---
description: Hospedar contenido web en la aplicación Win32 con el control de WebView 2 de Microsoft Edge
title: Vista previa de Microsoft Edge 2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 460364b0c93e80c0e3868c3b69e20ea9dcf6c129
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697199"
---
# Introducción a WebView2 (vista previa para desarrolladores)

Este tutorial pasa por las funcionalidades más usadas de [WebView2 (Developer Preview)](https://aka.ms/webview) y comienza a crear tu primera aplicación de WebView2. Visita la referencia de la [API](../reference/win32/0-9-538-reference-webview2.md) para obtener más información sobre las API individuales.  

## Requisitos previos

* [Microsoft Edge (cromo)](https://www.microsoftedgeinsider.com/download/) instalado en el sistema operativo compatible (actualmente Windows 10, Windows 8,1 y Windows 7). **Se recomienda usar el canal Canarias y la versión mínima requerida es 82.0.488.0**.
* [Visual Studio](https://visualstudio.microsoft.com/) 2015 o posterior con compatibilidad con C++ instalado.

## Paso 1: crear una sola aplicación Win32 de ventana

Comenzaremos con un proyecto de escritorio básico que contenga una sola ventana principal. Como este no es el principal enfoque de este tutorial, simplemente usaremos código de ejemplo modificado de [Tutorial: crear una aplicación de escritorio de Windows tradicional (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019). [Descarga](https://aka.ms/HelloWebView) la muestra modificada para comenzar.

Abra **WebView2GettingStarted. sln** en Visual Studio. Si está usando una versión anterior de Visual Studio, haga clic con el botón secundario del mouse en el proyecto **WebView2GettingStarted** y haga clic en **propiedades**. En **propiedades de configuración**  >  **General**, modifique la **versión del SDK de Windows** y el conjunto de herramientas de **plataforma** para usar el SDK de Win10 y el conjunto de herramientas de vs disponibles.

![versión de herramienta](../media/tool-version.png)

Visual Studio puede mostrar algunos errores porque falta el archivo de encabezado WebView2, que debería desaparecer una vez completado el paso 2.

## Paso 2: instalar el SDK de WebView2

Ahora vamos a agregar el SDK de WebView2 al proyecto. Para la versión preliminar de desarrollador, puedes instalar el SDK de Win32 a través de Nuget.

1. Haga clic con el botón derecho en el proyecto y haga clic en **administrar paquetes Nuget**.

    ![Administración de Nuget: paquetes](../media/manage-nuget-packages.png)

2. Escriba **Microsoft. Windows. ImplementationLibrary** en la barra de búsqueda, haga clic en **Microsoft. Windows. ImplementationLibrary** de los resultados y haga clic en **instalar** en la ventana del lado derecho e instale el SDK más reciente. Nuget descargará el SDK en su equipo. Aunque usamos la [biblioteca de implementación de Windows](https://github.com/Microsoft/wil) y la [biblioteca de plantillas de C++ de Windows Runtime](/cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019) para facilitar el trabajo con com en este tutorial, son totalmente opcionales.

    ![queda](../media/wil.png)

3. Escriba **Microsoft. Web. WebView2** en la barra de búsqueda, haga clic en **Microsoft. Web. WebView2** de los resultados y haga clic en **instalar** en la ventana del lado derecho e instale el SDK más reciente. Nuget descargará el SDK en su equipo.

    ![Nuget](../media/nuget.png)

4. Incluya el encabezado WebView2. En **HelloWebView. cpp**, agregue `#include "WebView2.h"` debajo de las líneas de `#include` s.

    ```cpp
    ...
    #include <wrl.h>
    #include <wil/com.h>
    // include WebView2 header
    #include "WebView2.h"
    ```

Estás listo para usar y compilar en la API de WebView2. Presione F5 para compilar y ejecutar la aplicación de ejemplo. Debería ver una aplicación que muestra una ventana vacía.

![vaciar aplicación](../media/empty-app.png)

## Paso 3: crear un único WebView en la ventana principal

Ahora vamos a agregar una vista previa a la ventana principal. Usaremos `CreateCoreWebView2Environment` para configurar el entorno y encontrar el explorador Microsoft Edge (cromo) que encienden el control. También puede usar `CreateCoreWebView2EnvironmentWithOptions` si desea especificar la ubicación del explorador, la carpeta de usuario, las marcas del explorador, etc., en lugar de usar la configuración predeterminada. Una vez finalizado `CreateCoreWebView2Environment` , podrás llamar en `ICoreWebView2Environment::CreateCoreWebView2Controller` la devolución de llamada `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` y llamar `ICoreWebView2Controller::get_CoreWebView2` para obtener la vista previa asociada.

En la devolución de llamada, vamos a establecer unos cuantos ajustes, cambiar el tamaño de la vista en WebView para que tome el 100% de la ventana primaria y navegar a Bing.

Copie el siguiente código en **HelloWebView. cpp** entre `// <-- WebView2 sample code starts here -->` y `// <-- WebView2 sample code ends here -->` .

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
                // this is a redundant demo step as they are the default settings values
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

Presiona F5 para compilar y ejecutar la aplicación. Ahora tiene una ventana WebView que muestra Bing.

![ventana de Bing](../media/bing-window.png)

## Paso 4: eventos de navegación

Ya hemos cubierto la navegación por la dirección URL `ICoreWebView2::Navigate` en el último paso. Durante la navegación, WebView desencadena una secuencia de eventos en los que el host puede escuchar,,, `NavigationStarting` `SourceChanged` y, `ContentLoading` `HistoryChanged` a continuación, `NavigationCompleted` . Haz clic [aquí](../reference/win32/0-9-538/ICoreWebView2.md#navigation-events) para obtener más información.

![navegación-eventos](../media/navigation-events.png)

En casos de error pueden o no ser `SourceChanged` , `ContentLoading` o `HistoryChanged` eventos dependiendo de si la navegación continúa o no en una página de error. En el caso de una redirección HTTP, habrá varios `NavigationStarting` eventos en una fila.

Como ejemplo de uso de esos eventos, vamos a registrar un controlador para `NavigationStarting` Cancelar solicitudes que no sean https. Copie el código siguiente a **HelloWebView. cpp** a continuación `// Step 4 - Navigation events` .

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

Ahora la aplicación no se desplazará a ningún sitio que no sea HTTPS. Puede usar un mecanismo similar para realizar otras tareas, como restringir la navegación a dentro de su propio dominio.

## Paso 5: scripting

La aplicación de hospedaje también puede inyectar JavaScript en WebView. Puede realizar tareas en la vista previa de las tareas para ejecutar JavaScript arbitrario o agregar scripts de inicialización. Los scripts de inicialización agregados se aplican a todos los futuros documentos de nivel superior y navegación de Marcos secundarios hasta que se eliminan y se ejecutan después de que se haya creado el objeto global y antes de que se ejecute cualquier otro script incluido en el documento HTML.

Copie el siguiente código a continuación `// Step 5 - Scripting` .

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

Ahora WebView inmovilizará el objeto Object y devolverá el documento de página una vez.

**Tenga en cuenta que estas API de inyección de script (y otras API de WebView2) son asincrónicas, por lo que debe usar devoluciones de llamada si el código se va a ejecutar en un orden determinado.**

## Paso 6: comunicación entre el host y el contenido web

El host y el contenido web también pueden comunicarse con ellos `postMessage` . El contenido web que se ejecuta dentro de WebView puede publicar mensajes en el host mediante `window.chrome.webview.postMessage` , y el mensaje sería controlado por cualquier registro `ICoreWebView2WebMessageReceivedEventHandler` en el host. Del mismo modo, el anfitrión puede enviar mensajes a través de la web a través de `ICoreWebView2::PostWebMessageAsString` o `ICoreWebView2::PostWebMessageAsJSON` , que los controladores agregados hayan detectado `window.chrome.webview.addEventListener` . El mecanismo de comunicación permite que el contenido web use capacidades nativas al pasar mensajes para solicitar al host que llame a las API nativas.

Como ejemplo para comprender el mecanismo, vamos a intentar imprimir la dirección URL del documento en WebView con un poco de recorrido,

1. el anfitrión registra un controlador para devolver el mensaje recibido al contenido web
2. el anfitrión inyecta un script en el contenido web que registra un controlador para imprimir el mensaje desde el host
3. el anfitrión inyecta un script en el contenido web que publica la dirección URL en el host.
4. el controlador del host se desencadena y devuelve el mensaje (la dirección URL) al contenido Web.
5. se desencadena el controlador del contenido web e imprime el mensaje del host (la dirección URL).

Copia el siguiente código `// Step 6 - Communication between host and web content` ,

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

Presiona F5 para compilar y ejecutar la aplicación. Ahora mostrará las direcciones URL antes de navegar hasta las páginas.

![Show-URL](../media/show-url.png)

¡ Felicidades! acabas de crear tu primera WebView2 aplicación!

## Pasos siguientes

Existen numerosas funcionalidades de WebView2 que no se cubren en este tutorial.

Para obtener más información:

* Retirada de la [API de WebView2](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) para obtener un ejemplo completo de las capacidades de WebView2's.
* Checkout [WebView2Browser](https://github.com/MicrosoftEdge/WebView2Browser) una aplicación creada con WebView2.
* Para obtener información detallada sobre nuestra API, [consulta la referencia](../reference/win32/0-9-538-reference-webview2.md) de la API.  

## Ponerse en contacto con el equipo de WebView2  

Ayúdanos a crear una experiencia WebView2 más rica compartiendo tus comentarios. Visita nuestro [repositorio de comentarios](https://aka.ms/webviewfeedback) para enviar solicitudes de características o informes de errores o buscar problemas conocidos.

---
description: Convenciones de la API de Win32 C++ WebView2
title: Convenciones de la API de Win32 C++ WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, controlador de explorador, edge html
ms.openlocfilehash: b47e53a4846d4bb662ae108c6445a6c2a615722a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470861"
---
# <a name="win32-c-webview2-api-conventions"></a>Convenciones de la API de WebView2 de Win32 C++  

:::row:::
   :::column span="1":::
      Plataformas compatibles:
   :::column-end:::
   :::column span="2":::
      Win32
   :::column-end:::
:::row-end:::  

## <a name="prerequisites"></a>Requisitos previos  

*   Experiencia con la API de Win32  

## <a name="async-methods"></a>Métodos asincrónicos  

Los métodos asincrónicos de la API de WebView2 Win32 C++ usan una interfaz delegada para ponerse en contacto con usted por los siguientes motivos.  

*   Se ha completado el método asincrónico.  
*   El código correcto o de error.  
*   El resultado del método asincrónico.  

El parámetro final de todos los métodos asincrónicos es un puntero a una interfaz de delegado de la que se proporciona una implementación.  

La interfaz de delegado tiene un único método que toma como primer `Invoke` parámetro una del código correcto o de `HRESULT` error.  Además, puede haber un segundo parámetro que sea el resultado del método si el método tiene un resultado.  Por ejemplo, el [método ICoreWebView2::CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] toma como parámetro final un `ICoreWebView2CapturePreviewCompletedHandler` puntero.  Para enviar una `CapturePreview` solicitud de método, proporcione una instancia del `ICoreWebView2CapturePreviewCompletedHandler` puntero que implemente.  El siguiente fragmento de código usa un método para implementar.  

```cpp
HRESULT Invoke(HRESULT result)
```  

El método se implementa `Invoke` y se solicita al método cuando se completa la `CoreWebView2` `Invoke` `CapturePreview` solicitud.  El parámetro único es la descripción del código correcto o `HRESULT` de error de la `CapturePreview` solicitud.  

Como alternativa, para , proporciona una instancia que tiene un método que le proporciona el código de éxito o `ICoreWebView2::ExecuteScript` `Invoke` error de la `ExecuteScript` solicitud.  También proporcione el segundo parámetro que es el JSON del resultado de ejecutar el script.  

Puede implementar manualmente las interfaces de delegado o puede `CompleteHandler` usar la función [Callback (WRL).][CppCxWrlCallbackFunction]  La [función Callback (WRL)][CppCxWrlCallbackFunction] se usa en el siguiente fragmento de código de WebView2.  

```cpp
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```  

## <a name="events"></a>Eventos  

Los eventos de la API de WebView2 Win32 C++ usan el par `add_EventName` de métodos and para suscribirse y cancelar la suscripción a `remove_EventName` eventos.  El `add_EventName` método toma una interfaz de delegado del controlador de eventos y devuelve un token como parámetro de `EventRegistrationToken` salida.  El `remove_EventName` método toma un token y cancela la suscripción de evento `EventRegistrationToken` correspondiente.  

Las interfaces de delegado del controlador de eventos funcionan de forma similar a las interfaces de delegado del controlador completadas con el método asincrónico.  Se implementa la interfaz de delegado del controlador de eventos y `CoreWebView2` se envía una devolución de llamada cada vez que se ejecuta el evento.  Cada interfaz de delegado del controlador de eventos tiene un único `Invoke` método que tiene un parámetro sender seguido de un parámetro event args.  El remitente es la instancia del objeto en el que se suscribió para eventos.  El parámetro event args es una interfaz que contiene información sobre el evento de activación actual.  

Por ejemplo, el `NavigationCompleted` evento on tiene el par de `ICoreWebView2` `ICoreWebView2::add_NavigationCompleted` `ICoreWebView2::remove_NavigationCompleted` métodos and.  Al enviar una solicitud, se proporciona una instancia de la que ya `ICoreWebView2NavigationCompletedEventHandler` implementó el `Invoke` método.  Cuando se `NavigationCompleted` ejecuta el evento, se `Invoke` solicita el método.  El primer parámetro ejecuta el `NavigationCompleted` evento.  El segundo parámetro contiene información sobre si la navegación se completó correctamente y así sucesivamente.  

De forma similar a la interfaz de delegado del controlador completado del método asincrónico, use una de las siguientes acciones para configurarla.  

*   Implemente directamente.  
*   Use la [función de devolución de llamada (WRL)][CppCxWrlCallbackFunction] que se usa en el siguiente fragmento de código de WebView2.  

<!-- todo:  what is async method completed handler delegate interface?  Is there a shorter name for it?  -->  

```cpp
// Register a handler for the NavigationCompleted event.
// Check whether the navigation succeeded, and if not, do something.
// Also update the Cancel buttons.
CHECK_FAILURE(m_webView->add_NavigationCompleted(
    Callback<ICoreWebView2NavigationCompletedEventHandler>(
        [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
            -> HRESULT {
            BOOL success;
            CHECK_FAILURE(args->get_IsSuccess(&success));
            if (!success)
            {
                COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                {
                    // Do something here if you want to handle a specific error case.
                    // In most cases it is not necessary, because the WebView
                    // displays an error page automatically.
                }
            }
            m_toolbar->SetItemEnabled(Toolbar::Item_CancelButton, false);
            m_toolbar->SetItemEnabled(Toolbar::Item_ReloadButton, true);
            return S_OK;
        })
        .Get(),
    &m_navigationCompletedToken));
```  

## <a name="strings"></a>Cadenas  

Los parámetros de salida de cadena `LPWSTR` son cadenas terminadas en null.  El solicitante proporciona la cadena mediante `CoTaskMemAlloc` .  La propiedad se transfiere al solicitante y el solicitante debe liberar la memoria mediante `CoTaskMemFree` .  

Los parámetros de entrada de cadena `LPCWSTR` son cadenas terminadas en null.  El solicitante garantiza que la cadena es válida durante la duración de la solicitud de función sincrónica.  Si el receptor debe almacenar el valor en algún momento después de que se complete la solicitud de función, el receptor debe proporcionar una copia asociada del valor de cadena.  

## <a name="uri-and-json-parsing"></a>Análisis DE URI y JSON  

Varios métodos proporcionan o aceptan URI y JSON como cadenas.  Use la biblioteca preferida para analizar y generar las cadenas.  

Si WinRT está disponible para la aplicación, puedes usar los métodos and para analizar o producir cadenas JSON o para analizar y `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` producir `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` URI.  Ambos métodos funcionan en aplicaciones de Win32.  

Si usa y analiza uri, puede usar las siguientes marcas de creación de URI para que el comportamiento coincida más estrechamente con el análisis de URI en `IUri` `CreateUri` `CreateUri` WebView.  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

## <a name="see-also"></a>Consulte también  

*   Para empezar a usar WebView2 Win32 C/C++, vaya a [Introducción a WebView2][Webview2IndexGettingStarted].  
*   Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][DotnetApiMicrosoftWebWebview2WpfWebview2].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Getting in touch with the Microsoft Edge WebView team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2GettingstartedWin32]: ../gettingstarted/win32.md "Introducción a WebView2 | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2CapturePreview]: /microsoft-edge/webview2/reference/win32/icorewebview2#capturepreview "CapturePreview: interfaz ICoreWebView2 | Microsoft Docs"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Función de devolución de llamada (WRL) | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Clase WebView2 | Microsoft Docs"  

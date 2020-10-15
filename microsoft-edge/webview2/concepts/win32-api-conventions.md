---
description: Convenciones de la API de C++ de WebView2 Win32
title: Convenciones de la API de C++ de WebView2 Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 42f0b5c9970b2e4a6424eb70458c58a98ec8dbc7
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/15/2020
ms.locfileid: "11118978"
---
# Convenciones de la API de C++ de WebView2 Win32  

## Métodos asincrónicos  

Métodos asincrónicos en la API C++ de WebView2 Win32 use una interfaz de delegado para devoluciones de llamada para indicar cuándo se ha completado el método asincrónico, el código de éxito o el error, y para algunos, el resultado del método asincrónico.  El último parámetro de todos los métodos asincrónicos es un puntero a una interfaz de delegado de la que se proporciona una implementación.  

La interfaz Delegate tiene un único `Invoke` método que toma como primer parámetro un `HRESULT` código de éxito o error.  Además, es posible que haya un segundo parámetro que sea el resultado del método si el método tiene un resultado.  Por ejemplo, el método [ICoreWebView2:: CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] toma como parámetro final un `ICoreWebView2CapturePreviewCompletedHandler` puntero.  Para enviar una `CapturePreview` solicitud de método, se proporciona una instancia del `ICoreWebView2CapturePreviewCompletedHandler` puntero que se implementa.  El siguiente fragmento de código usa un método para implementar.  

```cpp
HRESULT Invoke(HRESULT result)
```  

Implemente el `Invoke` método y `CoreWebView2` solicite el `Invoke` método cuando se `CapturePreview` complete la solicitud.  El único parámetro es el que `HRESULT` describe el código de éxito o error de la `CapturePreview` solicitud.  

O para `ICoreWebView2::ExecuteScript` , usted proporciona una instancia de `ICoreWebView2ExecuteScriptCompletedHandler` que tiene un `Invoke` método que le proporciona el código de éxito o error de la `ExecuteScript` solicitud, así como el segundo parámetro, `resultObjectAsJson` que es la JSON del resultado de ejecutar el script.  

Puede implementar manualmente las `CompleteHandler` interfaces delegados o puede usar la [función de devolución de llamada WRL][CppCxWrlCallbackFunction].  La función de devolución de llamada se usa en el siguiente fragmento de código WebView2.  

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

## Eventos  

Los eventos de la API de C++ de WebView2 usan el `add_EventName` `remove_EventName` par de métodos and para suscribirse y anular la suscripción de eventos.  El `add_EventName` método toma una interfaz de delegado de controlador de eventos y devuelve un `EventRegistrationToken` como parámetro de salida.  El `remove_EventName` método toma una `EventRegistrationToken` y cancela la suscripción de la suscripción a eventos correspondiente.  

Las interfaces de delegación de controlador de eventos funcionan muy de forma similar al método Async interfaces delegadas de controlador completas.  Implementa la interfaz de delegación del controlador de eventos y `CoreWebView2` envía una devolución de llamada siempre que se desencadena el evento.  Cada interfaz delegada del controlador de eventos tiene un `Invoke` método único que tiene un parámetro Sender seguido de un parámetro de argumentos de evento.  El remitente es la instancia del objeto en el que suscribiste eventos.  El parámetro de argumentos de evento es una interfaz que contiene información sobre el evento que se está desencadenando en ese momento.  

Por ejemplo `NavigationCompleted` , el evento on `ICoreWebView2` tiene `ICoreWebView2::add_NavigationCompleted` el `ICoreWebView2::remove_NavigationCompleted` par y método.  Al solicitar agregar, se proporciona una instancia de `ICoreWebView2NavigationCompletedEventHandler` en la que ha implementado previamente un `Invoke` método.  Cuando `NavigationCompleted` se activa el evento, `Invoke` se solicita el método.  El primer parámetro es el `ICoreWebView2` que está desencadenando el `NavigationCompleted` evento.  El segundo parámetro es el `ICoreWebView2NavigationCompletedEventArgs` que contiene información sobre si la navegación se completó correctamente y así sucesivamente.  

Del mismo modo que el método asincrónico completó la interfaz de delegado de controlador, puedes implementarla directamente o puedes usar la función de devolución de llamada WRL que se usa en el siguiente fragmento de código WebView2.  

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

## Cadena  

Los parámetros de salida `LPWSTR` de cadenas son cadenas terminadas en NULL.  El solicitante asigna la cadena usando `CoTaskMemAlloc` .  La propiedad se transfiere al solicitante y el solicitante debe liberarla con la memoria `CoTaskMemFree` .  

La cadena de parámetros son `LPCWSTR` cadenas terminadas en NULL.  El solicitante garantiza que la cadena es válida durante la solicitud de la función sincrónica.  Si el receptor debe conservar ese valor en algún punto después de que finalice la solicitud de función, el receptor debe asignar una copia asociada del valor de la cadena.  

## URI y análisis de JSON  

Varios métodos proporcionan o aceptan identificadores URI y JSON como cadenas.  Use su propia biblioteca preferida para analizar y generar las cadenas.  

Si WinRT está disponible para tu aplicación, puedes usar los `RuntimeClass_Windows_Data_Json_JsonObject` métodos y `IJsonObjectStatics` para analizar o producir cadenas JSON o `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` métodos para analizar y producir URI.  Ambos métodos funcionan en aplicaciones Win32.  

Si usas `IUri` y `CreateUri` para analizar los URI, es posible que desees usar los siguientes marcadores de creación de URI para que el `CreateUri` comportamiento coincida más estrechamente con el análisis de URI en la vista de usuario.  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

<!-- links -->  

[Webview2ReferenceWin32Icorewebview2CapturePreview]: /microsoft-edge/webview2/reference/win32/icorewebview2#capturepreview "CapturePreview: ICoreWebView2 | Microsoft docs"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Función callback (WRL) | Microsoft docs"  

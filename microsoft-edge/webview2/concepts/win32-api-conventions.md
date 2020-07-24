---
description: Convenciones de la API de C++ de WebView2 Win32
title: Convenciones de la API de C++ de WebView2 Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: c8792133da2b858cfaa456df5a7dce26c3c65154
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895594"
---
# <span data-ttu-id="7de04-104">Convenciones de la API de C++ de WebView2 Win32</span><span class="sxs-lookup"><span data-stu-id="7de04-104">Win32 C++ WebView2 API conventions</span></span>  

## <span data-ttu-id="7de04-105">Métodos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="7de04-105">Async Methods</span></span>  

<span data-ttu-id="7de04-106">Métodos asincrónicos en la API C++ de WebView2 Win32 use una interfaz de delegado para devoluciones de llamada para indicar cuándo se ha completado el método asincrónico, el código de éxito o el error, y para algunos, el resultado del método asincrónico.</span><span class="sxs-lookup"><span data-stu-id="7de04-106">Asynchronous methods in the WebView2 Win32 C++ API use a delegate interface to callback to you to indicate when the async method has completed, the success or failure code, and for some, the result of the asynchronous method.</span></span>  <span data-ttu-id="7de04-107">El último parámetro de todos los métodos asincrónicos es un puntero a una interfaz de delegado de la que se proporciona una implementación.</span><span class="sxs-lookup"><span data-stu-id="7de04-107">The final parameter for all asynchronous methods is a pointer to a delegate interface of which you provide an implementation.</span></span>  

<span data-ttu-id="7de04-108">La interfaz Delegate tiene un único `Invoke` método que toma como primer parámetro un `HRESULT` código de éxito o error.</span><span class="sxs-lookup"><span data-stu-id="7de04-108">The delegate interface has a single `Invoke` method that takes as a first parameter an `HRESULT` of the success or failure code.</span></span>  <span data-ttu-id="7de04-109">Además, es posible que haya un segundo parámetro que sea el resultado del método si el método tiene un resultado.</span><span class="sxs-lookup"><span data-stu-id="7de04-109">Additionally there may be a second parameter that is the result of the method if the method has a result.</span></span>  <span data-ttu-id="7de04-110">Por ejemplo, el método [ICoreWebView2:: CapturePreview][Webview2ReferenceWin3209538Icorewebview2CapturePreview] toma como parámetro final un `ICoreWebView2CapturePreviewCompletedHandler` puntero.</span><span class="sxs-lookup"><span data-stu-id="7de04-110">For example, the [ICoreWebView2::CapturePreview][Webview2ReferenceWin3209538Icorewebview2CapturePreview] method takes as the final parameter an `ICoreWebView2CapturePreviewCompletedHandler` pointer.</span></span>  <span data-ttu-id="7de04-111">Para enviar una `CapturePreview` solicitud de método, se proporciona una instancia del `ICoreWebView2CapturePreviewCompletedHandler` puntero que se implementa.</span><span class="sxs-lookup"><span data-stu-id="7de04-111">To send a `CapturePreview` method request, you provide an instance of the `ICoreWebView2CapturePreviewCompletedHandler` pointer that you implement.</span></span>  <span data-ttu-id="7de04-112">El siguiente fragmento de código usa un método para implementar.</span><span class="sxs-lookup"><span data-stu-id="7de04-112">The following code snippet uses one method to implement.</span></span>  

```cpp
HRESULT Invoke(HRESULT result)
```  

<span data-ttu-id="7de04-113">Implemente el `Invoke` método y `CoreWebView2` solicite el `Invoke` método cuando se `CapturePreview` complete la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7de04-113">You implement the `Invoke` method and `CoreWebView2` requests your `Invoke` method when `CapturePreview` request completes.</span></span>  <span data-ttu-id="7de04-114">El único parámetro es el que `HRESULT` describe el código de éxito o error de la `CapturePreview` solicitud.</span><span class="sxs-lookup"><span data-stu-id="7de04-114">The single parameter is the `HRESULT` describing the success or failure code of the `CapturePreview` request.</span></span>  

<span data-ttu-id="7de04-115">O para `ICoreWebView2::ExecuteScript` , usted proporciona una instancia de `ICoreWebView2ExecuteScriptCompletedHandler` que tiene un `Invoke` método que le proporciona el código de éxito o error de la `ExecuteScript` solicitud, así como el segundo parámetro, `resultObjectAsJson` que es la JSON del resultado de ejecutar el script.</span><span class="sxs-lookup"><span data-stu-id="7de04-115">Or for `ICoreWebView2::ExecuteScript`, you provide an instance of `ICoreWebView2ExecuteScriptCompletedHandler` which has an `Invoke` method that provides you with the success or failure code of the `ExecuteScript` request as well as the second parameter `resultObjectAsJson` which is the JSON of the result of running the script.</span></span>  

<span data-ttu-id="7de04-116">Puede implementar manualmente las `CompleteHandler` interfaces delegados o puede usar la [función de devolución de llamada WRL][CppCxWrlCallbackFunction].</span><span class="sxs-lookup"><span data-stu-id="7de04-116">You may manually implement the `CompleteHandler` delegate interfaces, or you may use the [WRL Callback function][CppCxWrlCallbackFunction].</span></span>  <span data-ttu-id="7de04-117">La función de devolución de llamada se usa en el siguiente fragmento de código WebView2.</span><span class="sxs-lookup"><span data-stu-id="7de04-117">The Callback function is used throughout the following WebView2 code snippet.</span></span>  

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

## <span data-ttu-id="7de04-118">Eventos</span><span class="sxs-lookup"><span data-stu-id="7de04-118">Events</span></span>  

<span data-ttu-id="7de04-119">Los eventos de la API de C++ de WebView2 usan el `add_EventName` `remove_EventName` par de métodos and para suscribirse y anular la suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="7de04-119">Events in the WebView2 Win32 C++ API use the `add_EventName` and `remove_EventName` method pair to subscribe and unsubscribe from events.</span></span>  <span data-ttu-id="7de04-120">El `add_EventName` método toma una interfaz de delegado de controlador de eventos y devuelve un `EventRegistrationToken` como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="7de04-120">The `add_EventName` method takes an event handler delegate interface and gives back an `EventRegistrationToken` as an out parameter.</span></span>  <span data-ttu-id="7de04-121">El `remove_EventName` método toma una `EventRegistrationToken` y cancela la suscripción de la suscripción a eventos correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7de04-121">The `remove_EventName` method takes an `EventRegistrationToken` and unsubscribes the corresponding event subscription.</span></span>  

<span data-ttu-id="7de04-122">Las interfaces de delegación de controlador de eventos funcionan muy de forma similar al método Async interfaces delegadas de controlador completas.</span><span class="sxs-lookup"><span data-stu-id="7de04-122">Event handler delegate interfaces work very similarly to the async method completed handler delegate interfaces.</span></span>  <span data-ttu-id="7de04-123">Implementa la interfaz de delegación del controlador de eventos y `CoreWebView2` envía una devolución de llamada siempre que se desencadena el evento.</span><span class="sxs-lookup"><span data-stu-id="7de04-123">You implement the event handler delegate interface and `CoreWebView2` sends a callback whenever the event fires.</span></span>  <span data-ttu-id="7de04-124">Cada interfaz delegada del controlador de eventos tiene un `Invoke` método único que tiene un parámetro Sender seguido de un parámetro de argumentos de evento.</span><span class="sxs-lookup"><span data-stu-id="7de04-124">Every event handler delegate interface has a single `Invoke` method that has a sender parameter followed by an event args parameter.</span></span>  <span data-ttu-id="7de04-125">El remitente es la instancia del objeto en el que suscribiste eventos.</span><span class="sxs-lookup"><span data-stu-id="7de04-125">The sender is the instance of the object on which you subscribed for events.</span></span>  <span data-ttu-id="7de04-126">El parámetro de argumentos de evento es una interfaz que contiene información sobre el evento que se está desencadenando en ese momento.</span><span class="sxs-lookup"><span data-stu-id="7de04-126">The event args parameter is an interface that contains information about the currently firing event.</span></span>  

<span data-ttu-id="7de04-127">Por ejemplo `NavigationCompleted` , el evento on `ICoreWebView2` tiene `ICoreWebView2::add_NavigationCompleted` el `ICoreWebView2::remove_NavigationCompleted` par y método.</span><span class="sxs-lookup"><span data-stu-id="7de04-127">For instance the `NavigationCompleted` event on `ICoreWebView2` has the `ICoreWebView2::add_NavigationCompleted` and `ICoreWebView2::remove_NavigationCompleted` method pair.</span></span>  <span data-ttu-id="7de04-128">Al solicitar agregar, se proporciona una instancia de `ICoreWebView2NavigationCompletedEventHandler` en la que ha implementado previamente un `Invoke` método.</span><span class="sxs-lookup"><span data-stu-id="7de04-128">When you request add you provide an instance of `ICoreWebView2NavigationCompletedEventHandler` in which you previously implemented `Invoke` method.</span></span>  <span data-ttu-id="7de04-129">Cuando `NavigationCompleted` se activa el evento, `Invoke` se solicita el método.</span><span class="sxs-lookup"><span data-stu-id="7de04-129">When the `NavigationCompleted` event fires, your `Invoke` method is requested.</span></span>  <span data-ttu-id="7de04-130">El primer parámetro es el `ICoreWebView2` que está desencadenando el `NavigationCompleted` evento.</span><span class="sxs-lookup"><span data-stu-id="7de04-130">The first parameter is the `ICoreWebView2` which is firing the `NavigationCompleted` event.</span></span>  <span data-ttu-id="7de04-131">El segundo parámetro es el `ICoreWebView2NavigationCompletedEventArgs` que contiene información sobre si la navegación se completó correctamente y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="7de04-131">The second parameter is the `ICoreWebView2NavigationCompletedEventArgs` which contains information about if the navigation completed successfully and so on.</span></span>  

<span data-ttu-id="7de04-132">Del mismo modo que el método asincrónico completó la interfaz de delegado de controlador, puedes implementarla directamente o puedes usar la función de devolución de llamada WRL que se usa en el siguiente fragmento de código WebView2.</span><span class="sxs-lookup"><span data-stu-id="7de04-132">Similarly to the async method completed handler delegate interface you are able to implement it yourself directly, or you may use the WRL Callback function that is used in the following WebView2 code snippet.</span></span>  

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

## <span data-ttu-id="7de04-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="7de04-133">Strings</span></span>  

<span data-ttu-id="7de04-134">Los parámetros de salida `LPWSTR` de cadenas son cadenas terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="7de04-134">String out parameters are `LPWSTR` null-terminated strings.</span></span>  <span data-ttu-id="7de04-135">El solicitante asigna la cadena usando `CoTaskMemAlloc` .</span><span class="sxs-lookup"><span data-stu-id="7de04-135">The requester allocates the string using `CoTaskMemAlloc`.</span></span>  <span data-ttu-id="7de04-136">La propiedad se transfiere al solicitante y el solicitante debe liberarla con la memoria `CoTaskMemFree` .</span><span class="sxs-lookup"><span data-stu-id="7de04-136">Ownership is transferred to the requester and it is up to the requester to free the memory using `CoTaskMemFree`.</span></span>  

<span data-ttu-id="7de04-137">La cadena de parámetros son `LPCWSTR` cadenas terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="7de04-137">String in parameters are `LPCWSTR` null-terminated strings.</span></span>  <span data-ttu-id="7de04-138">El solicitante garantiza que la cadena es válida durante la solicitud de la función sincrónica.</span><span class="sxs-lookup"><span data-stu-id="7de04-138">The requester ensures the string is valid for the duration of the synchronous function request.</span></span>  <span data-ttu-id="7de04-139">Si el receptor debe conservar ese valor en algún punto después de que finalice la solicitud de función, el receptor debe asignar una copia asociada del valor de la cadena.</span><span class="sxs-lookup"><span data-stu-id="7de04-139">If the receiver must retain that value to some point after the function request completes, the receiver must allocate an associated copy of the string value.</span></span>  

## <span data-ttu-id="7de04-140">URI y análisis de JSON</span><span class="sxs-lookup"><span data-stu-id="7de04-140">URI and JSON parsing</span></span>  

<span data-ttu-id="7de04-141">Varios métodos proporcionan o aceptan identificadores URI y JSON como cadenas.</span><span class="sxs-lookup"><span data-stu-id="7de04-141">Various methods provide or accept URIs and JSON as strings.</span></span>  <span data-ttu-id="7de04-142">Use su propia biblioteca preferida para analizar y generar las cadenas.</span><span class="sxs-lookup"><span data-stu-id="7de04-142">Please use your own preferred library for parsing and generating the strings.</span></span>  

<span data-ttu-id="7de04-143">Si WinRT está disponible para tu aplicación, puedes usar los `RuntimeClass_Windows_Data_Json_JsonObject` métodos y `IJsonObjectStatics` para analizar o producir cadenas JSON o `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` métodos para analizar y producir URI.</span><span class="sxs-lookup"><span data-stu-id="7de04-143">If WinRT is available for your app, you may use the `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` methods to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` methods to parse and produce URIs.</span></span>  <span data-ttu-id="7de04-144">Ambos métodos funcionan en aplicaciones Win32.</span><span class="sxs-lookup"><span data-stu-id="7de04-144">Both of methods work in Win32 apps.</span></span>  

<span data-ttu-id="7de04-145">Si usas `IUri` y `CreateUri` para analizar los URI, es posible que desees usar los siguientes marcadores de creación de URI para que el `CreateUri` comportamiento coincida más estrechamente con el análisis de URI en la vista de usuario.</span><span class="sxs-lookup"><span data-stu-id="7de04-145">If you use `IUri` and `CreateUri` to parse URIs, you may want to use the following URI creation flags to have `CreateUri` behavior more closely match the URI parsing in the WebView.</span></span>  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

<!-- links -->  

[Webview2ReferenceWin3209538Icorewebview2CapturePreview]: ../reference/win32/0-9-538/icorewebview2.md#capturepreview "CapturePreview: ICoreWebView2 | Microsoft docs"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Función callback (WRL) | Microsoft docs"  

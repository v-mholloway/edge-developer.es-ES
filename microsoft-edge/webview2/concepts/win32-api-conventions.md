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
# <a name="win32-c-webview2-api-conventions"></a><span data-ttu-id="16443-104">Convenciones de la API de WebView2 de Win32 C++</span><span class="sxs-lookup"><span data-stu-id="16443-104">Win32 C++ WebView2 API conventions</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="16443-105">Plataformas compatibles:</span><span class="sxs-lookup"><span data-stu-id="16443-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="16443-106">Win32</span><span class="sxs-lookup"><span data-stu-id="16443-106">Win32</span></span>
   :::column-end:::
:::row-end:::  

## <a name="prerequisites"></a><span data-ttu-id="16443-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="16443-107">Prerequisites</span></span>  

*   <span data-ttu-id="16443-108">Experiencia con la API de Win32</span><span class="sxs-lookup"><span data-stu-id="16443-108">Experience using Win32 API</span></span>  

## <a name="async-methods"></a><span data-ttu-id="16443-109">Métodos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="16443-109">Async methods</span></span>  

<span data-ttu-id="16443-110">Los métodos asincrónicos de la API de WebView2 Win32 C++ usan una interfaz delegada para ponerse en contacto con usted por los siguientes motivos.</span><span class="sxs-lookup"><span data-stu-id="16443-110">Asynchronous methods in the WebView2 Win32 C++ API use a delegate interface to contact you for the following reasons.</span></span>  

*   <span data-ttu-id="16443-111">Se ha completado el método asincrónico.</span><span class="sxs-lookup"><span data-stu-id="16443-111">The async method has completed.</span></span>  
*   <span data-ttu-id="16443-112">El código correcto o de error.</span><span class="sxs-lookup"><span data-stu-id="16443-112">The success or failure code.</span></span>  
*   <span data-ttu-id="16443-113">El resultado del método asincrónico.</span><span class="sxs-lookup"><span data-stu-id="16443-113">The result of the asynchronous method.</span></span>  

<span data-ttu-id="16443-114">El parámetro final de todos los métodos asincrónicos es un puntero a una interfaz de delegado de la que se proporciona una implementación.</span><span class="sxs-lookup"><span data-stu-id="16443-114">The final parameter for all asynchronous methods is a pointer to a delegate interface of which you provide an implementation.</span></span>  

<span data-ttu-id="16443-115">La interfaz de delegado tiene un único método que toma como primer `Invoke` parámetro una del código correcto o de `HRESULT` error.</span><span class="sxs-lookup"><span data-stu-id="16443-115">The delegate interface has a single `Invoke` method that takes as a first parameter an `HRESULT` of the success or failure code.</span></span>  <span data-ttu-id="16443-116">Además, puede haber un segundo parámetro que sea el resultado del método si el método tiene un resultado.</span><span class="sxs-lookup"><span data-stu-id="16443-116">Additionally, there may be a second parameter that is the result of the method if the method has a result.</span></span>  <span data-ttu-id="16443-117">Por ejemplo, el [método ICoreWebView2::CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] toma como parámetro final un `ICoreWebView2CapturePreviewCompletedHandler` puntero.</span><span class="sxs-lookup"><span data-stu-id="16443-117">For example, the [ICoreWebView2::CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] method takes as the final parameter an `ICoreWebView2CapturePreviewCompletedHandler` pointer.</span></span>  <span data-ttu-id="16443-118">Para enviar una `CapturePreview` solicitud de método, proporcione una instancia del `ICoreWebView2CapturePreviewCompletedHandler` puntero que implemente.</span><span class="sxs-lookup"><span data-stu-id="16443-118">To send a `CapturePreview` method request, you provide an instance of the `ICoreWebView2CapturePreviewCompletedHandler` pointer that you implement.</span></span>  <span data-ttu-id="16443-119">El siguiente fragmento de código usa un método para implementar.</span><span class="sxs-lookup"><span data-stu-id="16443-119">The following code snippet uses one method to implement.</span></span>  

```cpp
HRESULT Invoke(HRESULT result)
```  

<span data-ttu-id="16443-120">El método se implementa `Invoke` y se solicita al método cuando se completa la `CoreWebView2` `Invoke` `CapturePreview` solicitud.</span><span class="sxs-lookup"><span data-stu-id="16443-120">You implement the `Invoke` method and `CoreWebView2` requests your `Invoke` method when `CapturePreview` request completes.</span></span>  <span data-ttu-id="16443-121">El parámetro único es la descripción del código correcto o `HRESULT` de error de la `CapturePreview` solicitud.</span><span class="sxs-lookup"><span data-stu-id="16443-121">The single parameter is the `HRESULT` describing the success or failure code of the `CapturePreview` request.</span></span>  

<span data-ttu-id="16443-122">Como alternativa, para , proporciona una instancia que tiene un método que le proporciona el código de éxito o `ICoreWebView2::ExecuteScript` `Invoke` error de la `ExecuteScript` solicitud.</span><span class="sxs-lookup"><span data-stu-id="16443-122">Alternately, for `ICoreWebView2::ExecuteScript`, you provide an instance that has an `Invoke` method that provides you with the success or failure code of the `ExecuteScript` request.</span></span>  <span data-ttu-id="16443-123">También proporcione el segundo parámetro que es el JSON del resultado de ejecutar el script.</span><span class="sxs-lookup"><span data-stu-id="16443-123">Also provide the second parameter that is the JSON of the result of running the script.</span></span>  

<span data-ttu-id="16443-124">Puede implementar manualmente las interfaces de delegado o puede `CompleteHandler` usar la función [Callback (WRL).][CppCxWrlCallbackFunction]</span><span class="sxs-lookup"><span data-stu-id="16443-124">You may manually implement the `CompleteHandler` delegate interfaces, or you may use the [Callback function (WRL)][CppCxWrlCallbackFunction].</span></span>  <span data-ttu-id="16443-125">La [función Callback (WRL)][CppCxWrlCallbackFunction] se usa en el siguiente fragmento de código de WebView2.</span><span class="sxs-lookup"><span data-stu-id="16443-125">The [Callback function (WRL)][CppCxWrlCallbackFunction] is used throughout the following WebView2 code snippet.</span></span>  

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

## <a name="events"></a><span data-ttu-id="16443-126">Eventos</span><span class="sxs-lookup"><span data-stu-id="16443-126">Events</span></span>  

<span data-ttu-id="16443-127">Los eventos de la API de WebView2 Win32 C++ usan el par `add_EventName` de métodos and para suscribirse y cancelar la suscripción a `remove_EventName` eventos.</span><span class="sxs-lookup"><span data-stu-id="16443-127">Events in the WebView2 Win32 C++ API use the `add_EventName` and `remove_EventName` method pair to subscribe and unsubscribe from events.</span></span>  <span data-ttu-id="16443-128">El `add_EventName` método toma una interfaz de delegado del controlador de eventos y devuelve un token como parámetro de `EventRegistrationToken` salida.</span><span class="sxs-lookup"><span data-stu-id="16443-128">The `add_EventName` method takes an event handler delegate interface and gives back an `EventRegistrationToken` token as an output parameter.</span></span>  <span data-ttu-id="16443-129">El `remove_EventName` método toma un token y cancela la suscripción de evento `EventRegistrationToken` correspondiente.</span><span class="sxs-lookup"><span data-stu-id="16443-129">The `remove_EventName` method takes an `EventRegistrationToken` token and unsubscribes the corresponding event subscription.</span></span>  

<span data-ttu-id="16443-130">Las interfaces de delegado del controlador de eventos funcionan de forma similar a las interfaces de delegado del controlador completadas con el método asincrónico.</span><span class="sxs-lookup"><span data-stu-id="16443-130">Event handler delegate interfaces work similarly to the async method completed handler delegate interfaces.</span></span>  <span data-ttu-id="16443-131">Se implementa la interfaz de delegado del controlador de eventos y `CoreWebView2` se envía una devolución de llamada cada vez que se ejecuta el evento.</span><span class="sxs-lookup"><span data-stu-id="16443-131">You implement the event handler delegate interface and `CoreWebView2` sends a callback whenever the event runs.</span></span>  <span data-ttu-id="16443-132">Cada interfaz de delegado del controlador de eventos tiene un único `Invoke` método que tiene un parámetro sender seguido de un parámetro event args.</span><span class="sxs-lookup"><span data-stu-id="16443-132">Every event handler delegate interface has a single `Invoke` method that has a sender parameter followed by an event args parameter.</span></span>  <span data-ttu-id="16443-133">El remitente es la instancia del objeto en el que se suscribió para eventos.</span><span class="sxs-lookup"><span data-stu-id="16443-133">The sender is the instance of the object on which you subscribed for events.</span></span>  <span data-ttu-id="16443-134">El parámetro event args es una interfaz que contiene información sobre el evento de activación actual.</span><span class="sxs-lookup"><span data-stu-id="16443-134">The event args parameter is an interface that contains information about the currently firing event.</span></span>  

<span data-ttu-id="16443-135">Por ejemplo, el `NavigationCompleted` evento on tiene el par de `ICoreWebView2` `ICoreWebView2::add_NavigationCompleted` `ICoreWebView2::remove_NavigationCompleted` métodos and.</span><span class="sxs-lookup"><span data-stu-id="16443-135">For instance, the `NavigationCompleted` event on `ICoreWebView2` has the `ICoreWebView2::add_NavigationCompleted` and `ICoreWebView2::remove_NavigationCompleted` method pair.</span></span>  <span data-ttu-id="16443-136">Al enviar una solicitud, se proporciona una instancia de la que ya `ICoreWebView2NavigationCompletedEventHandler` implementó el `Invoke` método.</span><span class="sxs-lookup"><span data-stu-id="16443-136">When you send a request, you provide an instance of `ICoreWebView2NavigationCompletedEventHandler` in which you previously implemented `Invoke` method.</span></span>  <span data-ttu-id="16443-137">Cuando se `NavigationCompleted` ejecuta el evento, se `Invoke` solicita el método.</span><span class="sxs-lookup"><span data-stu-id="16443-137">When the `NavigationCompleted` event runs, your `Invoke` method is requested.</span></span>  <span data-ttu-id="16443-138">El primer parámetro ejecuta el `NavigationCompleted` evento.</span><span class="sxs-lookup"><span data-stu-id="16443-138">The first parameter runs the `NavigationCompleted` event.</span></span>  <span data-ttu-id="16443-139">El segundo parámetro contiene información sobre si la navegación se completó correctamente y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="16443-139">The second parameter contains information about if the navigation completed successfully and so on.</span></span>  

<span data-ttu-id="16443-140">De forma similar a la interfaz de delegado del controlador completado del método asincrónico, use una de las siguientes acciones para configurarla.</span><span class="sxs-lookup"><span data-stu-id="16443-140">Similar to the async method completed handler delegate interface, use one of the following actions to set it up.</span></span>  

*   <span data-ttu-id="16443-141">Implemente directamente.</span><span class="sxs-lookup"><span data-stu-id="16443-141">Implement it directly.</span></span>  
*   <span data-ttu-id="16443-142">Use la [función de devolución de llamada (WRL)][CppCxWrlCallbackFunction] que se usa en el siguiente fragmento de código de WebView2.</span><span class="sxs-lookup"><span data-stu-id="16443-142">Use the [Callback function (WRL)][CppCxWrlCallbackFunction] function that is used in the following WebView2 code snippet.</span></span>  

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

## <a name="strings"></a><span data-ttu-id="16443-143">Cadenas</span><span class="sxs-lookup"><span data-stu-id="16443-143">Strings</span></span>  

<span data-ttu-id="16443-144">Los parámetros de salida de cadena `LPWSTR` son cadenas terminadas en null.</span><span class="sxs-lookup"><span data-stu-id="16443-144">String output parameters are `LPWSTR` null-terminated strings.</span></span>  <span data-ttu-id="16443-145">El solicitante proporciona la cadena mediante `CoTaskMemAlloc` .</span><span class="sxs-lookup"><span data-stu-id="16443-145">The requester provides the string using `CoTaskMemAlloc`.</span></span>  <span data-ttu-id="16443-146">La propiedad se transfiere al solicitante y el solicitante debe liberar la memoria mediante `CoTaskMemFree` .</span><span class="sxs-lookup"><span data-stu-id="16443-146">Ownership is transferred to the requester and it is up to the requester to free the memory using `CoTaskMemFree`.</span></span>  

<span data-ttu-id="16443-147">Los parámetros de entrada de cadena `LPCWSTR` son cadenas terminadas en null.</span><span class="sxs-lookup"><span data-stu-id="16443-147">String input parameters are `LPCWSTR` null-terminated strings.</span></span>  <span data-ttu-id="16443-148">El solicitante garantiza que la cadena es válida durante la duración de la solicitud de función sincrónica.</span><span class="sxs-lookup"><span data-stu-id="16443-148">The requester ensures the string is valid for the duration of the synchronous function request.</span></span>  <span data-ttu-id="16443-149">Si el receptor debe almacenar el valor en algún momento después de que se complete la solicitud de función, el receptor debe proporcionar una copia asociada del valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="16443-149">If the receiver must store the value to some point after the function request completes, the receiver must give an associated copy of the string value.</span></span>  

## <a name="uri-and-json-parsing"></a><span data-ttu-id="16443-150">Análisis DE URI y JSON</span><span class="sxs-lookup"><span data-stu-id="16443-150">URI and JSON parsing</span></span>  

<span data-ttu-id="16443-151">Varios métodos proporcionan o aceptan URI y JSON como cadenas.</span><span class="sxs-lookup"><span data-stu-id="16443-151">Various methods provide or accept URIs and JSON as strings.</span></span>  <span data-ttu-id="16443-152">Use la biblioteca preferida para analizar y generar las cadenas.</span><span class="sxs-lookup"><span data-stu-id="16443-152">Use your preferred library for parsing and generating the strings.</span></span>  

<span data-ttu-id="16443-153">Si WinRT está disponible para la aplicación, puedes usar los métodos and para analizar o producir cadenas JSON o para analizar y `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` producir `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` URI.</span><span class="sxs-lookup"><span data-stu-id="16443-153">If WinRT is available for your app, you may use the `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` methods to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` methods to parse and produce URIs.</span></span>  <span data-ttu-id="16443-154">Ambos métodos funcionan en aplicaciones de Win32.</span><span class="sxs-lookup"><span data-stu-id="16443-154">Both of methods work in Win32 apps.</span></span>  

<span data-ttu-id="16443-155">Si usa y analiza uri, puede usar las siguientes marcas de creación de URI para que el comportamiento coincida más estrechamente con el análisis de URI en `IUri` `CreateUri` `CreateUri` WebView.</span><span class="sxs-lookup"><span data-stu-id="16443-155">If you use `IUri` and `CreateUri` to parse URIs, you may want to use the following URI creation flags to have `CreateUri` behavior more closely match the URI parsing in the WebView.</span></span>  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

## <a name="see-also"></a><span data-ttu-id="16443-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="16443-156">See also</span></span>  

*   <span data-ttu-id="16443-157">Para empezar a usar WebView2 Win32 C/C++, vaya a [Introducción a WebView2][Webview2IndexGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="16443-157">To get started using WebView2 Win32 C/C++, navigate to [Getting started with WebView2][Webview2IndexGettingStarted] guides.</span></span>  
*   <span data-ttu-id="16443-158">Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="16443-158">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="16443-159">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="16443-159">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2GettingstartedWin32]: ../gettingstarted/win32.md "Introducción a WebView2 | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2CapturePreview]: /microsoft-edge/webview2/reference/win32/icorewebview2#capturepreview "CapturePreview: interfaz ICoreWebView2 | Microsoft Docs"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Función de devolución de llamada (WRL) | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Clase WebView2 | Microsoft Docs"  

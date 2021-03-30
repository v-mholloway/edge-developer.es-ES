---
description: Modelo de subprocesamiento
title: Modelo de subprocesos | WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, controlador de explorador, edge html
ms.openlocfilehash: 7b447f5cc5fcce3439166638d47a0b87e5536c0a
ms.sourcegitcommit: 5e218b24fb21fcfa9c82b99f17373fed1ba5a21c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/29/2021
ms.locfileid: "11462046"
---
# <a name="threading-model"></a><span data-ttu-id="a8b9e-104">Modelo de subprocesamiento</span><span class="sxs-lookup"><span data-stu-id="a8b9e-104">Threading model</span></span> 

:::row:::
   :::column span="1":::
      <span data-ttu-id="a8b9e-105">Plataformas compatibles:</span><span class="sxs-lookup"><span data-stu-id="a8b9e-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a8b9e-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="a8b9e-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="a8b9e-107">El control WebView2 se basa en el modelo de objetos componentes [(COM)][WindowsWin32ComTheComponentObjectModel] y debe ejecutarse en un subproceso [de single threaded Apartments (STA).][WindowsWin32ComSingleThreadedApartments]</span><span class="sxs-lookup"><span data-stu-id="a8b9e-107">The WebView2 control is based on the [Component Object Model (COM)][WindowsWin32ComTheComponentObjectModel] and must run on a [Single Threaded Apartments (STA)][WindowsWin32ComSingleThreadedApartments] thread.</span></span>  

## <a name="thread-safety"></a><span data-ttu-id="a8b9e-108">Seguridad de subprocesos</span><span class="sxs-lookup"><span data-stu-id="a8b9e-108">Thread safety</span></span>  

<span data-ttu-id="a8b9e-109">El WebView2 debe crearse en un subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-109">The WebView2 must be created on a UI thread.</span></span>  <span data-ttu-id="a8b9e-110">En concreto, un subproceso con una bomba de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-110">Specifically, a thread with a message pump.</span></span>  <span data-ttu-id="a8b9e-111">Todas las devoluciones de llamada se producen en ese subproceso y las solicitudes en webView2 deben realizarse en ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-111">All callbacks occur on that thread and requests into the WebView2 must be done on that thread.</span></span>  <span data-ttu-id="a8b9e-112">No es seguro usar WebView2 desde otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-112">It isn't safe to use the WebView2 from another thread.</span></span>  

<span data-ttu-id="a8b9e-113">La única excepción es para la `Content` propiedad `CoreWebView2WebResourceRequest` de .</span><span class="sxs-lookup"><span data-stu-id="a8b9e-113">The only exception is for the `Content` property of `CoreWebView2WebResourceRequest`.</span></span>  <span data-ttu-id="a8b9e-114">La `Content` secuencia de propiedades se lee desde un subproceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-114">The `Content` property stream is read from a background thread.</span></span>  <span data-ttu-id="a8b9e-115">La secuencia debe ser ágil o crearse a partir de un STA en segundo plano para evitar la degradación del rendimiento en el subproceso de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-115">The stream should be agile or be created from a background STA to prevent performance degradation to the UI thread.</span></span>  

## <a name="re-entrancy"></a><span data-ttu-id="a8b9e-116">Volver a participar</span><span class="sxs-lookup"><span data-stu-id="a8b9e-116">Re-entrancy</span></span>  

<span data-ttu-id="a8b9e-117">Las devoluciones de llamada, incluidos los controladores de eventos y los controladores de finalización, se ejecutan en serie.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-117">Callbacks including event handlers and completion handlers run serially.</span></span>  
<span data-ttu-id="a8b9e-118">Después de ejecutar un controlador de eventos e iniciar un bucle de mensajes, no podrá ejecutar ningún controlador de eventos o una devolución de llamada de finalización de forma que vuelva a participar.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-118">After you run an event handler and begin a message loop, you're unable to run any event handler or completion callback in a re-entrant manner.</span></span>  

## <a name="deferrals"></a><span data-ttu-id="a8b9e-119">Aplazamientos</span><span class="sxs-lookup"><span data-stu-id="a8b9e-119">Deferrals</span></span>  

<span data-ttu-id="a8b9e-120">Algunos eventos WebView2 leen los valores establecidos en los argumentos de evento relacionados o inician alguna acción después de que se complete el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-120">Some WebView2 events read values set on the related event arguments or start some action after the event handler completes.</span></span>  <span data-ttu-id="a8b9e-121">Si también necesita ejecutar una operación asincrónica como un controlador de eventos, use el método en los argumentos de `GetDeferral` evento de los eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-121">If you also need to run an asynchronous operation such an event handler, use the `GetDeferral` method on the event arguments of the associated events.</span></span>  <span data-ttu-id="a8b9e-122">El objeto devuelto garantiza que el controlador de eventos no se considera completo hasta que se solicita `Deferral` `Complete` el método `Deferral` del.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-122">The returned `Deferral` object ensures the event handler isn't considered complete until the `Complete` method of the `Deferral` is requested.</span></span>  

<span data-ttu-id="a8b9e-123">Por ejemplo, puede usar el evento para proporcionar una para conectarse como una ventana secundaria cuando se complete `NewWindowRequested` `CoreWebView2` el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-123">For instance, you may use the `NewWindowRequested` event to provide a `CoreWebView2` to connect as a child window when the event handler completes.</span></span>  <span data-ttu-id="a8b9e-124">Pero si necesita crear de forma asincrónica `CoreWebView2` el , solicite el método en el `GetDeferral` `NewWindowRequestedEventArgs` .</span><span class="sxs-lookup"><span data-stu-id="a8b9e-124">But if you need to asynchronously create the `CoreWebView2`, request the `GetDeferral` method on the `NewWindowRequestedEventArgs`.</span></span>  <span data-ttu-id="a8b9e-125">Después de crear de forma asincrónica la propiedad y establecerla en la solicitud , en el `CoreWebView2` objeto se devolverá mediante el `NewWindow` `NewWindowRequestedEventArgs` `Complete` `Deferral` `GetDeferral` método.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-125">After you've asynchronously created the `CoreWebView2` and set the `NewWindow` property on the `NewWindowRequestedEventArgs`, request `Complete` on the `Deferral` object be returned using the `GetDeferral` method.</span></span>  

## <a name="block-the-ui-thread"></a><span data-ttu-id="a8b9e-126">Bloquear el subproceso de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="a8b9e-126">Block the UI thread</span></span>  

<span data-ttu-id="a8b9e-127">WebView2 se basa en la bomba de mensajes del subproceso de interfaz de usuario para ejecutar devoluciones de llamada del controlador de eventos y devoluciones de llamada de finalización de métodos asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-127">The WebView2 relies on the message pump of the UI thread to run event handler callbacks and async method completion callbacks.</span></span>  <span data-ttu-id="a8b9e-128">Si usa métodos que bloquean la bomba de mensajes como o , los controladores de eventos WebView2 y los controladores de finalización de `Task.Result` `WaitForSingleObject` métodos asincrónicos no se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-128">If you use methods that block the message pump such as `Task.Result` or `WaitForSingleObject`, then your WebView2 event handlers and async method completion handlers don't run.</span></span>  <span data-ttu-id="a8b9e-129">Por ejemplo, el siguiente código no se completa, ya que detiene la bomba de mensajes mientras espera `Task.Result` `ExecuteScriptAsync` a que se complete.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-129">For example, the following code doesn't complete, because `Task.Result` stops the message pump while it waits for `ExecuteScriptAsync` to complete.</span></span>  <span data-ttu-id="a8b9e-130">Dado que la bomba de mensajes está bloqueada, `ExecuteScriptAsync` no se puede completar.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-130">Since the message pump is blocked, the `ExecuteScriptAsync` isn't able to complete.</span></span>   

```csharp
private void Button_Click(object sender, EventArgs e)
{
    string result = webView2Control.CoreWebView2.ExecuteScriptAsync("'test'").Result;
    MessageBox.Show(this, result, "Script Result");
}
```  

<span data-ttu-id="a8b9e-131">Usa un mecanismo asincrónico como y , que no bloquea la bomba de `await` mensajes ni el subproceso de la interfaz de `async` `await` usuario.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-131">Use an asynchronous `await` mechanism such as `async` and `await`, which doesn't block the message pump or the UI thread.</span></span>  

```csharp
private async void Button_Click(object sender, EventArgs e)
{
    string result = await webView2Control.CoreWebView2.ExecuteScriptAsync("'test'");
    MessageBox.Show(this, result, "Script Result");
}
```  

## <a name="see-also"></a><span data-ttu-id="a8b9e-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a8b9e-132">See also</span></span>  

*   <span data-ttu-id="a8b9e-133">Para empezar a usar WebView2, vaya a Guías de introducción a [WebView2.][Webview2IndexGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="a8b9e-133">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2IndexGettingStarted] guides.</span></span>  
*   <span data-ttu-id="a8b9e-134">Para obtener un ejemplo completo de las capacidades de WebView2, vaya al repositorio [WebView2Samples][GithubMicrosoftedgeWebview2samples] en GitHub.</span><span class="sxs-lookup"><span data-stu-id="a8b9e-134">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="a8b9e-135">Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="a8b9e-135">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="a8b9e-136">Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="a8b9e-136">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="a8b9e-137">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="a8b9e-137">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGettingStarted]: ../index.md#getting-started "Introducción: introducción a Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Clase WebView2 | Microsoft Docs"  

[WindowsWin32ComSingleThreadedApartments]: /windows/win32/com/single-threaded-apartments "Single-Threaded Apartments | Microsoft Docs"  
[WindowsWin32ComTheComponentObjectModel]: /windows/win32/com/the-component-object-model "El modelo de objetos componentes | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

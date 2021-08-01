---
description: En el modelo de subprocesos WebView2, el WebView2 debe crearse en un subproceso de interfaz de usuario con una bomba de mensajes.
title: Modelo de subprocesos para WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, controlador de explorador, edge html
ms.openlocfilehash: fdedb23f3398d0ee6b19cdcea309f48d3d284cd1
ms.sourcegitcommit: 57f52b3edb34b8eb5389b746ff0970f7fd3b9a82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/31/2021
ms.locfileid: "11710684"
---
# <a name="threading-model-for-webview2"></a>Modelo de subprocesos para WebView2

:::row:::
   :::column span="1":::
      Plataformas compatibles:
   :::column-end:::
   :::column span="2":::
      Win32, Windows Forms, WinUi, WPF
   :::column-end:::
:::row-end:::  

El control WebView2 se basa en el modelo de objetos componentes [(COM)][WindowsWin32ComTheComponentObjectModel] y debe ejecutarse en un subproceso [de single threaded Apartments (STA).][WindowsWin32ComSingleThreadedApartments]  

## <a name="thread-safety"></a>Seguridad de subprocesos  

El WebView2 debe crearse en un subproceso de interfaz de usuario que use una bomba de mensajes.  Todas las devoluciones de llamada se producen en ese subproceso y las solicitudes en webView2 deben realizarse en ese subproceso.  No es seguro usar WebView2 desde otro subproceso.  

La única excepción es para la `Content` propiedad `CoreWebView2WebResourceRequest` de .  La `Content` secuencia de propiedades se lee desde un subproceso en segundo plano.  La secuencia debe ser ágil o debe crearse a partir de un STA en segundo plano, para evitar la degradación del rendimiento del subproceso de interfaz de usuario.  

## <a name="re-entrancy"></a>Volver a participar  

Las devoluciones de llamada, incluidos los controladores de eventos y los controladores de finalización, se ejecutan en serie.  Después de ejecutar un controlador de eventos y comenzar un bucle de mensajes, no se puede ejecutar un controlador de eventos o una devolución de llamada de finalización de una forma de volver a participar.  Si una aplicación WebView2 intenta crear un bucle de mensajes anidado o una interfaz de usuario modal de forma sincrónica dentro de un controlador de eventos WebView, este enfoque conduce a intentos de reentrancy.  Dicha reentrancy no se admite en WebView2 y dejaría el controlador de eventos en la pila indefinidamente.

Por ejemplo, no se admite el siguiente enfoque de codificación.

```csharp
private void Btn_Click(object sender, EventArgs e)
{
   // Post web message when button is clicked
   this.webView2Control.ExecuteScriptAsync("window.chrome.webview.postMessage(\"Open Dialog\");");
}

private void CoreWebView2_WebMessageReceived(object sender, CoreWebView2WebMessageReceivedEventArgs e)
{
   string msg = e.TryGetWebMessageAsString();
   if (msg == "Open Dialog")
   {
      Form1 form = new Form1(); // Create a new form that contains a new WebView when web message is received.
      form.ShowDialog(); // This will cause a reentrancy issue and cause the newly created WebView inside the modal dialog to hang.
   }
}
```     

En su lugar, programe el trabajo adecuado para que se lleve a cabo después de completar el controlador de eventos, como se muestra en el código siguiente.

```csharp
private void CoreWebView2_WebMessageReceived(object sender, CoreWebView2WebMessageReceivedEventArgs e)
{
   string msg = e.TryGetWebMessageAsString();
   if (msg == "Open Dialog")
   {
      // Show a modal dialog after the current event handler is completed, to avoid potential reentrancy caused by running a nested message loop in the WebView2 event handler.
      System.Threading.SynchronizationContext.Current.Post((_) => {
         Form1 form = new Form1(); 
         form.ShowDialog();
         form.Closed();
      }, null);
   }
}
``` 

> [!NOTE]
> Para las aplicaciones WinForms y WPF, para obtener la pila de llamadas completa con fines de depuración, debe activar la depuración de código nativo para aplicaciones webView2, como se muestra a continuación.
> 1.  Abra el proyecto WebView2 en Visual Studio.
> 1.  En **el Explorador de**soluciones, haga clic con el botón secundario en el proyecto WebView2 y, a continuación, seleccione **Propiedades**.  
> 1.  Seleccione la **pestaña Depurar** y, a continuación, active la casilla Habilitar depuración de **código nativo,** como se muestra a continuación.

:::image type="complex" source="../media/webview-enable-native-debug.png" alt-text="Habilitar la depuración de código nativo en Visual Studio" lightbox="../media/webview-enable-native-debug.png":::
   Habilitar la depuración de código nativo en Visual Studio
:::image-end:::  

## <a name="deferrals"></a>Aplazamientos  

Algunos eventos WebView2 leen valores establecidos en los argumentos de evento relacionados o inician alguna acción después de que se complete el controlador de eventos.  Si también necesita ejecutar una operación asincrónica, como un controlador de eventos, use el método en los argumentos de evento `GetDeferral` de los eventos asociados.  El objeto devuelto garantiza que el controlador de eventos no se considera completo hasta que se solicita `Deferral` `Complete` el método `Deferral` del.  

Por ejemplo, puede usar el evento para proporcionar una para conectarse como una ventana secundaria cuando se complete `NewWindowRequested` `CoreWebView2` el controlador de eventos.  Pero si necesita crear de forma asincrónica `CoreWebView2` el , debe solicitar el método en el `GetDeferral` `NewWindowRequestedEventArgs` .  Después de crear de forma asincrónica la propiedad y establecerla en la solicitud , en el objeto devuelto `CoreWebView2` `NewWindow` por el `NewWindowRequestedEventArgs` `Complete` `Deferral` `GetDeferral` método.  

## <a name="block-the-ui-thread"></a>Bloquear el subproceso de interfaz de usuario  

WebView2 se basa en la bomba de mensajes del subproceso de interfaz de usuario para ejecutar devoluciones de llamada del controlador de eventos y devoluciones de llamada de finalización de métodos asincrónicos.  Si usa métodos que bloquean la bomba de mensajes, como o , los controladores de eventos WebView2 y los controladores de finalización `Task.Result` `WaitForSingleObject` de métodos asincrónicos no se ejecutan.  Por ejemplo, el siguiente código no se completa, ya que detiene la bomba de mensajes mientras espera `Task.Result` `ExecuteScriptAsync` a que se complete.  Dado que la bomba de mensajes está bloqueada, `ExecuteScriptAsync` no se puede completar.

Por ejemplo, el siguiente código no funciona, ya que usa `Task.Result` .

```csharp
private void Button_Click(object sender, EventArgs e)
{
    string result = webView2Control.CoreWebView2.ExecuteScriptAsync("'test'").Result;
    MessageBox.Show(this, result, "Script Result");
}
```  

En su lugar, usa un mecanismo asincrónico como y , que no bloquea la bomba de `await` mensajes o el subproceso de interfaz de `async` `await` usuario.  Por ejemplo:

```csharp
private async void Button_Click(object sender, EventArgs e)
{
    string result = await webView2Control.CoreWebView2.ExecuteScriptAsync("'test'");
    MessageBox.Show(this, result, "Script Result");
}
```  

## <a name="see-also"></a>Vea también  

*   Para empezar a usar WebView2, vaya a [WebView2 Introducción Guías][Webview2IndexGetStarted].  
*   Para obtener un ejemplo completo de las funcionalidades de WebView2, vaya a [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] en GitHub.  
*   Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][DotnetApiMicrosoftWebWebview2WpfWebview2].  
*   Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Ponerse en contacto con el equipo de Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  
[Webview2IndexGetStarted]: ../index.md#get-started "Introducción: introducción a Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 | Microsoft Docs"  
<!-- external links -->
[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Clase WebView2 | Microsoft Docs"  

[WindowsWin32ComSingleThreadedApartments]: /windows/win32/com/single-threaded-apartments "Single-Threaded Apartments | Microsoft Docs"  
[WindowsWin32ComTheComponentObjectModel]: /windows/win32/com/the-component-object-model "El modelo de objetos componentes | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

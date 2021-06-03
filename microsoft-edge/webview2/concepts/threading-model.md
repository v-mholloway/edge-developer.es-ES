---
description: Modelo de subprocesos
title: Modelo de subprocesos | WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, controlador de explorador, edge html
ms.openlocfilehash: 9a7ce3d66e53b832d4430afb153e6539d97e5db7
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535611"
---
# <a name="threading-model"></a>Modelo de subprocesos 

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

El WebView2 debe crearse en un subproceso de interfaz de usuario.  En concreto, un subproceso con una bomba de mensajes.  Todas las devoluciones de llamada se producen en ese subproceso y las solicitudes en webView2 deben realizarse en ese subproceso.  No es seguro usar WebView2 desde otro subproceso.  

La única excepción es para la `Content` propiedad `CoreWebView2WebResourceRequest` de .  La `Content` secuencia de propiedades se lee desde un subproceso en segundo plano.  La secuencia debe ser ágil o crearse a partir de un STA en segundo plano para evitar la degradación del rendimiento en el subproceso de la interfaz de usuario.  

## <a name="re-entrancy"></a>Volver a participar  

Las devoluciones de llamada, incluidos los controladores de eventos y los controladores de finalización, se ejecutan en serie.  
Después de ejecutar un controlador de eventos e iniciar un bucle de mensajes, no podrá ejecutar ningún controlador de eventos o una devolución de llamada de finalización de forma que vuelva a participar.  

## <a name="deferrals"></a>Aplazamientos  

Algunos eventos WebView2 leen los valores establecidos en los argumentos de evento relacionados o inician alguna acción después de que se complete el controlador de eventos.  Si también necesita ejecutar una operación asincrónica como un controlador de eventos, use el método en los argumentos de `GetDeferral` evento de los eventos asociados.  El objeto devuelto garantiza que el controlador de eventos no se considera completo hasta que se solicita `Deferral` `Complete` el método `Deferral` del.  

Por ejemplo, puede usar el evento para proporcionar una para conectarse como una ventana secundaria cuando se complete `NewWindowRequested` `CoreWebView2` el controlador de eventos.  Pero si necesita crear de forma asincrónica `CoreWebView2` el , solicite el método en el `GetDeferral` `NewWindowRequestedEventArgs` .  Después de crear de forma asincrónica la propiedad y establecerla en la solicitud , en el `CoreWebView2` objeto se devolverá mediante el `NewWindow` `NewWindowRequestedEventArgs` `Complete` `Deferral` `GetDeferral` método.  

## <a name="block-the-ui-thread"></a>Bloquear el subproceso de interfaz de usuario  

WebView2 se basa en la bomba de mensajes del subproceso de interfaz de usuario para ejecutar devoluciones de llamada del controlador de eventos y devoluciones de llamada de finalización de métodos asincrónicos.  Si usa métodos que bloquean la bomba de mensajes como o , los controladores de eventos WebView2 y los controladores de finalización de `Task.Result` `WaitForSingleObject` métodos asincrónicos no se ejecutan.  Por ejemplo, el siguiente código no se completa, ya que detiene la bomba de mensajes mientras espera `Task.Result` `ExecuteScriptAsync` a que se complete.  Dado que la bomba de mensajes está bloqueada, `ExecuteScriptAsync` no se puede completar.   

```csharp
private void Button_Click(object sender, EventArgs e)
{
    string result = webView2Control.CoreWebView2.ExecuteScriptAsync("'test'").Result;
    MessageBox.Show(this, result, "Script Result");
}
```  

Usa un mecanismo asincrónico como y , que no bloquea la bomba de `await` mensajes ni el subproceso de la interfaz de `async` `await` usuario.  

```csharp
private async void Button_Click(object sender, EventArgs e)
{
    string result = await webView2Control.CoreWebView2.ExecuteScriptAsync("'test'");
    MessageBox.Show(this, result, "Script Result");
}
```  

## <a name="see-also"></a>Consulta también  

*   Para empezar a usar WebView2, vaya a Guías de Introducción [WebView2.][Webview2IndexGetStarted]  
*   Para obtener un ejemplo completo de las funcionalidades de WebView2, vaya a [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] en GitHub.  
*   Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][DotnetApiMicrosoftWebWebview2WpfWebview2].  
*   Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Getting in touch with the Microsoft Edge WebView team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Introducción: introducción a Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Clase WebView2 | Microsoft Docs"  

[WindowsWin32ComSingleThreadedApartments]: /windows/win32/com/single-threaded-apartments "Single-Threaded Apartments | Microsoft Docs"  
[WindowsWin32ComTheComponentObjectModel]: /windows/win32/com/the-component-object-model "El modelo de objetos componentes | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

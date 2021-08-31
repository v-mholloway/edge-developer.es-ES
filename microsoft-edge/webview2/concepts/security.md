---
description: Comprender cómo desarrollar aplicaciones webview2 seguras
title: Procedimientos recomendados para desarrollar aplicaciones webview2 seguras
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral, seguridad
ms.openlocfilehash: 4f4da9e2db588b99f6fe2538941969beb2343a77
ms.sourcegitcommit: 66a8e3db5b63b0532ca2f4003fa37bde6bd225b0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2021
ms.locfileid: "11934068"
---
# <a name="best-practices-for-developing-secure-webview2-applications"></a>Procedimientos recomendados para desarrollar aplicaciones webview2 seguras  

El [control WebView2][Webview2Main] permite a los desarrolladores hospedar contenido web en las aplicaciones nativas. Cuando se usa correctamente, hospedar contenido web ofrece varias ventajas, como el uso de la interfaz de usuario basada en web, el acceso a las características de la plataforma web, el uso compartido de código entre plataformas, entre plataformas, y así sucesivamente.  Para evitar vulnerabilidades que pueden surgir al hospedar contenido web, asegúrese de diseñar la aplicación WebView2 para supervisar estrechamente las interacciones entre el contenido web y la aplicación host.  

1.  Trate todo el contenido web como inseguro.  
    *   Valide los mensajes web y los parámetros del objeto host antes de consumir cada uno, ya que los mensajes y parámetros web pueden estar malformados \(involuntaria o malintencionadamente\) y provocar que la aplicación se comporte inesperadamente.
    *   Compruebe siempre el origen del documento que se ejecuta dentro de WebView2 y evalúe la fiabilidad del contenido.  
1.  Diseñe mensajes web específicos e interacciones de objetos host en lugar de usar servidores proxy genéricos.  
1.  Establezca las siguientes opciones para restringir la funcionalidad de contenido web [modificando ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] o [CoreWebView2Settings (.NET).][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]  
    *   Se establece en , si no espera que el `AreHostObjectsAllowed` contenido web tenga acceso a objetos `false` host.  
    *   Establezca en , si no espera que el contenido `IsWebMessageEnabled` web publique mensajes web en la aplicación `false` nativa.  
    *   Establezca en , si no espera que el contenido web ejecute `IsScriptEnabled` scripts \(por ejemplo, al mostrar `false` contenido html estático\).  
    *   Establezca en , si no espera que el `AreDefaultScriptDialogsEnabled` contenido web se muestre o cuadros de `false` `alert` `prompt` diálogo.  
1.  En los pasos siguientes, use los `NavigationStarting` eventos y para actualizar la configuración según el origen de la nueva `FrameNavigationStarting` página.  
    1.  Para evitar que la aplicación vaya a determinadas páginas, use los eventos para comprobar y, a continuación, bloquear la navegación de páginas o fotogramas.  
    1.  Al navegar a una página nueva, es posible que deba ajustar los valores de propiedad en [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] o [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] como se describió anteriormente.  
1.  Al navegar a un nuevo documento, use el `ContentLoading` evento para quitar objetos host expuestos mediante `RemoveHostObjectFromScript` .  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Introducción a Microsoft Edge WebView2 | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2settings]: /microsoft-edge/webview2/reference/win32/icorewebview2settings "interfaz ICoreWebView2Settings | Microsoft Docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]: /dotnet/api/microsoft.web.webview2.core.corewebview2settings "Clase CoreWebView2Settings (Microsoft.Web.WebView2.Core) | Microsoft Docs"  

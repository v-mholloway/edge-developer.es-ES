---
description: Comprender cómo desarrollar aplicaciones de WebView2 seguras
title: Procedimientos recomendados para desarrollar aplicaciones de WebView2 seguras
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge, seguridad
ms.openlocfilehash: 774c812789bea4936611c41915e0c34f93205dba
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010764"
---
# Procedimientos recomendados para desarrollar aplicaciones de WebView2 seguras  

El [control WebView2][Webview2Main] permite a los programadores hospedar contenido web en las aplicaciones nativas. Cuando se usa correctamente, el contenido Web de hospedaje ofrece varias ventajas, como el uso de interfaces de usuario basadas en Web, el acceso a características de la plataforma web, el uso compartido de código entre plataformas, etc.  Para evitar las vulnerabilidades que pueden surgir al hospedar contenido Web, asegúrese de diseñar su aplicación WebView2 para supervisar estrechamente las interacciones entre el contenido web y la aplicación host.  

1.  Tratar todo el contenido web como inseguro.  
    *   Valide los mensajes web y los parámetros de objeto de host antes de consumirlos, ya que los mensajes web y los parámetros pueden tener un formato incorrecto \ (involuntariamente o malintencionado \) y hacer que la aplicación se comporte de manera inesperada.
    *   Compruebe siempre el origen del documento que se está ejecutando dentro de WebView2 y evalúe la confiabilidad del contenido.  
1.  Diseñe mensajes Web específicos y interacciones de objeto de hospedaje en lugar de usar proxies genéricos.  
1.  Establezca las siguientes opciones para restringir la funcionalidad de contenido web modificando [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209622Icorewebview2settings] o [CoreWebView2Settings (.net)][Webview2ReferenceWin3209628MicrosoftWebWebview2CoreCorewebview2settings].  
    *   Se establece `AreHostObjectsAllowed` en `false` si no se espera que el contenido web tenga acceso a los objetos host.  
    *   Se establece `IsWebMessageEnabled` en `false` si no se espera que el contenido web publique mensajes Web en la aplicación nativa.  
    *   Se establece `IsScriptEnabled` en `false` si no se espera que el contenido web ejecute scripts \ (por ejemplo, al mostrar contenido HTML estático \).  
    *   Se establece `AreDefaultScriptDialogsEnabled` en `false` si no se espera que el contenido web aparezca o no en los `alert` cuadros de `prompt` diálogo.  
1.  En los pasos siguientes, use los `NavigationStarting` `FrameNavigationStarting` eventos y para actualizar la configuración en función del origen de la página nueva.  
    1.  Para evitar que la aplicación navegue a determinadas páginas, use los eventos para comprobar y, a continuación, bloquear la navegación de página o marco.  
    1.  Al navegar a una página nueva, es posible que tenga que ajustar los valores de propiedad en [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209622Icorewebview2settings] o [CoreWebView2Settings (.net)][Webview2ReferenceWin3209628MicrosoftWebWebview2CoreCorewebview2settings] como se ha descrito anteriormente.  
1.  Cuando navegue a un documento nuevo, use el `ContentLoading` evento para quitar objetos de host expuestos mediante `RemoveHostObjectFromScript` .  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  

[Webview2ReferenceWin3209622Icorewebview2settings]: ../reference/win32/0-9-622/icorewebview2settings.md "interfaz ICoreWebView2Settings | Microsoft docs"  

[Webview2ReferenceWin3209628MicrosoftWebWebview2CoreCorewebview2settings]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2settings.md "Clase Microsoft. Web. WebView2. Core. CoreWebView2Settings | Microsoft docs"  

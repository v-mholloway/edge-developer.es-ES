---
description: Comprender cómo desarrollar aplicaciones de WebView2 seguras
title: Procedimientos recomendados para desarrollar aplicaciones de WebView2 seguras
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge, seguridad
ms.openlocfilehash: f30163954f1906f71afa520b87d58c7647a5250a
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894308"
---
# <span data-ttu-id="a62c3-104">Procedimientos recomendados para desarrollar aplicaciones de WebView2 seguras</span><span class="sxs-lookup"><span data-stu-id="a62c3-104">Best practices for developing secure WebView2 applications</span></span>  

<span data-ttu-id="a62c3-105">El [control WebView2][Webview2Main] permite a los programadores hospedar contenido web en las aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="a62c3-105">The [WebView2 control][Webview2Main] allows developers to host web content in the native applications.</span></span> <span data-ttu-id="a62c3-106">Cuando se usa correctamente, el contenido Web de hospedaje ofrece varias ventajas, como el uso de interfaces de usuario basadas en Web, el acceso a características de la plataforma web, el uso compartido de código entre plataformas, etc.</span><span class="sxs-lookup"><span data-stu-id="a62c3-106">When used correctly, hosting web content offers several advantages, such as using web-based UI, accessing features of the web platform, sharing code cross-platform, and so on.</span></span>  <span data-ttu-id="a62c3-107">Para evitar las vulnerabilidades que pueden surgir al hospedar contenido Web, asegúrese de diseñar su aplicación WebView2 para supervisar estrechamente las interacciones entre el contenido web y la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="a62c3-107">To avoid vulnerabilities that can arise from hosting web content, make sure to design your WebView2 application to closely monitor interactions between the web content and the host application.</span></span>  

1.  <span data-ttu-id="a62c3-108">Tratar todo el contenido web como inseguro.</span><span class="sxs-lookup"><span data-stu-id="a62c3-108">Treat all web content as insecure.</span></span>  
    *   <span data-ttu-id="a62c3-109">Valide los mensajes web y los parámetros de objeto de host antes de consumirlos, ya que los mensajes web y los parámetros pueden tener un formato incorrecto \ (involuntariamente o malintencionado \) y hacer que la aplicación se comporte de manera inesperada.</span><span class="sxs-lookup"><span data-stu-id="a62c3-109">Validate web messages and host object parameters before consuming each, because web messages and parameters can be malformed \(unintentionally or maliciously\) and cause the app to behave unexpectedly.</span></span>
    *   <span data-ttu-id="a62c3-110">Compruebe siempre el origen del documento que se está ejecutando dentro de WebView2 y evalúe la confiabilidad del contenido.</span><span class="sxs-lookup"><span data-stu-id="a62c3-110">Always check the origin of the document running inside WebView2 and assess the trustworthiness of the content.</span></span>  
1.  <span data-ttu-id="a62c3-111">Diseñe mensajes Web específicos y interacciones de objeto de hospedaje en lugar de usar proxies genéricos.</span><span class="sxs-lookup"><span data-stu-id="a62c3-111">Design specific web messages and host object interactions instead of using generic proxies.</span></span>  
1.  <span data-ttu-id="a62c3-112">Establezca las siguientes opciones para restringir la funcionalidad de contenido web modificando [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] o [CoreWebView2Settings (.net)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings].</span><span class="sxs-lookup"><span data-stu-id="a62c3-112">Set the following options to restrict web content functionality by modifying [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings].</span></span>  
    *   <span data-ttu-id="a62c3-113">Se establece `AreHostObjectsAllowed` en `false` si no se espera que el contenido web tenga acceso a los objetos host.</span><span class="sxs-lookup"><span data-stu-id="a62c3-113">Set `AreHostObjectsAllowed` to `false`, if you do not expect the web content to access host objects.</span></span>  
    *   <span data-ttu-id="a62c3-114">Se establece `IsWebMessageEnabled` en `false` si no se espera que el contenido web publique mensajes Web en la aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="a62c3-114">Set `IsWebMessageEnabled` to `false`, if you do not expect the web content to post web messages to your native application.</span></span>  
    *   <span data-ttu-id="a62c3-115">Se establece `IsScriptEnabled` en `false` si no se espera que el contenido web ejecute scripts \ (por ejemplo, al mostrar contenido HTML estático \).</span><span class="sxs-lookup"><span data-stu-id="a62c3-115">Set `IsScriptEnabled` to `false`, if you do not expect the web content to run scripts \(for example, when showing static html content\).</span></span>  
    *   <span data-ttu-id="a62c3-116">Se establece `AreDefaultScriptDialogsEnabled` en `false` si no se espera que el contenido web aparezca o no en los `alert` cuadros de `prompt` diálogo.</span><span class="sxs-lookup"><span data-stu-id="a62c3-116">Set `AreDefaultScriptDialogsEnabled` to `false`, if you do not expect the web content to show `alert` or `prompt` dialog boxes.</span></span>  
1.  <span data-ttu-id="a62c3-117">En los pasos siguientes, use los `NavigationStarting` `FrameNavigationStarting` eventos y para actualizar la configuración en función del origen de la página nueva.</span><span class="sxs-lookup"><span data-stu-id="a62c3-117">In the following steps, use the `NavigationStarting` and `FrameNavigationStarting` events to update settings based on the origin of the new page.</span></span>  
    1.  <span data-ttu-id="a62c3-118">Para evitar que la aplicación navegue a determinadas páginas, use los eventos para comprobar y, a continuación, bloquear la navegación de página o marco.</span><span class="sxs-lookup"><span data-stu-id="a62c3-118">To prevent your application from navigating to certain pages, use the events to check and then block page or frame navigation.</span></span>  
    1.  <span data-ttu-id="a62c3-119">Al navegar a una página nueva, es posible que tenga que ajustar los valores de propiedad en [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] o [CoreWebView2Settings (.net)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings] como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a62c3-119">When navigating to a new page, you may need to adjust the property values on [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings] as previously described.</span></span>  
1.  <span data-ttu-id="a62c3-120">Cuando navegue a un documento nuevo, use el `ContentLoading` evento para quitar objetos de host expuestos mediante `RemoveHostObjectFromScript` .</span><span class="sxs-lookup"><span data-stu-id="a62c3-120">When navigating to a new document, use the `ContentLoading` event to remove exposed host objects using `RemoveHostObjectFromScript`.</span></span>  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  

[Webview2ReferenceWin3209538Icorewebview2settings]: ../reference/win32/0-9-538/icorewebview2settings.md "interfaz ICoreWebView2Settings | Microsoft docs"  

[Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings]: ../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2settings.md "Clase Microsoft. Web. WebView2. Core. CoreWebView2Settings | Microsoft docs"  

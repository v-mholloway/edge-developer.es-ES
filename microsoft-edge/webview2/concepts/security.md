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
ms.openlocfilehash: d53417cc1ac98b44565692edbaec06216f7c110b
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119006"
---
# <span data-ttu-id="58d64-104">Procedimientos recomendados para desarrollar aplicaciones webview2 seguras</span><span class="sxs-lookup"><span data-stu-id="58d64-104">Best practices for developing secure WebView2 applications</span></span>  

<span data-ttu-id="58d64-105">El [control WebView2][Webview2Main] permite a los desarrolladores hospedar contenido web en las aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="58d64-105">The [WebView2 control][Webview2Main] allows developers to host web content in the native applications.</span></span> <span data-ttu-id="58d64-106">Cuando se usa correctamente, hospedar contenido web ofrece varias ventajas, como el uso de la interfaz de usuario basada en web, el acceso a las características de la plataforma web, el uso compartido de código entre plataformas, entre plataformas, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="58d64-106">When used correctly, hosting web content offers several advantages, such as using web-based UI, accessing features of the web platform, sharing code cross-platform, and so on.</span></span>  <span data-ttu-id="58d64-107">Para evitar vulnerabilidades que pueden surgir al hospedar contenido web, asegúrese de diseñar la aplicación WebView2 para supervisar estrechamente las interacciones entre el contenido web y la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="58d64-107">To avoid vulnerabilities that can arise from hosting web content, make sure to design your WebView2 application to closely monitor interactions between the web content and the host application.</span></span>  

1.  <span data-ttu-id="58d64-108">Trate todo el contenido web como inseguro.</span><span class="sxs-lookup"><span data-stu-id="58d64-108">Treat all web content as insecure.</span></span>  
    *   <span data-ttu-id="58d64-109">Valide los mensajes web y los parámetros del objeto host antes de consumir cada uno, ya que los mensajes y parámetros web pueden estar malformados \(involuntaria o malintencionadamente\) y provocar que la aplicación se comporte inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="58d64-109">Validate web messages and host object parameters before consuming each, because web messages and parameters can be malformed \(unintentionally or maliciously\) and cause the app to behave unexpectedly.</span></span>
    *   <span data-ttu-id="58d64-110">Compruebe siempre el origen del documento que se ejecuta dentro de WebView2 y evalúe la fiabilidad del contenido.</span><span class="sxs-lookup"><span data-stu-id="58d64-110">Always check the origin of the document running inside WebView2 and assess the trustworthiness of the content.</span></span>  
1.  <span data-ttu-id="58d64-111">Diseñe mensajes web específicos e interacciones de objetos host en lugar de usar servidores proxy genéricos.</span><span class="sxs-lookup"><span data-stu-id="58d64-111">Design specific web messages and host object interactions instead of using generic proxies.</span></span>  
1.  <span data-ttu-id="58d64-112">Establezca las siguientes opciones para restringir la funcionalidad de contenido web [modificando ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] o [CoreWebView2Settings (.NET).][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]</span><span class="sxs-lookup"><span data-stu-id="58d64-112">Set the following options to restrict web content functionality by modifying [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings].</span></span>  
    *   <span data-ttu-id="58d64-113">Se establece en , si no espera que el `AreHostObjectsAllowed` contenido web tenga acceso a objetos `false` host.</span><span class="sxs-lookup"><span data-stu-id="58d64-113">Set `AreHostObjectsAllowed` to `false`, if you do not expect the web content to access host objects.</span></span>  
    *   <span data-ttu-id="58d64-114">Establezca en , si no espera que el contenido `IsWebMessageEnabled` web publique mensajes web en la aplicación `false` nativa.</span><span class="sxs-lookup"><span data-stu-id="58d64-114">Set `IsWebMessageEnabled` to `false`, if you do not expect the web content to post web messages to your native application.</span></span>  
    *   <span data-ttu-id="58d64-115">Establezca en , si no espera que el contenido web ejecute `IsScriptEnabled` scripts \(por ejemplo, al mostrar `false` contenido html estático\).</span><span class="sxs-lookup"><span data-stu-id="58d64-115">Set `IsScriptEnabled` to `false`, if you do not expect the web content to run scripts \(for example, when showing static html content\).</span></span>  
    *   <span data-ttu-id="58d64-116">Establezca en , si no espera que el `AreDefaultScriptDialogsEnabled` contenido web se muestre o cuadros de `false` `alert` `prompt` diálogo.</span><span class="sxs-lookup"><span data-stu-id="58d64-116">Set `AreDefaultScriptDialogsEnabled` to `false`, if you do not expect the web content to show `alert` or `prompt` dialog boxes.</span></span>  
1.  <span data-ttu-id="58d64-117">En los pasos siguientes, use los `NavigationStarting` eventos y para actualizar la configuración según el origen de la nueva `FrameNavigationStarting` página.</span><span class="sxs-lookup"><span data-stu-id="58d64-117">In the following steps, use the `NavigationStarting` and `FrameNavigationStarting` events to update settings based on the origin of the new page.</span></span>  
    1.  <span data-ttu-id="58d64-118">Para evitar que la aplicación vaya a determinadas páginas, use los eventos para comprobar y, a continuación, bloquear la navegación de páginas o fotogramas.</span><span class="sxs-lookup"><span data-stu-id="58d64-118">To prevent your application from navigating to certain pages, use the events to check and then block page or frame navigation.</span></span>  
    1.  <span data-ttu-id="58d64-119">Al navegar a una página nueva, es posible que deba ajustar los valores de propiedad en [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] o [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="58d64-119">When navigating to a new page, you may need to adjust the property values on [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] as previously described.</span></span>  
1.  <span data-ttu-id="58d64-120">Al navegar a un nuevo documento, use el `ContentLoading` evento para quitar objetos host expuestos mediante `RemoveHostObjectFromScript` .</span><span class="sxs-lookup"><span data-stu-id="58d64-120">When navigating to a new document, use the `ContentLoading` event to remove exposed host objects using `RemoveHostObjectFromScript`.</span></span>  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2settings]: /microsoft-edge/webview2/reference/win32/icorewebview2settings "interfaz ICoreWebView2Settings | Microsoft Docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]: /dotnet/api/microsoft.web.webview2.core.corewebview2settings "Clase CoreWebView2Settings (Microsoft.Web.WebView2.Core) | Microsoft Docs"  

---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
ms.openlocfilehash: 42ea3beb51dc315ed7ab3b7b0c04c7414adab2db
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012604"
---
# <span data-ttu-id="f62d3-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="f62d3-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

<span data-ttu-id="f62d3-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f62d3-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f62d3-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f62d3-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f62d3-107">Se crea un receptor para un evento de protocolo DevTools en particular y le permite suscribirse y anular la suscripción de ese evento.</span><span class="sxs-lookup"><span data-stu-id="f62d3-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="f62d3-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="f62d3-108">Summary</span></span>

 <span data-ttu-id="f62d3-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f62d3-109">Members</span></span>                        | <span data-ttu-id="f62d3-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f62d3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f62d3-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="f62d3-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="f62d3-112">Suscribirse a un evento de DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="f62d3-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="f62d3-113">Obtenido del objeto WebView a través de GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="f62d3-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="f62d3-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="f62d3-114">Members</span></span>

#### <span data-ttu-id="f62d3-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="f62d3-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="f62d3-116">Suscribirse a un evento de DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="f62d3-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="f62d3-117">evento público EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="f62d3-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="f62d3-118">Se llamará al método Invoke del controlador siempre que se desencadene el evento DevToolsProtocol correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f62d3-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="f62d3-119">Se llamará a Invoke con un objeto de argumentos de evento que contenga el objeto de parámetro del protocolo DevTools como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="f62d3-119">Invoke will be called with an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>


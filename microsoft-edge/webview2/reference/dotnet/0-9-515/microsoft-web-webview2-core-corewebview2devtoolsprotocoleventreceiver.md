---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 23ee363fd90416d07c76644879a5f4b6cc2acabe
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655389"
---
# <span data-ttu-id="8d2f7-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="8d2f7-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

<span data-ttu-id="8d2f7-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="8d2f7-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="8d2f7-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="8d2f7-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="8d2f7-107">Se crea un receptor para un evento de protocolo DevTools en particular y le permite suscribirse y anular la suscripción de ese evento.</span><span class="sxs-lookup"><span data-stu-id="8d2f7-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="8d2f7-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="8d2f7-108">Summary</span></span>

 <span data-ttu-id="8d2f7-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8d2f7-109">Members</span></span>                        | <span data-ttu-id="8d2f7-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8d2f7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8d2f7-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="8d2f7-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="8d2f7-112">Suscribirse a un evento de DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="8d2f7-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="8d2f7-113">Obtenido del objeto WebView a través de GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="8d2f7-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="8d2f7-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="8d2f7-114">Members</span></span>

#### <span data-ttu-id="8d2f7-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="8d2f7-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="8d2f7-116">Suscribirse a un evento de DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="8d2f7-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="8d2f7-117">evento público EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="8d2f7-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="8d2f7-118">Se llamará al método Invoke del controlador siempre que se desencadene el evento DevToolsProtocol correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8d2f7-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="8d2f7-119">Se llamará a Invoke con el objeto de parámetro de un evento que contiene el objeto de parámetro del protocolo DevTools como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="8d2f7-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>


---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceivedEventHandler
ms.openlocfilehash: 2cb38d40e4e4a5e527cc8e8643b31ae7ceebecbe
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879600"
---
# <span data-ttu-id="28d02-104">interfaz ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="28d02-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="28d02-105">La persona que llama implementa esta interfaz para recibir eventos DevToolsProtocolEventReceived de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="28d02-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="28d02-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="28d02-106">Summary</span></span>

 <span data-ttu-id="28d02-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="28d02-107">Members</span></span>                        | <span data-ttu-id="28d02-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="28d02-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="28d02-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="28d02-109">Invoke</span></span>](#invoke) | <span data-ttu-id="28d02-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="28d02-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="28d02-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="28d02-111">Members</span></span>

#### <span data-ttu-id="28d02-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="28d02-112">Invoke</span></span> 

<span data-ttu-id="28d02-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="28d02-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="28d02-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="28d02-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>


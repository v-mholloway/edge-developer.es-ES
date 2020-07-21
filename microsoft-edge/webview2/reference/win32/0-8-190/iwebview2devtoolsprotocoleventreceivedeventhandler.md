---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: a26a2c18c402bffe11353b2f53f0559acde3663b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886167"
---
# <span data-ttu-id="aec23-104">0.8.355: IWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="aec23-104">0.8.355 - interface IWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="aec23-105">La persona que llama implementa esta interfaz para recibir eventos DevToolsProtocolEventReceived desde el [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="aec23-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the [IWebView2WebView](IWebView2WebView.md).</span></span>

## <span data-ttu-id="aec23-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="aec23-106">Summary</span></span>

 <span data-ttu-id="aec23-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="aec23-107">Members</span></span>                        | <span data-ttu-id="aec23-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="aec23-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aec23-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="aec23-109">Invoke</span></span>](#invoke) | <span data-ttu-id="aec23-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="aec23-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="aec23-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="aec23-111">Members</span></span>

#### <span data-ttu-id="aec23-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="aec23-112">Invoke</span></span> 

<span data-ttu-id="aec23-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="aec23-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="aec23-114">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DevToolsProtocolEventReceivedEventArgs](IWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="aec23-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DevToolsProtocolEventReceivedEventArgs](IWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: c08a851eb21947cae4af465a233dc4c49508c84c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884214"
---
# <span data-ttu-id="d1548-104">0.9.430: ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d1548-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="d1548-105">La persona que llama implementa esta interfaz para recibir eventos DevToolsProtocolEventReceived de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="d1548-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="d1548-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="d1548-106">Summary</span></span>

 <span data-ttu-id="d1548-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1548-107">Members</span></span>                        | <span data-ttu-id="d1548-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d1548-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d1548-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d1548-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d1548-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d1548-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d1548-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1548-111">Members</span></span>

#### <span data-ttu-id="d1548-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="d1548-112">Invoke</span></span> 

<span data-ttu-id="d1548-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d1548-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d1548-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d1548-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>


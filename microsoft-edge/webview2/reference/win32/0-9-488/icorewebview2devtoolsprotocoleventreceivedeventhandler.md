---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 1e59d8d830c3357fafd4f8315388ee5fff93a3d2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880811"
---
# <span data-ttu-id="b3ef1-104">0.9.515: ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b3ef1-104">0.9.515 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="b3ef1-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="b3ef1-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b3ef1-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="b3ef1-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="b3ef1-107">La persona que llama implementa esta interfaz para recibir eventos DevToolsProtocolEventReceived de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="b3ef1-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="b3ef1-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="b3ef1-108">Summary</span></span>

 <span data-ttu-id="b3ef1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b3ef1-109">Members</span></span>                        | <span data-ttu-id="b3ef1-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b3ef1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b3ef1-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="b3ef1-111">Invoke</span></span>](#invoke) | <span data-ttu-id="b3ef1-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b3ef1-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b3ef1-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="b3ef1-113">Members</span></span>

#### <span data-ttu-id="b3ef1-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="b3ef1-114">Invoke</span></span> 

<span data-ttu-id="b3ef1-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b3ef1-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b3ef1-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b3ef1-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 45f1cac30841498f14050c780be83a4898e52408
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655341"
---
# <span data-ttu-id="e2605-104">interfaz ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e2605-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="e2605-105">La persona que llama implementa esta interfaz para recibir eventos DevToolsProtocolEventReceived de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="e2605-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="e2605-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e2605-106">Summary</span></span>

 <span data-ttu-id="e2605-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e2605-107">Members</span></span>                        | <span data-ttu-id="e2605-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e2605-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e2605-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e2605-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e2605-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e2605-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e2605-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e2605-111">Members</span></span>

#### <span data-ttu-id="e2605-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e2605-112">Invoke</span></span> 

<span data-ttu-id="e2605-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e2605-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e2605-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e2605-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>


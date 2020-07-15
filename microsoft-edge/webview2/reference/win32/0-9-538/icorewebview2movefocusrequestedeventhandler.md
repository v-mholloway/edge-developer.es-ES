---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2MoveFocusRequestedEventHandler
ms.openlocfilehash: b0e7f3f005b90c5656eeeac09716130544b0ee20
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879838"
---
# <span data-ttu-id="e8728-104">interfaz ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e8728-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="e8728-105">La persona que llama implementa este método para recibir el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="e8728-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="e8728-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e8728-106">Summary</span></span>

 <span data-ttu-id="e8728-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e8728-107">Members</span></span>                        | <span data-ttu-id="e8728-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e8728-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e8728-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e8728-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e8728-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e8728-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e8728-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e8728-111">Members</span></span>

#### <span data-ttu-id="e8728-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e8728-112">Invoke</span></span> 

<span data-ttu-id="e8728-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e8728-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e8728-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e8728-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>


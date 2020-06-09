---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: a90e7d3479f93d58d72db5c69cca53669a6d4501
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699347"
---
# <span data-ttu-id="c2310-104">interfaz ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c2310-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="c2310-105">La persona que llama implementa este método para recibir el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="c2310-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="c2310-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="c2310-106">Summary</span></span>

 <span data-ttu-id="c2310-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2310-107">Members</span></span>                        | <span data-ttu-id="c2310-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c2310-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c2310-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c2310-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c2310-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c2310-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c2310-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2310-111">Members</span></span>

#### <span data-ttu-id="c2310-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c2310-112">Invoke</span></span> 

<span data-ttu-id="c2310-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c2310-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c2310-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c2310-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>


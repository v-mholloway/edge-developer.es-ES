---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2FocusChangedEventHandler
ms.openlocfilehash: fc952437a9d5ffa7bb709bb6fb322438851babcd
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879901"
---
# <span data-ttu-id="b28d1-104">interfaz ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b28d1-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="b28d1-105">La persona que llama implementa este método para recibir los eventos GotFocus y LostFocus.</span><span class="sxs-lookup"><span data-stu-id="b28d1-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="b28d1-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="b28d1-106">Summary</span></span>

 <span data-ttu-id="b28d1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b28d1-107">Members</span></span>                        | <span data-ttu-id="b28d1-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b28d1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b28d1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b28d1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b28d1-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b28d1-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="b28d1-111">No hay argumentos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="b28d1-111">There are no event args for this event.</span></span>

## <span data-ttu-id="b28d1-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="b28d1-112">Members</span></span>

#### <span data-ttu-id="b28d1-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="b28d1-113">Invoke</span></span> 

<span data-ttu-id="b28d1-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b28d1-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b28d1-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b28d1-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="b28d1-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="b28d1-116">There are no event args and the args parameter will be null.</span></span>


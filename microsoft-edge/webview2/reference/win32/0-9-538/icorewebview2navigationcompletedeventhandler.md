---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NavigationCompletedEventHandler
ms.openlocfilehash: 7e61f54882d653a28ec31a97c59758eeff300b26
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011268"
---
# <span data-ttu-id="fc7a6-104">0.9.579: ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="fc7a6-104">0.9.579 - interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="fc7a6-105">La persona que llama implementa esta interfaz para recibir el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="fc7a6-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="fc7a6-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="fc7a6-106">Summary</span></span>

 <span data-ttu-id="fc7a6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc7a6-107">Members</span></span>                        | <span data-ttu-id="fc7a6-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="fc7a6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fc7a6-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="fc7a6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="fc7a6-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fc7a6-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="fc7a6-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc7a6-111">Members</span></span>

#### <span data-ttu-id="fc7a6-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="fc7a6-112">Invoke</span></span> 

<span data-ttu-id="fc7a6-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fc7a6-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fc7a6-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="fc7a6-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>


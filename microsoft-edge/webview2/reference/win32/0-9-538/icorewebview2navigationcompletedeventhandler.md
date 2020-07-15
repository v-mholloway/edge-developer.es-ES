---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NavigationCompletedEventHandler
ms.openlocfilehash: 24651585298998eaa42b2be242785de1bf4d6f84
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879796"
---
# <span data-ttu-id="4addb-104">interfaz ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4addb-104">interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="4addb-105">La persona que llama implementa esta interfaz para recibir el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="4addb-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="4addb-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="4addb-106">Summary</span></span>

 <span data-ttu-id="4addb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4addb-107">Members</span></span>                        | <span data-ttu-id="4addb-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="4addb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4addb-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4addb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4addb-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4addb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="4addb-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4addb-111">Members</span></span>

#### <span data-ttu-id="4addb-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="4addb-112">Invoke</span></span> 

<span data-ttu-id="4addb-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4addb-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4addb-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="4addb-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>


---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: cf9d04c14f39a9ba1686d5cc9b002041313b645d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879915"
---
# <span data-ttu-id="b950b-104">interfaz ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b950b-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="b950b-105">La persona que llama implementa esta interfaz para recibir el evento HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="b950b-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="b950b-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="b950b-106">Summary</span></span>

 <span data-ttu-id="b950b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b950b-107">Members</span></span>                        | <span data-ttu-id="b950b-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b950b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b950b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b950b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b950b-110">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="b950b-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="b950b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b950b-111">Members</span></span>

#### <span data-ttu-id="b950b-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b950b-112">Invoke</span></span> 

<span data-ttu-id="b950b-113">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="b950b-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="b950b-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b950b-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>


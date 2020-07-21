---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: d90f461f6c2a1e573b0514213ec34f83f0d23366
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885502"
---
# <span data-ttu-id="4e346-104">0.9.515: ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4e346-104">0.9.515 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="4e346-105">La persona que llama implementa esta interfaz para recibir el evento HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="4e346-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="4e346-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="4e346-106">Summary</span></span>

 <span data-ttu-id="4e346-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e346-107">Members</span></span>                        | <span data-ttu-id="4e346-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="4e346-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4e346-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4e346-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4e346-110">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="4e346-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="4e346-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e346-111">Members</span></span>

#### <span data-ttu-id="4e346-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="4e346-112">Invoke</span></span> 

<span data-ttu-id="4e346-113">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="4e346-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="4e346-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="4e346-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>


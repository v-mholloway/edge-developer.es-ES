---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: e47ca26475ba1b59fa4ea8c87a7aada0d8d6695f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884137"
---
# <span data-ttu-id="5211c-104">0.9.430: ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="5211c-104">0.9.430 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="5211c-105">La persona que llama implementa esta interfaz para recibir el evento HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="5211c-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="5211c-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="5211c-106">Summary</span></span>

 <span data-ttu-id="5211c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5211c-107">Members</span></span>                        | <span data-ttu-id="5211c-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="5211c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5211c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5211c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5211c-110">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="5211c-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="5211c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="5211c-111">Members</span></span>

#### <span data-ttu-id="5211c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="5211c-112">Invoke</span></span> 

<span data-ttu-id="5211c-113">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="5211c-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="5211c-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="5211c-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,IUnknown \* args)</span></span>


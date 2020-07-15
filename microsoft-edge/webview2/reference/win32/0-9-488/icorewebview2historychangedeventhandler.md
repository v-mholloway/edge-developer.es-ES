---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 5c4807a6f1772354f4448b25d49ea7ea86278f57
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880608"
---
# <span data-ttu-id="e9674-104">0.9.515: ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9674-104">0.9.515 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e9674-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="e9674-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e9674-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="e9674-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e9674-107">La persona que llama implementa esta interfaz para recibir el evento HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="e9674-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="e9674-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="e9674-108">Summary</span></span>

 <span data-ttu-id="e9674-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e9674-109">Members</span></span>                        | <span data-ttu-id="e9674-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e9674-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e9674-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="e9674-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e9674-112">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="e9674-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="e9674-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="e9674-113">Members</span></span>

#### <span data-ttu-id="e9674-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="e9674-114">Invoke</span></span> 

<span data-ttu-id="e9674-115">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="e9674-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="e9674-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e9674-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>


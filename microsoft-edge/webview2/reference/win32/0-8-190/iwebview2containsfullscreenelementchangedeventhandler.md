---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: b1d0bf7ea5f472d5a1c3682c2cbef564947ee54b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886188"
---
# <span data-ttu-id="84fe3-104">0.8.355: IWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="84fe3-104">0.8.355 - interface IWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="84fe3-105">La persona que llama implementa este método para recibir los eventos ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="84fe3-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="84fe3-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="84fe3-106">Summary</span></span>

 <span data-ttu-id="84fe3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="84fe3-107">Members</span></span>                        | <span data-ttu-id="84fe3-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="84fe3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="84fe3-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="84fe3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="84fe3-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="84fe3-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="84fe3-111">No hay argumentos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="84fe3-111">There are no event args for this event.</span></span>

## <span data-ttu-id="84fe3-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="84fe3-112">Members</span></span>

#### <span data-ttu-id="84fe3-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="84fe3-113">Invoke</span></span> 

<span data-ttu-id="84fe3-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="84fe3-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="84fe3-115">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView5](IWebView2WebView5.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="84fe3-115">public HRESULT [Invoke](#invoke)([IWebView2WebView5](IWebView2WebView5.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="84fe3-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="84fe3-116">There are no event args and the args parameter will be null.</span></span>


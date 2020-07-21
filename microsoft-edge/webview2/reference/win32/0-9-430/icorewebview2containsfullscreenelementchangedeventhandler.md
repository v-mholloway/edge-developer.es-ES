---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 8afab2e15381c99f5f677b13e539e4b6a9279b63
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884326"
---
# <span data-ttu-id="0486b-104">0.9.430: ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0486b-104">0.9.430 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="0486b-105">La persona que llama implementa este método para recibir los eventos ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="0486b-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="0486b-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="0486b-106">Summary</span></span>

 <span data-ttu-id="0486b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0486b-107">Members</span></span>                        | <span data-ttu-id="0486b-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0486b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0486b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0486b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0486b-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0486b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="0486b-111">No hay argumentos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="0486b-111">There are no event args for this event.</span></span>

## <span data-ttu-id="0486b-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="0486b-112">Members</span></span>

#### <span data-ttu-id="0486b-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="0486b-113">Invoke</span></span> 

<span data-ttu-id="0486b-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0486b-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0486b-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="0486b-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="0486b-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="0486b-116">There are no event args and the args parameter will be null.</span></span>


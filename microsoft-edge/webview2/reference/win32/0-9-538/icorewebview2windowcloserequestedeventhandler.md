---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2WindowCloseRequestedEventHandler
ms.openlocfilehash: 34b0f941029251824cdc108e0aca41e6eab93695
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011382"
---
# <span data-ttu-id="74dfc-104">0.9.579: ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="74dfc-104">0.9.579 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="74dfc-105">La persona que llama implementa esta interfaz para recibir eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="74dfc-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="74dfc-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="74dfc-106">Summary</span></span>

 <span data-ttu-id="74dfc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="74dfc-107">Members</span></span>                        | <span data-ttu-id="74dfc-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="74dfc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="74dfc-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="74dfc-109">Invoke</span></span>](#invoke) | <span data-ttu-id="74dfc-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="74dfc-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="74dfc-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="74dfc-111">Members</span></span>

#### <span data-ttu-id="74dfc-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="74dfc-112">Invoke</span></span> 

<span data-ttu-id="74dfc-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="74dfc-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="74dfc-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="74dfc-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="74dfc-115">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="74dfc-115">There are no event args and the args parameter will be null.</span></span>


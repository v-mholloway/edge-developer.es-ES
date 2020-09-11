---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NewBrowserVersionAvailableEventHandler
ms.openlocfilehash: 5221a08f8da8e0b51bb873a2e312e4012c868528
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012728"
---
# <span data-ttu-id="a301a-104">interfaz ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="a301a-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="a301a-105">La persona que llama implementa esta interfaz para recibir eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="a301a-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="a301a-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="a301a-106">Summary</span></span>

 <span data-ttu-id="a301a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a301a-107">Members</span></span>                        | <span data-ttu-id="a301a-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a301a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a301a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a301a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a301a-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a301a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a301a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a301a-111">Members</span></span>

#### <span data-ttu-id="a301a-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a301a-112">Invoke</span></span> 

<span data-ttu-id="a301a-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a301a-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a301a-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="a301a-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>


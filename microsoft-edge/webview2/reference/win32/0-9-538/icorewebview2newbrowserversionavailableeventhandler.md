---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NewBrowserVersionAvailableEventHandler
ms.openlocfilehash: 82a5e73b8b928897e5c0af1610631c9e7d636337
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879747"
---
# <span data-ttu-id="59a59-104">interfaz ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="59a59-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="59a59-105">La persona que llama implementa esta interfaz para recibir eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="59a59-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="59a59-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="59a59-106">Summary</span></span>

 <span data-ttu-id="59a59-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="59a59-107">Members</span></span>                        | <span data-ttu-id="59a59-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="59a59-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="59a59-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="59a59-109">Invoke</span></span>](#invoke) | <span data-ttu-id="59a59-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="59a59-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="59a59-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="59a59-111">Members</span></span>

#### <span data-ttu-id="59a59-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="59a59-112">Invoke</span></span> 

<span data-ttu-id="59a59-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="59a59-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="59a59-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="59a59-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>


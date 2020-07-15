---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NavigationStartingEventHandler
ms.openlocfilehash: aca4e1090356b2dec147485f0290e1d19869ec63
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879754"
---
# <span data-ttu-id="f377b-104">interfaz ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="f377b-104">interface ICoreWebView2NavigationStartingEventHandler</span></span> 

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="f377b-105">La persona que llama implementa esta interfaz para recibir el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f377b-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="f377b-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="f377b-106">Summary</span></span>

 <span data-ttu-id="f377b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f377b-107">Members</span></span>                        | <span data-ttu-id="f377b-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f377b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f377b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f377b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f377b-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f377b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f377b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f377b-111">Members</span></span>

#### <span data-ttu-id="f377b-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f377b-112">Invoke</span></span> 

<span data-ttu-id="f377b-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f377b-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f377b-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f377b-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span></span>


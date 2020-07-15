---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2WindowCloseRequestedEventHandler
ms.openlocfilehash: fcfdb3b28f4f1d1e1d1159e6664cb898613d0601
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879964"
---
# <span data-ttu-id="8f49a-104">interfaz ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8f49a-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="8f49a-105">La persona que llama implementa esta interfaz para recibir eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="8f49a-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="8f49a-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="8f49a-106">Summary</span></span>

 <span data-ttu-id="8f49a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8f49a-107">Members</span></span>                        | <span data-ttu-id="8f49a-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8f49a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8f49a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="8f49a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8f49a-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8f49a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8f49a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="8f49a-111">Members</span></span>

#### <span data-ttu-id="8f49a-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="8f49a-112">Invoke</span></span> 

<span data-ttu-id="8f49a-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8f49a-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8f49a-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="8f49a-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="8f49a-115">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="8f49a-115">There are no event args and the args parameter will be null.</span></span>


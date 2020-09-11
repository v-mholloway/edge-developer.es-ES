---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2SourceChangedEventHandler
ms.openlocfilehash: 2c174d498843b7cc1d680d58eb36b5f53d652ad3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012717"
---
# <span data-ttu-id="fb731-104">interfaz ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="fb731-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="fb731-105">La persona que llama implementa esta interfaz para recibir el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="fb731-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="fb731-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="fb731-106">Summary</span></span>

 <span data-ttu-id="fb731-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="fb731-107">Members</span></span>                        | <span data-ttu-id="fb731-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="fb731-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fb731-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="fb731-109">Invoke</span></span>](#invoke) | <span data-ttu-id="fb731-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fb731-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="fb731-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="fb731-111">Members</span></span>

#### <span data-ttu-id="fb731-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="fb731-112">Invoke</span></span> 

<span data-ttu-id="fb731-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fb731-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fb731-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="fb731-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>


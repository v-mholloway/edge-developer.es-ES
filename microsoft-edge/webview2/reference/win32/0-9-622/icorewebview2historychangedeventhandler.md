---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: 909b055af0f9594bb3c85b215cb8e02f13606aa0
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012692"
---
# <span data-ttu-id="124ba-104">interfaz ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="124ba-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="124ba-105">La persona que llama implementa esta interfaz para recibir el evento HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="124ba-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="124ba-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="124ba-106">Summary</span></span>

 <span data-ttu-id="124ba-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="124ba-107">Members</span></span>                        | <span data-ttu-id="124ba-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="124ba-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="124ba-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="124ba-109">Invoke</span></span>](#invoke) | <span data-ttu-id="124ba-110">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="124ba-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="124ba-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="124ba-111">Members</span></span>

#### <span data-ttu-id="124ba-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="124ba-112">Invoke</span></span> 

<span data-ttu-id="124ba-113">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="124ba-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="124ba-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="124ba-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>


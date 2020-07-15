---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2DocumentTitleChangedEventHandler
ms.openlocfilehash: 6ea83bb610ff3348e361a7628f31aa022c3a62e9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879544"
---
# <span data-ttu-id="94c25-104">interfaz ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="94c25-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="94c25-105">La persona que llama implementa esta interfaz para recibir eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="94c25-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="94c25-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="94c25-106">Summary</span></span>

 <span data-ttu-id="94c25-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="94c25-107">Members</span></span>                        | <span data-ttu-id="94c25-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="94c25-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="94c25-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="94c25-109">Invoke</span></span>](#invoke) | <span data-ttu-id="94c25-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="94c25-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="94c25-111">Use la propiedad DocumentTitle para obtener el título modificado.</span><span class="sxs-lookup"><span data-stu-id="94c25-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="94c25-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="94c25-112">Members</span></span>

#### <span data-ttu-id="94c25-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="94c25-113">Invoke</span></span> 

<span data-ttu-id="94c25-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="94c25-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="94c25-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="94c25-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="94c25-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="94c25-116">There are no event args and the args parameter will be null.</span></span>


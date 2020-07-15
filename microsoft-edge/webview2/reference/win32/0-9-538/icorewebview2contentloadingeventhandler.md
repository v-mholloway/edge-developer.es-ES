---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ContentLoadingEventHandler
ms.openlocfilehash: fb6e3cfabae0116ac746d6e8e5cc03efa0f1c1b6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877450"
---
# <span data-ttu-id="c9244-104">interfaz ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="c9244-104">interface ICoreWebView2ContentLoadingEventHandler</span></span> 

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="c9244-105">La persona que llama implementa esta interfaz para recibir el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="c9244-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="c9244-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="c9244-106">Summary</span></span>

 <span data-ttu-id="c9244-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c9244-107">Members</span></span>                        | <span data-ttu-id="c9244-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c9244-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c9244-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c9244-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c9244-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c9244-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c9244-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c9244-111">Members</span></span>

#### <span data-ttu-id="c9244-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c9244-112">Invoke</span></span> 

<span data-ttu-id="c9244-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c9244-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c9244-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c9244-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>


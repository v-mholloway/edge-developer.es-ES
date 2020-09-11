---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ContentLoadingEventHandler
ms.openlocfilehash: 906b09ad99d6d6d9e74c52c0582584b9e46f74ba
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010540"
---
# <span data-ttu-id="6e631-104">0.9.579: ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="6e631-104">0.9.579 - interface ICoreWebView2ContentLoadingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="6e631-105">La persona que llama implementa esta interfaz para recibir el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="6e631-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="6e631-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6e631-106">Summary</span></span>

 <span data-ttu-id="6e631-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6e631-107">Members</span></span>                        | <span data-ttu-id="6e631-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6e631-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6e631-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6e631-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6e631-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6e631-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="6e631-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="6e631-111">Members</span></span>

#### <span data-ttu-id="6e631-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="6e631-112">Invoke</span></span> 

<span data-ttu-id="6e631-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6e631-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6e631-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="6e631-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>


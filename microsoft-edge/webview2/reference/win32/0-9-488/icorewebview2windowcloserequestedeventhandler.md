---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 9163eb811e018e346f610dae71d5fdb7e39de186
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885439"
---
# <span data-ttu-id="b8760-104">0.9.515: ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b8760-104">0.9.515 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="b8760-105">La persona que llama implementa esta interfaz para recibir eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="b8760-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="b8760-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="b8760-106">Summary</span></span>

 <span data-ttu-id="b8760-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8760-107">Members</span></span>                        | <span data-ttu-id="b8760-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b8760-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b8760-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b8760-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b8760-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b8760-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b8760-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8760-111">Members</span></span>

#### <span data-ttu-id="b8760-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b8760-112">Invoke</span></span> 

<span data-ttu-id="b8760-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b8760-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b8760-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b8760-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="b8760-115">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="b8760-115">There are no event args and the args parameter will be null.</span></span>


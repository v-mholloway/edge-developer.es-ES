---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 45f9b638347d096ce89c9fcaac1bfb7e904ebee9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886300"
---
# <span data-ttu-id="dfe2f-104">0.9.515: ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="dfe2f-104">0.9.515 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="dfe2f-105">La persona que llama implementa este método para recibir el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="dfe2f-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="dfe2f-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="dfe2f-106">Summary</span></span>

 <span data-ttu-id="dfe2f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="dfe2f-107">Members</span></span>                        | <span data-ttu-id="dfe2f-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="dfe2f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dfe2f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="dfe2f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="dfe2f-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="dfe2f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="dfe2f-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="dfe2f-111">Members</span></span>

#### <span data-ttu-id="dfe2f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="dfe2f-112">Invoke</span></span> 

<span data-ttu-id="dfe2f-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="dfe2f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="dfe2f-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="dfe2f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 6b7d48fbec0c3bb0008f0f429bf6414ed855a09f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884795"
---
# <span data-ttu-id="a194a-104">0.9.515: ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a194a-104">0.9.515 - interface ICoreWebView2ProcessFailedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="a194a-105">La persona que llama implementa esta interfaz para recibir eventos ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="a194a-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="a194a-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="a194a-106">Summary</span></span>

 <span data-ttu-id="a194a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a194a-107">Members</span></span>                        | <span data-ttu-id="a194a-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a194a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a194a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a194a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a194a-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a194a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a194a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a194a-111">Members</span></span>

#### <span data-ttu-id="a194a-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a194a-112">Invoke</span></span> 

<span data-ttu-id="a194a-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a194a-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a194a-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a194a-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>


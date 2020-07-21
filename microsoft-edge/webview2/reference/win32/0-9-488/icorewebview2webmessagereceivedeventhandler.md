---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: b69854163a45c09d605cac2f544866d58546c71b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885187"
---
# <span data-ttu-id="b4784-104">0.9.515: ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b4784-104">0.9.515 - interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="b4784-105">La persona que llama implementa esta interfaz para recibir el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="b4784-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="b4784-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="b4784-106">Summary</span></span>

 <span data-ttu-id="b4784-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b4784-107">Members</span></span>                        | <span data-ttu-id="b4784-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b4784-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b4784-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b4784-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b4784-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b4784-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b4784-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b4784-111">Members</span></span>

#### <span data-ttu-id="b4784-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b4784-112">Invoke</span></span> 

<span data-ttu-id="b4784-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b4784-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b4784-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b4784-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>


---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2MoveFocusRequestedEventHandler
ms.openlocfilehash: 89b1e7fada56bcf535ae07be109acbb340fdc9a8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012657"
---
# <span data-ttu-id="4c079-104">interfaz ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4c079-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="4c079-105">La persona que llama implementa este método para recibir el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="4c079-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="4c079-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="4c079-106">Summary</span></span>

 <span data-ttu-id="4c079-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4c079-107">Members</span></span>                        | <span data-ttu-id="4c079-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="4c079-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4c079-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4c079-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4c079-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4c079-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="4c079-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4c079-111">Members</span></span>

#### <span data-ttu-id="4c079-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="4c079-112">Invoke</span></span> 

<span data-ttu-id="4c079-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4c079-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4c079-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="4c079-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>


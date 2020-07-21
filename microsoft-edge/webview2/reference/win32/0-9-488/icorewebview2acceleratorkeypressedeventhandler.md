---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 13538c0ef14b9517a8a53e00d24ef93819adeb15
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883976"
---
# <span data-ttu-id="6a31d-104">0.9.515: ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6a31d-104">0.9.515 - interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="6a31d-105">La persona que llama implementa esta interfaz para recibir el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="6a31d-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="6a31d-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6a31d-106">Summary</span></span>

 <span data-ttu-id="6a31d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6a31d-107">Members</span></span>                        | <span data-ttu-id="6a31d-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6a31d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6a31d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6a31d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6a31d-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6a31d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="6a31d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="6a31d-111">Members</span></span>

#### <span data-ttu-id="6a31d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="6a31d-112">Invoke</span></span> 

<span data-ttu-id="6a31d-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6a31d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6a31d-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="6a31d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>


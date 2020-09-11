---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2AcceleratorKeyPressedEventHandler
ms.openlocfilehash: 15ad3a4afb76ea8068066097340af204b45fe416
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012743"
---
# <span data-ttu-id="c96c1-104">interfaz ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c96c1-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="c96c1-105">La persona que llama implementa esta interfaz para recibir el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="c96c1-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="c96c1-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="c96c1-106">Summary</span></span>

 <span data-ttu-id="c96c1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c96c1-107">Members</span></span>                        | <span data-ttu-id="c96c1-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c96c1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c96c1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c96c1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c96c1-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c96c1-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c96c1-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c96c1-111">Members</span></span>

#### <span data-ttu-id="c96c1-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c96c1-112">Invoke</span></span> 

<span data-ttu-id="c96c1-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c96c1-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c96c1-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c96c1-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>


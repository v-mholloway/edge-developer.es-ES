---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ProcessFailedEventHandler
ms.openlocfilehash: 98f3f092bc1feb75ea2f94857c31dd80bcb907ee
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012719"
---
# <span data-ttu-id="d1f85-104">interfaz ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d1f85-104">interface ICoreWebView2ProcessFailedEventHandler</span></span> 

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="d1f85-105">La persona que llama implementa esta interfaz para recibir eventos ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d1f85-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="d1f85-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="d1f85-106">Summary</span></span>

 <span data-ttu-id="d1f85-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1f85-107">Members</span></span>                        | <span data-ttu-id="d1f85-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d1f85-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d1f85-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d1f85-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d1f85-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d1f85-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d1f85-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1f85-111">Members</span></span>

#### <span data-ttu-id="d1f85-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="d1f85-112">Invoke</span></span> 

<span data-ttu-id="d1f85-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d1f85-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d1f85-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d1f85-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>


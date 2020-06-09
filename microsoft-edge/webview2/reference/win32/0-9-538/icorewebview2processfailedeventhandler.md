---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 2c109e02de28101c88ea55d849db5701f36795a9
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699333"
---
# <span data-ttu-id="d46c3-104">interfaz ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d46c3-104">interface ICoreWebView2ProcessFailedEventHandler</span></span> 

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="d46c3-105">La persona que llama implementa esta interfaz para recibir eventos ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d46c3-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="d46c3-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="d46c3-106">Summary</span></span>

 <span data-ttu-id="d46c3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d46c3-107">Members</span></span>                        | <span data-ttu-id="d46c3-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d46c3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d46c3-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d46c3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d46c3-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d46c3-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d46c3-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="d46c3-111">Members</span></span>

#### <span data-ttu-id="d46c3-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="d46c3-112">Invoke</span></span> 

<span data-ttu-id="d46c3-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d46c3-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d46c3-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d46c3-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>


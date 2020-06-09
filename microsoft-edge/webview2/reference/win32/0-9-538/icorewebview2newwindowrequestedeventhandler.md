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
ms.openlocfilehash: a39eeadaf1243d57223f3739dce836b1db998998
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699303"
---
# <span data-ttu-id="f7694-104">interfaz ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f7694-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="f7694-105">La persona que llama implementa esta interfaz para recibir eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f7694-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="f7694-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="f7694-106">Summary</span></span>

 <span data-ttu-id="f7694-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f7694-107">Members</span></span>                        | <span data-ttu-id="f7694-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f7694-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f7694-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f7694-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f7694-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f7694-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f7694-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f7694-111">Members</span></span>

#### <span data-ttu-id="f7694-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f7694-112">Invoke</span></span> 

<span data-ttu-id="f7694-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f7694-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f7694-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f7694-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>


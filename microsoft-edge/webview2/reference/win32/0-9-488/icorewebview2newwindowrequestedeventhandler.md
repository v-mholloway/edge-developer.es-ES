---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: a8cd4dd948aa00aca7c2ef7d8c0c744b30db37e3
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655323"
---
# <span data-ttu-id="57e75-104">interfaz ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="57e75-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="57e75-105">La persona que llama implementa esta interfaz para recibir eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="57e75-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="57e75-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="57e75-106">Summary</span></span>

 <span data-ttu-id="57e75-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="57e75-107">Members</span></span>                        | <span data-ttu-id="57e75-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="57e75-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="57e75-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="57e75-109">Invoke</span></span>](#invoke) | <span data-ttu-id="57e75-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="57e75-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="57e75-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="57e75-111">Members</span></span>

#### <span data-ttu-id="57e75-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="57e75-112">Invoke</span></span> 

<span data-ttu-id="57e75-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="57e75-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="57e75-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="57e75-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>


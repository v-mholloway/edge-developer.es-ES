---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: ec9edbacc3a2968a3ab7db94b8b05fbb2aaf7763
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880468"
---
# <span data-ttu-id="007b8-104">0.9.515: ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="007b8-104">0.9.515 - interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="007b8-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="007b8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="007b8-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="007b8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="007b8-107">La persona que llama implementa esta interfaz para recibir eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="007b8-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="007b8-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="007b8-108">Summary</span></span>

 <span data-ttu-id="007b8-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="007b8-109">Members</span></span>                        | <span data-ttu-id="007b8-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="007b8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="007b8-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="007b8-111">Invoke</span></span>](#invoke) | <span data-ttu-id="007b8-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="007b8-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="007b8-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="007b8-113">Members</span></span>

#### <span data-ttu-id="007b8-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="007b8-114">Invoke</span></span> 

<span data-ttu-id="007b8-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="007b8-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="007b8-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="007b8-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>


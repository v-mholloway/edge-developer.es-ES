---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 8381e82d3c0daa33349fa97171b077517830d527
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880460"
---
# <span data-ttu-id="5f3d9-104">0.9.515: ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="5f3d9-104">0.9.515 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="5f3d9-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="5f3d9-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="5f3d9-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="5f3d9-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="5f3d9-107">La persona que llama implementa esta interfaz para recibir eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="5f3d9-107">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="5f3d9-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="5f3d9-108">Summary</span></span>

 <span data-ttu-id="5f3d9-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5f3d9-109">Members</span></span>                        | <span data-ttu-id="5f3d9-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="5f3d9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5f3d9-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="5f3d9-111">Invoke</span></span>](#invoke) | <span data-ttu-id="5f3d9-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5f3d9-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="5f3d9-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="5f3d9-113">Members</span></span>

#### <span data-ttu-id="5f3d9-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="5f3d9-114">Invoke</span></span> 

<span data-ttu-id="5f3d9-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5f3d9-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5f3d9-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="5f3d9-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 5ff441c65970f603011db1bbe93822a54c2a5bf6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878473"
---
# <span data-ttu-id="866f0-104">0.8.355: IWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="866f0-104">0.8.355 - interface IWebView2MoveFocusRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="866f0-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="866f0-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="866f0-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="866f0-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="866f0-107">La persona que llama implementa este método para recibir el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="866f0-107">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="866f0-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="866f0-108">Summary</span></span>

 <span data-ttu-id="866f0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="866f0-109">Members</span></span>                        | <span data-ttu-id="866f0-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="866f0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="866f0-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="866f0-111">Invoke</span></span>](#invoke) | <span data-ttu-id="866f0-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="866f0-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="866f0-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="866f0-113">Members</span></span>

#### <span data-ttu-id="866f0-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="866f0-114">Invoke</span></span> 

<span data-ttu-id="866f0-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="866f0-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="866f0-116">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="866f0-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>


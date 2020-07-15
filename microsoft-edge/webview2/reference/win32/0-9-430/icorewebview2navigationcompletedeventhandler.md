---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: f6746b25f32e1141f5314e96b2012851fd1a7dd2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877954"
---
# <span data-ttu-id="9e370-104">0.9.430: ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9e370-104">0.9.430 - interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="9e370-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="9e370-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="9e370-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="9e370-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="9e370-107">La persona que llama implementa esta interfaz para recibir el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9e370-107">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="9e370-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="9e370-108">Summary</span></span>

 <span data-ttu-id="9e370-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e370-109">Members</span></span>                        | <span data-ttu-id="9e370-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9e370-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9e370-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="9e370-111">Invoke</span></span>](#invoke) | <span data-ttu-id="9e370-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9e370-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="9e370-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e370-113">Members</span></span>

#### <span data-ttu-id="9e370-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="9e370-114">Invoke</span></span> 

<span data-ttu-id="9e370-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9e370-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9e370-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2NavigationCompletedEventArgs](ICoreWebView2NavigationCompletedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="9e370-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationCompletedEventArgs](ICoreWebView2NavigationCompletedEventArgs.md) \* args)</span></span>


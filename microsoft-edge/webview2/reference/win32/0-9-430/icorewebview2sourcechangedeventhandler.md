---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 1e3e9d3f661a6e0643d7094c9127fdf33501624a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880181"
---
# <span data-ttu-id="e0c34-104">0.9.430: ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e0c34-104">0.9.430 - interface ICoreWebView2SourceChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e0c34-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="e0c34-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="e0c34-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="e0c34-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e0c34-107">La persona que llama implementa esta interfaz para recibir el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="e0c34-107">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="e0c34-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="e0c34-108">Summary</span></span>

 <span data-ttu-id="e0c34-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e0c34-109">Members</span></span>                        | <span data-ttu-id="e0c34-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e0c34-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e0c34-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="e0c34-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e0c34-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e0c34-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e0c34-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="e0c34-113">Members</span></span>

#### <span data-ttu-id="e0c34-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="e0c34-114">Invoke</span></span> 

<span data-ttu-id="e0c34-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e0c34-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e0c34-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* WebView,[ICoreWebView2SourceChangedEventArgs](ICoreWebView2SourceChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e0c34-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,[ICoreWebView2SourceChangedEventArgs](ICoreWebView2SourceChangedEventArgs.md) \* args)</span></span>


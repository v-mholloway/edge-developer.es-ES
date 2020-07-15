---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 9e8b1cc973eefbd41c1fac0d7d9723ba35ec7302
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878683"
---
# <span data-ttu-id="fa664-104">0.8.355: IWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="fa664-104">0.8.355 - interface IWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="fa664-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="fa664-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="fa664-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="fa664-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="fa664-107">La persona que llama implementa este método para recibir el resultado del método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="fa664-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="fa664-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="fa664-108">Summary</span></span>

 <span data-ttu-id="fa664-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fa664-109">Members</span></span>                        | <span data-ttu-id="fa664-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="fa664-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fa664-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="fa664-111">Invoke</span></span>](#invoke) | <span data-ttu-id="fa664-112">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fa664-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="fa664-113">El resultado se escribe en la secuencia proporcionada en la llamada al método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="fa664-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="fa664-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="fa664-114">Members</span></span>

#### <span data-ttu-id="fa664-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="fa664-115">Invoke</span></span> 

<span data-ttu-id="fa664-116">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fa664-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="fa664-117">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="fa664-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


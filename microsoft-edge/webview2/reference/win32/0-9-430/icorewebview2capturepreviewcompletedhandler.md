---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 321aff5097783391e4596c22dbd5cb906e45dace
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881161"
---
# <span data-ttu-id="6851c-104">0.9.430: ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="6851c-104">0.9.430 - interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="6851c-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="6851c-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="6851c-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="6851c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6851c-107">La persona que llama implementa este método para recibir el resultado del método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="6851c-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="6851c-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="6851c-108">Summary</span></span>

 <span data-ttu-id="6851c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6851c-109">Members</span></span>                        | <span data-ttu-id="6851c-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6851c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6851c-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="6851c-111">Invoke</span></span>](#invoke) | <span data-ttu-id="6851c-112">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6851c-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="6851c-113">El resultado se escribe en la secuencia proporcionada en la llamada al método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="6851c-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="6851c-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="6851c-114">Members</span></span>

#### <span data-ttu-id="6851c-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="6851c-115">Invoke</span></span> 

<span data-ttu-id="6851c-116">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6851c-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6851c-117">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="6851c-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


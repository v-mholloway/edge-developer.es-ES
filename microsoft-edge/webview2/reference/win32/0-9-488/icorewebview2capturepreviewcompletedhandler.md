---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 6aaac0d062d0e97d3ec0c87bec243c5cf682ad6f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697052"
---
# <span data-ttu-id="68b91-104">interfaz ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="68b91-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="68b91-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="68b91-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="68b91-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="68b91-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="68b91-107">La persona que llama implementa este método para recibir el resultado del método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="68b91-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="68b91-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="68b91-108">Summary</span></span>

 <span data-ttu-id="68b91-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="68b91-109">Members</span></span>                        | <span data-ttu-id="68b91-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="68b91-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="68b91-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="68b91-111">Invoke</span></span>](#invoke) | <span data-ttu-id="68b91-112">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="68b91-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="68b91-113">El resultado se escribe en la secuencia proporcionada en la llamada al método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="68b91-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="68b91-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="68b91-114">Members</span></span>

#### <span data-ttu-id="68b91-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="68b91-115">Invoke</span></span> 

<span data-ttu-id="68b91-116">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="68b91-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="68b91-117">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="68b91-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


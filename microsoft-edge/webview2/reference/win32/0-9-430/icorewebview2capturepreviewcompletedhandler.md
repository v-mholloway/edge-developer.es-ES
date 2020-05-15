---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 06f7f664acb5f169215b603841d935730532b62b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655247"
---
# <span data-ttu-id="b7a00-104">interfaz ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b7a00-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="b7a00-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="b7a00-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="b7a00-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="b7a00-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b7a00-107">La persona que llama implementa este método para recibir el resultado del método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="b7a00-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="b7a00-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="b7a00-108">Summary</span></span>

 <span data-ttu-id="b7a00-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7a00-109">Members</span></span>                        | <span data-ttu-id="b7a00-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b7a00-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b7a00-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="b7a00-111">Invoke</span></span>](#invoke) | <span data-ttu-id="b7a00-112">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b7a00-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="b7a00-113">El resultado se escribe en la secuencia proporcionada en la llamada al método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="b7a00-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="b7a00-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7a00-114">Members</span></span>

#### <span data-ttu-id="b7a00-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="b7a00-115">Invoke</span></span> 

<span data-ttu-id="b7a00-116">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b7a00-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b7a00-117">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="b7a00-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


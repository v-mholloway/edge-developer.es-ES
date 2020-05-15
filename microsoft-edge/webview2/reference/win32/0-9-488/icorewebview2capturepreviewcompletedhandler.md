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
ms.openlocfilehash: 793dbde462e25ae0bfe0dc0bc475cc49e7237fb2
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655368"
---
# <span data-ttu-id="af11b-104">interfaz ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="af11b-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="af11b-105">La persona que llama implementa este método para recibir el resultado del método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="af11b-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="af11b-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="af11b-106">Summary</span></span>

 <span data-ttu-id="af11b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="af11b-107">Members</span></span>                        | <span data-ttu-id="af11b-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="af11b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="af11b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="af11b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="af11b-110">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="af11b-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="af11b-111">El resultado se escribe en la secuencia proporcionada en la llamada al método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="af11b-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="af11b-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="af11b-112">Members</span></span>

#### <span data-ttu-id="af11b-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="af11b-113">Invoke</span></span> 

<span data-ttu-id="af11b-114">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="af11b-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="af11b-115">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="af11b-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


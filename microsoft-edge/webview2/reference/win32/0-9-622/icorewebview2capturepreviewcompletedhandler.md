---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: e526b723f111d7212a5da4b25840c89b69eb2e52
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012588"
---
# <span data-ttu-id="001dd-104">interfaz ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="001dd-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="001dd-105">La persona que llama implementa este método para recibir el resultado del método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="001dd-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="001dd-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="001dd-106">Summary</span></span>

 <span data-ttu-id="001dd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="001dd-107">Members</span></span>                        | <span data-ttu-id="001dd-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="001dd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="001dd-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="001dd-109">Invoke</span></span>](#invoke) | <span data-ttu-id="001dd-110">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="001dd-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="001dd-111">El resultado se escribe en la secuencia proporcionada en la llamada al método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="001dd-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="001dd-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="001dd-112">Members</span></span>

#### <span data-ttu-id="001dd-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="001dd-113">Invoke</span></span> 

<span data-ttu-id="001dd-114">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="001dd-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="001dd-115">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ErrorCode)</span><span class="sxs-lookup"><span data-stu-id="001dd-115">public HRESULT [Invoke](#invoke)(HRESULT errorCode)</span></span>


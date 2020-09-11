---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: 96fff3ab67331bf5a8cf8323af5dddbca04f9e0e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010568"
---
# <span data-ttu-id="16b5b-104">0.9.579: ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="16b5b-104">0.9.579 - interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="16b5b-105">La persona que llama implementa este método para recibir el resultado del método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="16b5b-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="16b5b-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="16b5b-106">Summary</span></span>

 <span data-ttu-id="16b5b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="16b5b-107">Members</span></span>                        | <span data-ttu-id="16b5b-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="16b5b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="16b5b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="16b5b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="16b5b-110">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="16b5b-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="16b5b-111">El resultado se escribe en la secuencia proporcionada en la llamada al método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="16b5b-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="16b5b-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="16b5b-112">Members</span></span>

#### <span data-ttu-id="16b5b-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="16b5b-113">Invoke</span></span> 

<span data-ttu-id="16b5b-114">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="16b5b-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="16b5b-115">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="16b5b-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


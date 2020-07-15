---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: 013a7076648b93bf259d28422f418365d988a586
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877443"
---
# <span data-ttu-id="5755c-104">interfaz ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="5755c-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="5755c-105">La persona que llama implementa este método para recibir el resultado del método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="5755c-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="5755c-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="5755c-106">Summary</span></span>

 <span data-ttu-id="5755c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5755c-107">Members</span></span>                        | <span data-ttu-id="5755c-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="5755c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5755c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5755c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5755c-110">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5755c-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="5755c-111">El resultado se escribe en la secuencia proporcionada en la llamada al método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="5755c-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="5755c-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="5755c-112">Members</span></span>

#### <span data-ttu-id="5755c-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="5755c-113">Invoke</span></span> 

<span data-ttu-id="5755c-114">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5755c-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="5755c-115">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="5755c-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


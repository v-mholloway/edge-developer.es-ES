---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 290d82666e5b9c5062132e1eb7515e39e2deb978
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699381"
---
# <span data-ttu-id="d1dad-104">interfaz ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="d1dad-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="d1dad-105">La persona que llama implementa este método para recibir el resultado del método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="d1dad-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="d1dad-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="d1dad-106">Summary</span></span>

 <span data-ttu-id="d1dad-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1dad-107">Members</span></span>                        | <span data-ttu-id="d1dad-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d1dad-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d1dad-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d1dad-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d1dad-110">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d1dad-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="d1dad-111">El resultado se escribe en la secuencia proporcionada en la llamada al método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="d1dad-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="d1dad-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1dad-112">Members</span></span>

#### <span data-ttu-id="d1dad-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="d1dad-113">Invoke</span></span> 

<span data-ttu-id="d1dad-114">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d1dad-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="d1dad-115">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="d1dad-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 7e7a4173cec86cd6278d53074bff6a6e51b82710
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884319"
---
# <span data-ttu-id="96239-104">0.9.430: ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="96239-104">0.9.430 - interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="96239-105">La persona que llama implementa este método para recibir el resultado del método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="96239-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="96239-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="96239-106">Summary</span></span>

 <span data-ttu-id="96239-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="96239-107">Members</span></span>                        | <span data-ttu-id="96239-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="96239-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="96239-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="96239-109">Invoke</span></span>](#invoke) | <span data-ttu-id="96239-110">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="96239-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="96239-111">El resultado se escribe en la secuencia proporcionada en la llamada al método CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="96239-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="96239-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="96239-112">Members</span></span>

#### <span data-ttu-id="96239-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="96239-113">Invoke</span></span> 

<span data-ttu-id="96239-114">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="96239-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="96239-115">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="96239-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


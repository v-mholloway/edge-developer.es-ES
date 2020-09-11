---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: 6a854eb9ca73f45e366edfa144c273f780bcee94
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011415"
---
# <span data-ttu-id="5fd91-104">0.9.579: ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="5fd91-104">0.9.579 - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="5fd91-105">Controlador de finalización de PopulateResponseContent Async.</span><span class="sxs-lookup"><span data-stu-id="5fd91-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="5fd91-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="5fd91-106">Summary</span></span>

 <span data-ttu-id="5fd91-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5fd91-107">Members</span></span>                        | <span data-ttu-id="5fd91-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="5fd91-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5fd91-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5fd91-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5fd91-110">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5fd91-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="5fd91-111">Se invoca cuando la secuencia de contenido de la respuesta de un evento WebResourceResponseReceieved está disponible.</span><span class="sxs-lookup"><span data-stu-id="5fd91-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="5fd91-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="5fd91-112">Members</span></span>

#### <span data-ttu-id="5fd91-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="5fd91-113">Invoke</span></span> 

<span data-ttu-id="5fd91-114">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5fd91-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="5fd91-115">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="5fd91-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


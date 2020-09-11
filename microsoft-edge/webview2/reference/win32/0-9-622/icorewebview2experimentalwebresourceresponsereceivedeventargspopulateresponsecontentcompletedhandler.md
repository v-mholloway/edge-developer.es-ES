---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: 6c97e0591d55570f4076f6a5c4f2eebc2cc7c5ad
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012612"
---
# <span data-ttu-id="0f265-104">interfaz ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="0f265-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="0f265-105">Controlador de finalización de PopulateResponseContent Async.</span><span class="sxs-lookup"><span data-stu-id="0f265-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="0f265-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="0f265-106">Summary</span></span>

 <span data-ttu-id="0f265-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f265-107">Members</span></span>                        | <span data-ttu-id="0f265-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0f265-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0f265-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0f265-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0f265-110">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0f265-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="0f265-111">Se invoca cuando la secuencia de contenido de la respuesta de un evento WebResourceResponseReceieved está disponible.</span><span class="sxs-lookup"><span data-stu-id="0f265-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="0f265-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f265-112">Members</span></span>

#### <span data-ttu-id="0f265-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="0f265-113">Invoke</span></span> 

<span data-ttu-id="0f265-114">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0f265-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="0f265-115">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ErrorCode)</span><span class="sxs-lookup"><span data-stu-id="0f265-115">public HRESULT [Invoke](#invoke)(HRESULT errorCode)</span></span>


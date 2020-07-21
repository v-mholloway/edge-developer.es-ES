---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: c021cfa866e55bfdf30185eeaf6015db1b523271
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886569"
---
# <span data-ttu-id="0cd7e-104">interfaz ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="0cd7e-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="0cd7e-105">Controlador de finalización de PopulateResponseContent Async.</span><span class="sxs-lookup"><span data-stu-id="0cd7e-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="0cd7e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="0cd7e-106">Summary</span></span>

 <span data-ttu-id="0cd7e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0cd7e-107">Members</span></span>                        | <span data-ttu-id="0cd7e-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0cd7e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0cd7e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0cd7e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0cd7e-110">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0cd7e-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="0cd7e-111">Se invoca cuando la secuencia de contenido de la respuesta de un evento WebResourceResponseReceieved está disponible.</span><span class="sxs-lookup"><span data-stu-id="0cd7e-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="0cd7e-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="0cd7e-112">Members</span></span>

#### <span data-ttu-id="0cd7e-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="0cd7e-113">Invoke</span></span> 

<span data-ttu-id="0cd7e-114">Se llama para proporcionar al implementador el estado de finalización de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0cd7e-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="0cd7e-115">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT)</span><span class="sxs-lookup"><span data-stu-id="0cd7e-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


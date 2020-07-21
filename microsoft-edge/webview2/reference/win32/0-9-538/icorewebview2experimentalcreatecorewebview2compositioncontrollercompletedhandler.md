---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: ab811f717c90ce77293c74a0e54bd3a66c896e72
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885271"
---
# <span data-ttu-id="6fb87-104">interfaz ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="6fb87-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6fb87-105">La persona que llama implementa esta interfaz para recibir el CoreWebView2Controller creado a través de CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="6fb87-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="6fb87-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6fb87-106">Summary</span></span>

 <span data-ttu-id="6fb87-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6fb87-107">Members</span></span>                        | <span data-ttu-id="6fb87-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6fb87-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6fb87-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6fb87-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6fb87-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6fb87-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="6fb87-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="6fb87-111">Members</span></span>

#### <span data-ttu-id="6fb87-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="6fb87-112">Invoke</span></span> 

<span data-ttu-id="6fb87-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6fb87-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6fb87-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="6fb87-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>


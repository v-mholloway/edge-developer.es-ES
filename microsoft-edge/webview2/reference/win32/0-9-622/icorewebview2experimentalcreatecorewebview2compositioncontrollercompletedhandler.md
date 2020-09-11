---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: fd762c994d4c42e5e92dec09add2aa3b85b0ec80
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012651"
---
# <span data-ttu-id="9236d-104">interfaz ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="9236d-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="9236d-105">La persona que llama implementa esta interfaz para recibir el CoreWebView2Controller creado a través de CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="9236d-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="9236d-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="9236d-106">Summary</span></span>

 <span data-ttu-id="9236d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9236d-107">Members</span></span>                        | <span data-ttu-id="9236d-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9236d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9236d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9236d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9236d-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9236d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="9236d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="9236d-111">Members</span></span>

#### <span data-ttu-id="9236d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9236d-112">Invoke</span></span> 

<span data-ttu-id="9236d-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9236d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="9236d-114">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ErrorCode, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="9236d-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>


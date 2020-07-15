---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: 898b76b1865cbda1909fa710707019582439db93
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879999"
---
# <span data-ttu-id="0c4bf-104">interfaz ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="0c4bf-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="0c4bf-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="0c4bf-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="0c4bf-106">La persona que llama implementa esta interfaz para recibir el CoreWebView2Controller creado a través de CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="0c4bf-106">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="0c4bf-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="0c4bf-107">Summary</span></span>

 <span data-ttu-id="0c4bf-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c4bf-108">Members</span></span>                        | <span data-ttu-id="0c4bf-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0c4bf-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0c4bf-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="0c4bf-110">Invoke</span></span>](#invoke) | <span data-ttu-id="0c4bf-111">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0c4bf-111">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="0c4bf-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c4bf-112">Members</span></span>

#### <span data-ttu-id="0c4bf-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="0c4bf-113">Invoke</span></span> 

<span data-ttu-id="0c4bf-114">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0c4bf-114">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="0c4bf-115">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="0c4bf-115">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 9aa9a18701621ca78b74b12340ef5132953fbd2b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880671"
---
# <span data-ttu-id="fc07f-104">0.9.515: ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="fc07f-104">0.9.515 - interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="fc07f-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="fc07f-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="fc07f-106">La persona que llama implementa esta interfaz para recibir el CoreWebView2Controller creado a través de CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="fc07f-106">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="fc07f-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="fc07f-107">Summary</span></span>

 <span data-ttu-id="fc07f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc07f-108">Members</span></span>                        | <span data-ttu-id="fc07f-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="fc07f-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fc07f-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="fc07f-110">Invoke</span></span>](#invoke) | <span data-ttu-id="fc07f-111">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fc07f-111">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="fc07f-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc07f-112">Members</span></span>

#### <span data-ttu-id="fc07f-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="fc07f-113">Invoke</span></span> 

<span data-ttu-id="fc07f-114">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fc07f-114">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="fc07f-115">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="fc07f-115">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>


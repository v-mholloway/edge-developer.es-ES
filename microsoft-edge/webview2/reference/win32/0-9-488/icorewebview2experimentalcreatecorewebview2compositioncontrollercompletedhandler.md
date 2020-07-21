---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: f2598d40afc7c7def1c3fec634016f1a64905479
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885670"
---
# <span data-ttu-id="bad76-104">0.9.515: ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="bad76-104">0.9.515 - interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="bad76-105">La persona que llama implementa esta interfaz para recibir el CoreWebView2Controller creado a través de CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="bad76-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="bad76-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="bad76-106">Summary</span></span>

 <span data-ttu-id="bad76-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bad76-107">Members</span></span>                        | <span data-ttu-id="bad76-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="bad76-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bad76-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="bad76-109">Invoke</span></span>](#invoke) | <span data-ttu-id="bad76-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bad76-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="bad76-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="bad76-111">Members</span></span>

#### <span data-ttu-id="bad76-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="bad76-112">Invoke</span></span> 

<span data-ttu-id="bad76-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bad76-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="bad76-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="bad76-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>


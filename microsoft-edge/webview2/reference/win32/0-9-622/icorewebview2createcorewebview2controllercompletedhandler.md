---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: 845c3a3f0241fb66032ecf818c484b6110258327
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012766"
---
# <span data-ttu-id="67539-104">interfaz ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="67539-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="67539-105">La persona que llama implementa esta interfaz para recibir el CoreWebView2Controller creado a través de CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="67539-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="67539-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="67539-106">Summary</span></span>

 <span data-ttu-id="67539-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="67539-107">Members</span></span>                        | <span data-ttu-id="67539-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="67539-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="67539-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="67539-109">Invoke</span></span>](#invoke) | <span data-ttu-id="67539-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="67539-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="67539-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="67539-111">Members</span></span>

#### <span data-ttu-id="67539-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="67539-112">Invoke</span></span> 

<span data-ttu-id="67539-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="67539-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="67539-114">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ErrorCode, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="67539-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>


---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: e26d711c24758f82d42067fa28e71bc6ac1177ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877416"
---
# <span data-ttu-id="06806-104">interfaz ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="06806-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="06806-105">La persona que llama implementa esta interfaz para recibir el CoreWebView2Controller creado a través de CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="06806-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="06806-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="06806-106">Summary</span></span>

 <span data-ttu-id="06806-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="06806-107">Members</span></span>                        | <span data-ttu-id="06806-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="06806-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="06806-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="06806-109">Invoke</span></span>](#invoke) | <span data-ttu-id="06806-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="06806-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="06806-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="06806-111">Members</span></span>

#### <span data-ttu-id="06806-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="06806-112">Invoke</span></span> 

<span data-ttu-id="06806-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="06806-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="06806-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="06806-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>


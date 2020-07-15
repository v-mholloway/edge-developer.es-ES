---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 9baf172a112f7fa84dae3a38cdbc0b0e0324473f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880804"
---
# <span data-ttu-id="59c81-104">0.9.515: ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="59c81-104">0.9.515 - interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="59c81-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="59c81-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="59c81-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="59c81-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="59c81-107">La persona que llama implementa esta interfaz para recibir el CoreWebView2Controller creado a través de CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="59c81-107">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="59c81-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="59c81-108">Summary</span></span>

 <span data-ttu-id="59c81-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="59c81-109">Members</span></span>                        | <span data-ttu-id="59c81-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="59c81-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="59c81-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="59c81-111">Invoke</span></span>](#invoke) | <span data-ttu-id="59c81-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="59c81-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="59c81-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="59c81-113">Members</span></span>

#### <span data-ttu-id="59c81-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="59c81-114">Invoke</span></span> 

<span data-ttu-id="59c81-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="59c81-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="59c81-116">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="59c81-116">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>


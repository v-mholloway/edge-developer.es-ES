---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2CreateWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: fe81be15531cedae7a01355cbb6b6b27b52f15cc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878634"
---
# <span data-ttu-id="90016-104">0.8.355: IWebView2CreateWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="90016-104">0.8.355 - interface IWebView2CreateWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="90016-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="90016-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="90016-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="90016-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CreateWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="90016-107">La persona que llama implementa esta interfaz para recibir el WebView2Environment creado a través de CreateWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="90016-107">The caller implements this interface to receive the WebView2Environment created via CreateWebView2Environment.</span></span>

## <span data-ttu-id="90016-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="90016-108">Summary</span></span>

 <span data-ttu-id="90016-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="90016-109">Members</span></span>                        | <span data-ttu-id="90016-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="90016-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="90016-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="90016-111">Invoke</span></span>](#invoke) | <span data-ttu-id="90016-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="90016-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="90016-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="90016-113">Members</span></span>

#### <span data-ttu-id="90016-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="90016-114">Invoke</span></span> 

<span data-ttu-id="90016-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="90016-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="90016-116">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span><span class="sxs-lookup"><span data-stu-id="90016-116">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span></span>


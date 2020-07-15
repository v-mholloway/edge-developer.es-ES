---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 0bbd1f79e4ecd9e0816ec144149f2e66f20fc5fe
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880818"
---
# <span data-ttu-id="1b3bf-104">0.9.515: ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="1b3bf-104">0.9.515 - interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="1b3bf-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="1b3bf-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="1b3bf-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="1b3bf-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="1b3bf-107">La persona que llama implementa esta interfaz para recibir el WebView2Environment creado a través de CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="1b3bf-107">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="1b3bf-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="1b3bf-108">Summary</span></span>

 <span data-ttu-id="1b3bf-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1b3bf-109">Members</span></span>                        | <span data-ttu-id="1b3bf-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="1b3bf-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1b3bf-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="1b3bf-111">Invoke</span></span>](#invoke) | <span data-ttu-id="1b3bf-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1b3bf-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="1b3bf-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="1b3bf-113">Members</span></span>

#### <span data-ttu-id="1b3bf-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="1b3bf-114">Invoke</span></span> 

<span data-ttu-id="1b3bf-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1b3bf-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="1b3bf-116">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="1b3bf-116">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: df9d366005c146316903c4093b671cd304636775
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881091"
---
# <span data-ttu-id="f8432-104">0.9.430: ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f8432-104">0.9.430 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f8432-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="f8432-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="f8432-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="f8432-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f8432-107">La persona que llama implementa esta interfaz para recibir el resultado del método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="f8432-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="f8432-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="f8432-108">Summary</span></span>

 <span data-ttu-id="f8432-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f8432-109">Members</span></span>                        | <span data-ttu-id="f8432-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f8432-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f8432-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="f8432-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f8432-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f8432-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f8432-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="f8432-113">Members</span></span>

#### <span data-ttu-id="f8432-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f8432-114">Invoke</span></span> 

<span data-ttu-id="f8432-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f8432-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f8432-116">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="f8432-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>


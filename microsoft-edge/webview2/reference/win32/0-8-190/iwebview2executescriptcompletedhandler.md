---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 6330542e2a894858bc5e43958faaf19dfee6cc7c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655358"
---
# <span data-ttu-id="5c452-104">interfaz IWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="5c452-104">interface IWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="5c452-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="5c452-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="5c452-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="5c452-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="5c452-107">La persona que llama implementa esta interfaz para recibir el resultado del método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="5c452-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="5c452-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="5c452-108">Summary</span></span>

 <span data-ttu-id="5c452-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5c452-109">Members</span></span>                        | <span data-ttu-id="5c452-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="5c452-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5c452-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="5c452-111">Invoke</span></span>](#invoke) | <span data-ttu-id="5c452-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5c452-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="5c452-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="5c452-113">Members</span></span>

#### <span data-ttu-id="5c452-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="5c452-114">Invoke</span></span> 

<span data-ttu-id="5c452-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5c452-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="5c452-116">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="5c452-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>


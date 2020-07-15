---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 903574f0372e9d077907b9e9d538007cb71f830f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878676"
---
# <span data-ttu-id="d9e8c-104">0.8.355: IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="d9e8c-104">0.8.355 - interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="d9e8c-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="d9e8c-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="d9e8c-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="d9e8c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="d9e8c-107">La persona que llama implementa esta interfaz para recibir el resultado del método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="d9e8c-107">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="d9e8c-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="d9e8c-108">Summary</span></span>

 <span data-ttu-id="d9e8c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d9e8c-109">Members</span></span>                        | <span data-ttu-id="d9e8c-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d9e8c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d9e8c-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="d9e8c-111">Invoke</span></span>](#invoke) | <span data-ttu-id="d9e8c-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d9e8c-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="d9e8c-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="d9e8c-113">Members</span></span>

#### <span data-ttu-id="d9e8c-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="d9e8c-114">Invoke</span></span> 

<span data-ttu-id="d9e8c-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d9e8c-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="d9e8c-116">invocación [Invoke](#invoke)de HRESULT pública (código de código HRESULT, identificador de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d9e8c-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR id)</span></span>


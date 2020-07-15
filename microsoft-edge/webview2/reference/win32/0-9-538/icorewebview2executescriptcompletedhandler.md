---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExecuteScriptCompletedHandler
ms.openlocfilehash: ee59ef42852fc8f0b0529b9a3ca08e53972dee1a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879943"
---
# <span data-ttu-id="37aad-104">interfaz ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="37aad-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="37aad-105">La persona que llama implementa esta interfaz para recibir el resultado del método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="37aad-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="37aad-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="37aad-106">Summary</span></span>

 <span data-ttu-id="37aad-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="37aad-107">Members</span></span>                        | <span data-ttu-id="37aad-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="37aad-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="37aad-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="37aad-109">Invoke</span></span>](#invoke) | <span data-ttu-id="37aad-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="37aad-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="37aad-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="37aad-111">Members</span></span>

#### <span data-ttu-id="37aad-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="37aad-112">Invoke</span></span> 

<span data-ttu-id="37aad-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="37aad-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="37aad-114">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="37aad-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


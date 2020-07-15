---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 9a142ddf19d2a0494f868ed62a820ce2cc3cd358
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880937"
---
# <span data-ttu-id="bd184-104">0.9.515: ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="bd184-104">0.9.515 - interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="bd184-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="bd184-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="bd184-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="bd184-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="bd184-107">La persona que llama implementa esta interfaz para recibir resultados de finalización de CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="bd184-107">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="bd184-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="bd184-108">Summary</span></span>

 <span data-ttu-id="bd184-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="bd184-109">Members</span></span>                        | <span data-ttu-id="bd184-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="bd184-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bd184-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="bd184-111">Invoke</span></span>](#invoke) | <span data-ttu-id="bd184-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bd184-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="bd184-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="bd184-113">Members</span></span>

#### <span data-ttu-id="bd184-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="bd184-114">Invoke</span></span> 

<span data-ttu-id="bd184-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bd184-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="bd184-116">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="bd184-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


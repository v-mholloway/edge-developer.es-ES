---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
ms.openlocfilehash: c991e9e9520bd696c579fdca379295afe253ba5d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877520"
---
# <span data-ttu-id="e7ada-104">interfaz ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e7ada-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e7ada-105">La persona que llama implementa esta interfaz para recibir resultados de finalización de CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="e7ada-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="e7ada-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e7ada-106">Summary</span></span>

 <span data-ttu-id="e7ada-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e7ada-107">Members</span></span>                        | <span data-ttu-id="e7ada-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e7ada-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e7ada-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e7ada-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e7ada-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e7ada-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e7ada-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e7ada-111">Members</span></span>

#### <span data-ttu-id="e7ada-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e7ada-112">Invoke</span></span> 

<span data-ttu-id="e7ada-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e7ada-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e7ada-114">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="e7ada-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


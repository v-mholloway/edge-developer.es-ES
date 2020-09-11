---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
ms.openlocfilehash: f6c0037177843d65ce5fe7cc56f206d5661d4b2a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012775"
---
# <span data-ttu-id="6d565-104">interfaz ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="6d565-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6d565-105">La persona que llama implementa esta interfaz para recibir resultados de finalización de CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="6d565-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="6d565-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6d565-106">Summary</span></span>

 <span data-ttu-id="6d565-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6d565-107">Members</span></span>                        | <span data-ttu-id="6d565-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6d565-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6d565-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6d565-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6d565-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6d565-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="6d565-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="6d565-111">Members</span></span>

#### <span data-ttu-id="6d565-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="6d565-112">Invoke</span></span> 

<span data-ttu-id="6d565-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6d565-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6d565-114">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="6d565-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


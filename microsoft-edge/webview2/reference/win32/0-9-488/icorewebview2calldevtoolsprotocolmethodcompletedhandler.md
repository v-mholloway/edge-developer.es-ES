---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 7a983d313e242cc163fb16a9c0d0068a9d6663d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883934"
---
# <span data-ttu-id="ce27d-104">0.9.515: ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ce27d-104">0.9.515 - interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ce27d-105">La persona que llama implementa esta interfaz para recibir resultados de finalización de CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="ce27d-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="ce27d-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="ce27d-106">Summary</span></span>

 <span data-ttu-id="ce27d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ce27d-107">Members</span></span>                        | <span data-ttu-id="ce27d-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ce27d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ce27d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ce27d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ce27d-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ce27d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="ce27d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ce27d-111">Members</span></span>

#### <span data-ttu-id="ce27d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ce27d-112">Invoke</span></span> 

<span data-ttu-id="ce27d-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ce27d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ce27d-114">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="ce27d-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


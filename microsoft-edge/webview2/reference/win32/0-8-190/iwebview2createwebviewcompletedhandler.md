---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2CreateWebViewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 381f46c6682a77905d9caa720e4ba9b2d1d531b7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886155"
---
# <span data-ttu-id="95ba5-104">0.8.355: IWebView2CreateWebViewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="95ba5-104">0.8.355 - interface IWebView2CreateWebViewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CreateWebViewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="95ba5-105">La persona que llama implementa esta interfaz para recibir la vista en WebView creada a través de CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="95ba5-105">The caller implements this interface to receive the WebView created via CreateWebView.</span></span>

## <span data-ttu-id="95ba5-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="95ba5-106">Summary</span></span>

 <span data-ttu-id="95ba5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="95ba5-107">Members</span></span>                        | <span data-ttu-id="95ba5-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="95ba5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95ba5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="95ba5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="95ba5-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="95ba5-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="95ba5-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="95ba5-111">Members</span></span>

#### <span data-ttu-id="95ba5-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="95ba5-112">Invoke</span></span> 

<span data-ttu-id="95ba5-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="95ba5-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="95ba5-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT,[IWebView2WebView](IWebView2WebView.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="95ba5-114">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2WebView](IWebView2WebView.md) \* webView)</span></span>


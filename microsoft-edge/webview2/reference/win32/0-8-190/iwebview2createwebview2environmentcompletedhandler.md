---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2CreateWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 9937fe08f440ce468f178e4ac17935bbb8a1a8ed
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886174"
---
# <span data-ttu-id="e1ff1-104">0.8.355: IWebView2CreateWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e1ff1-104">0.8.355 - interface IWebView2CreateWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CreateWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e1ff1-105">La persona que llama implementa esta interfaz para recibir el WebView2Environment creado a través de CreateWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="e1ff1-105">The caller implements this interface to receive the WebView2Environment created via CreateWebView2Environment.</span></span>

## <span data-ttu-id="e1ff1-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e1ff1-106">Summary</span></span>

 <span data-ttu-id="e1ff1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1ff1-107">Members</span></span>                        | <span data-ttu-id="e1ff1-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e1ff1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1ff1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e1ff1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e1ff1-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e1ff1-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e1ff1-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1ff1-111">Members</span></span>

#### <span data-ttu-id="e1ff1-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e1ff1-112">Invoke</span></span> 

<span data-ttu-id="e1ff1-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e1ff1-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e1ff1-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span><span class="sxs-lookup"><span data-stu-id="e1ff1-114">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span></span>


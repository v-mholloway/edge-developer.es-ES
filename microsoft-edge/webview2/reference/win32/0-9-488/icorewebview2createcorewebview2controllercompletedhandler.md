---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: f85444231cb04857326d1662b2b4fb957e5305fe
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884501"
---
# <span data-ttu-id="620f5-104">0.9.515: ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="620f5-104">0.9.515 - interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="620f5-105">La persona que llama implementa esta interfaz para recibir el CoreWebView2Controller creado a través de CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="620f5-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="620f5-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="620f5-106">Summary</span></span>

 <span data-ttu-id="620f5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="620f5-107">Members</span></span>                        | <span data-ttu-id="620f5-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="620f5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="620f5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="620f5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="620f5-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="620f5-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="620f5-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="620f5-111">Members</span></span>

#### <span data-ttu-id="620f5-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="620f5-112">Invoke</span></span> 

<span data-ttu-id="620f5-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="620f5-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="620f5-114">invocación [Invoke](#invoke)de HRESULT pública (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="620f5-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>


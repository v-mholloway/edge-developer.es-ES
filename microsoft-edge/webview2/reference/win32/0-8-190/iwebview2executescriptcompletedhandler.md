---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 9a075cf5e5d3e5222e76b9ba7550636a67e5696a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886013"
---
# <span data-ttu-id="af55d-104">0.8.355: IWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="af55d-104">0.8.355 - interface IWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="af55d-105">La persona que llama implementa esta interfaz para recibir el resultado del método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="af55d-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="af55d-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="af55d-106">Summary</span></span>

 <span data-ttu-id="af55d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="af55d-107">Members</span></span>                        | <span data-ttu-id="af55d-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="af55d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="af55d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="af55d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="af55d-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="af55d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="af55d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="af55d-111">Members</span></span>

#### <span data-ttu-id="af55d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="af55d-112">Invoke</span></span> 

<span data-ttu-id="af55d-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="af55d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="af55d-114">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="af55d-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>


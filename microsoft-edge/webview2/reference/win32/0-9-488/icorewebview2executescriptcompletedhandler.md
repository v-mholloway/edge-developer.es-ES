---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: e3618b7dc7b866031709ee276c80ba45ec89512d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698039"
---
# <span data-ttu-id="1e5de-104">interfaz ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="1e5de-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="1e5de-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="1e5de-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="1e5de-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="1e5de-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="1e5de-107">La persona que llama implementa esta interfaz para recibir el resultado del método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="1e5de-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="1e5de-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="1e5de-108">Summary</span></span>

 <span data-ttu-id="1e5de-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e5de-109">Members</span></span>                        | <span data-ttu-id="1e5de-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="1e5de-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1e5de-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="1e5de-111">Invoke</span></span>](#invoke) | <span data-ttu-id="1e5de-112">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1e5de-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="1e5de-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e5de-113">Members</span></span>

#### <span data-ttu-id="1e5de-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="1e5de-114">Invoke</span></span> 

<span data-ttu-id="1e5de-115">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1e5de-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="1e5de-116">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="1e5de-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExecuteScriptCompletedHandler
ms.openlocfilehash: 0b257cef4ed4a85fcd41cd401ef00eea01a4d8b6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010232"
---
# <span data-ttu-id="bcbe8-104">0.9.579: ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="bcbe8-104">0.9.579 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="bcbe8-105">La persona que llama implementa esta interfaz para recibir el resultado del método ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="bcbe8-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="bcbe8-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="bcbe8-106">Summary</span></span>

 <span data-ttu-id="bcbe8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bcbe8-107">Members</span></span>                        | <span data-ttu-id="bcbe8-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="bcbe8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bcbe8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="bcbe8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="bcbe8-110">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bcbe8-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="bcbe8-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="bcbe8-111">Members</span></span>

#### <span data-ttu-id="bcbe8-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="bcbe8-112">Invoke</span></span> 

<span data-ttu-id="bcbe8-113">Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bcbe8-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="bcbe8-114">invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="bcbe8-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


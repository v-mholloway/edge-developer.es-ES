---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: ac3b1fc5ceb31cbf2d67649b91f3bfbf2c8ecbe3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880370"
---
# <span data-ttu-id="d4200-104">0.9.515: ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d4200-104">0.9.515 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="d4200-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="d4200-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="d4200-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="d4200-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="d4200-107">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d4200-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="d4200-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="d4200-108">Summary</span></span>

 <span data-ttu-id="d4200-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d4200-109">Members</span></span>                        | <span data-ttu-id="d4200-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d4200-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d4200-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="d4200-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="d4200-112">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="d4200-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="d4200-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="d4200-113">Members</span></span>

#### <span data-ttu-id="d4200-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="d4200-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="d4200-115">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="d4200-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="d4200-116">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="d4200-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


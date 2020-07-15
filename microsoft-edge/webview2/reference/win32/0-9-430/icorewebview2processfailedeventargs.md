---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: f4238f0d75f39727260296703e84740ca77b30d4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877740"
---
# <span data-ttu-id="9ba5f-104">0.9.430: ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9ba5f-104">0.9.430 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="9ba5f-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="9ba5f-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="9ba5f-107">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="9ba5f-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="9ba5f-108">Summary</span></span>

 <span data-ttu-id="9ba5f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9ba5f-109">Members</span></span>                        | <span data-ttu-id="9ba5f-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9ba5f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9ba5f-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="9ba5f-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="9ba5f-112">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="9ba5f-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="9ba5f-113">Members</span></span>

#### <span data-ttu-id="9ba5f-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="9ba5f-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="9ba5f-115">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="9ba5f-116">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="9ba5f-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


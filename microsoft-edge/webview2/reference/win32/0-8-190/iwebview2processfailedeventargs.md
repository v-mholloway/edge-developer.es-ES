---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 5ceb24d0d20f580e14e0d5af7ec09881c9ab0eb2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878249"
---
# <span data-ttu-id="54701-104">0.8.355: IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="54701-104">0.8.355 - interface IWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="54701-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="54701-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="54701-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="54701-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="54701-107">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="54701-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="54701-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="54701-108">Summary</span></span>

 <span data-ttu-id="54701-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="54701-109">Members</span></span>                        | <span data-ttu-id="54701-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="54701-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="54701-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="54701-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="54701-112">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="54701-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="54701-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="54701-113">Members</span></span>

#### <span data-ttu-id="54701-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="54701-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="54701-115">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="54701-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="54701-116">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="54701-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


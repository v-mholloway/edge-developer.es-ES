---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: a19f8c445d7ff1f6bee24cdd8871c28d41eedebe
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886414"
---
# <span data-ttu-id="78457-104">0.9.430: ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="78457-104">0.9.430 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="78457-105">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="78457-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="78457-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="78457-106">Summary</span></span>

 <span data-ttu-id="78457-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="78457-107">Members</span></span>                        | <span data-ttu-id="78457-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="78457-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="78457-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="78457-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="78457-110">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="78457-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="78457-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="78457-111">Members</span></span>

#### <span data-ttu-id="78457-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="78457-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="78457-113">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="78457-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="78457-114">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="78457-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


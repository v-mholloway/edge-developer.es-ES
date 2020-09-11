---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: af27c39b2ed9ba197ab1c567bcf18a43c3dee932
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010022"
---
# <span data-ttu-id="9bbd7-104">0.9.579: ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9bbd7-104">0.9.579 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="9bbd7-105">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="9bbd7-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="9bbd7-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="9bbd7-106">Summary</span></span>

 <span data-ttu-id="9bbd7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9bbd7-107">Members</span></span>                        | <span data-ttu-id="9bbd7-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9bbd7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9bbd7-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="9bbd7-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="9bbd7-110">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="9bbd7-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="9bbd7-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="9bbd7-111">Members</span></span>

#### <span data-ttu-id="9bbd7-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="9bbd7-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="9bbd7-113">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="9bbd7-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="9bbd7-114">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="9bbd7-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


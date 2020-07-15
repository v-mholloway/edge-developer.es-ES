---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: 70fb6f75594284560cb0d64663fbda47cc7404d6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879348"
---
# <span data-ttu-id="8b590-104">interfaz ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8b590-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="8b590-105">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="8b590-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="8b590-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="8b590-106">Summary</span></span>

 <span data-ttu-id="8b590-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8b590-107">Members</span></span>                        | <span data-ttu-id="8b590-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8b590-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8b590-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="8b590-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="8b590-110">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="8b590-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="8b590-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="8b590-111">Members</span></span>

#### <span data-ttu-id="8b590-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="8b590-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="8b590-113">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="8b590-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="8b590-114">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="8b590-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


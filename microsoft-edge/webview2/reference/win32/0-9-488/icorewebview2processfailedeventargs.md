---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 2dc5c437acadb06b5f8b12ae0dc54aec12412355
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883794"
---
# <span data-ttu-id="a0cbc-104">0.9.515: ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0cbc-104">0.9.515 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="a0cbc-105">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="a0cbc-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="a0cbc-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="a0cbc-106">Summary</span></span>

 <span data-ttu-id="a0cbc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0cbc-107">Members</span></span>                        | <span data-ttu-id="a0cbc-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a0cbc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a0cbc-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="a0cbc-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="a0cbc-110">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="a0cbc-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="a0cbc-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0cbc-111">Members</span></span>

#### <span data-ttu-id="a0cbc-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="a0cbc-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="a0cbc-113">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="a0cbc-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="a0cbc-114">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="a0cbc-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


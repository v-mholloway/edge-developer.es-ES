---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 697a49bfe68f83085f6c961ee2cdd5ab21f3b59b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885824"
---
# <span data-ttu-id="980be-104">0.8.355: IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="980be-104">0.8.355 - interface IWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="980be-105">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="980be-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="980be-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="980be-106">Summary</span></span>

 <span data-ttu-id="980be-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="980be-107">Members</span></span>                        | <span data-ttu-id="980be-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="980be-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="980be-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="980be-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="980be-110">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="980be-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="980be-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="980be-111">Members</span></span>

#### <span data-ttu-id="980be-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="980be-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="980be-113">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="980be-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="980be-114">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="980be-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: c01d98ca997a0b4e288ecaa8ede609c93fc84ea1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699334"
---
# <span data-ttu-id="75daf-104">interfaz ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="75daf-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="75daf-105">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="75daf-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="75daf-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="75daf-106">Summary</span></span>

 <span data-ttu-id="75daf-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="75daf-107">Members</span></span>                        | <span data-ttu-id="75daf-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="75daf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="75daf-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="75daf-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="75daf-110">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="75daf-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="75daf-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="75daf-111">Members</span></span>

#### <span data-ttu-id="75daf-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="75daf-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="75daf-113">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="75daf-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="75daf-114">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="75daf-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


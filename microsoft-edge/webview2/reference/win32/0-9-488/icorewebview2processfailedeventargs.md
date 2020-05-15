---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 0efc1656b8204b9775002db49e0e4a5734682cc4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655085"
---
# <span data-ttu-id="b98cd-104">interfaz ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b98cd-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="b98cd-105">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="b98cd-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="b98cd-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="b98cd-106">Summary</span></span>

 <span data-ttu-id="b98cd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b98cd-107">Members</span></span>                        | <span data-ttu-id="b98cd-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b98cd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b98cd-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="b98cd-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="b98cd-110">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="b98cd-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="b98cd-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b98cd-111">Members</span></span>

#### <span data-ttu-id="b98cd-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="b98cd-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="b98cd-113">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="b98cd-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="b98cd-114">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="b98cd-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 748c4affa73001270e2cf97b3d19db8c8ed23686
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655461"
---
# <span data-ttu-id="d3c78-104">interfaz IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d3c78-104">interface IWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="d3c78-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="d3c78-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="d3c78-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="d3c78-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="d3c78-107">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="d3c78-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="d3c78-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="d3c78-108">Summary</span></span>

 <span data-ttu-id="d3c78-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d3c78-109">Members</span></span>                        | <span data-ttu-id="d3c78-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d3c78-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d3c78-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="d3c78-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="d3c78-112">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="d3c78-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="d3c78-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="d3c78-113">Members</span></span>

#### <span data-ttu-id="d3c78-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="d3c78-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="d3c78-115">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="d3c78-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="d3c78-116">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="d3c78-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


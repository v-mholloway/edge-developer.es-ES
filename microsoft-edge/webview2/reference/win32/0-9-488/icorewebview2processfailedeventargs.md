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
ms.openlocfilehash: 4183f3a1c60bd9e2bdcff5227426db1f07c313cf
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697521"
---
# <span data-ttu-id="c6b7e-104">interfaz ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c6b7e-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c6b7e-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="c6b7e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="c6b7e-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="c6b7e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="c6b7e-107">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="c6b7e-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="c6b7e-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="c6b7e-108">Summary</span></span>

 <span data-ttu-id="c6b7e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c6b7e-109">Members</span></span>                        | <span data-ttu-id="c6b7e-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c6b7e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c6b7e-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="c6b7e-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="c6b7e-112">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="c6b7e-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="c6b7e-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="c6b7e-113">Members</span></span>

#### <span data-ttu-id="c6b7e-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="c6b7e-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="c6b7e-115">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="c6b7e-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="c6b7e-116">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="c6b7e-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


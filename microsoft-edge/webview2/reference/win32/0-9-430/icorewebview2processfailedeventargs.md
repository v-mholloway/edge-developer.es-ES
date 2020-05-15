---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 8fba2759ce0e264dcde515ee1191ec819f26eef9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655292"
---
# <span data-ttu-id="b7657-104">interfaz ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b7657-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="b7657-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="b7657-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="b7657-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="b7657-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="b7657-107">Argumentos de evento para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="b7657-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="b7657-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="b7657-108">Summary</span></span>

 <span data-ttu-id="b7657-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7657-109">Members</span></span>                        | <span data-ttu-id="b7657-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b7657-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b7657-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="b7657-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="b7657-112">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="b7657-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="b7657-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7657-113">Members</span></span>

#### <span data-ttu-id="b7657-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="b7657-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="b7657-115">El tipo de error de proceso que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="b7657-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="b7657-116">[get_ProcessFailedKind](#get_processfailedkind)de HRESULT público (CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="b7657-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


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
ms.openlocfilehash: d43cbe741cc9cd8b027a21115133db9377a95658
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655260"
---
# <span data-ttu-id="e90b4-104">interfaz IWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="e90b4-104">interface IWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="e90b4-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="e90b4-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e90b4-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="e90b4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="e90b4-107">Esta interfaz se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="e90b4-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="e90b4-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="e90b4-108">Summary</span></span>

 <span data-ttu-id="e90b4-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e90b4-109">Members</span></span>                        | <span data-ttu-id="e90b4-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e90b4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e90b4-111">Completar</span><span class="sxs-lookup"><span data-stu-id="e90b4-111">Complete</span></span>](#complete) | <span data-ttu-id="e90b4-112">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="e90b4-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="e90b4-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="e90b4-113">Members</span></span>

#### <span data-ttu-id="e90b4-114">Completar</span><span class="sxs-lookup"><span data-stu-id="e90b4-114">Complete</span></span> 

<span data-ttu-id="e90b4-115">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="e90b4-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="e90b4-116">HRESULT público [completado](#complete)()</span><span class="sxs-lookup"><span data-stu-id="e90b4-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="e90b4-117">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="e90b4-117">Complete should only be called once for each deferral taken.</span></span>


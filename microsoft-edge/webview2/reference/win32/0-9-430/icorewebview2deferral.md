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
ms.openlocfilehash: 4f7cf3b73e9f354d86e2595a4ed0d4bccda95285
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655234"
---
# <span data-ttu-id="ad303-104">interfaz ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="ad303-104">interface ICoreWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="ad303-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="ad303-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="ad303-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="ad303-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="ad303-107">Esta interfaz se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="ad303-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="ad303-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="ad303-108">Summary</span></span>

 <span data-ttu-id="ad303-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="ad303-109">Members</span></span>                        | <span data-ttu-id="ad303-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ad303-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ad303-111">Completar</span><span class="sxs-lookup"><span data-stu-id="ad303-111">Complete</span></span>](#complete) | <span data-ttu-id="ad303-112">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="ad303-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="ad303-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="ad303-113">Members</span></span>

#### <span data-ttu-id="ad303-114">Completar</span><span class="sxs-lookup"><span data-stu-id="ad303-114">Complete</span></span> 

<span data-ttu-id="ad303-115">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="ad303-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="ad303-116">HRESULT público [completado](#complete)()</span><span class="sxs-lookup"><span data-stu-id="ad303-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="ad303-117">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="ad303-117">Complete should only be called once for each deferral taken.</span></span>


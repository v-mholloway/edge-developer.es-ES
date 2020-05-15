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
ms.openlocfilehash: ebaab6dfe0781f544e89e86afc9f16ab50cb9222
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655346"
---
# <span data-ttu-id="7eed1-104">interfaz ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="7eed1-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="7eed1-105">Esta interfaz se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="7eed1-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="7eed1-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="7eed1-106">Summary</span></span>

 <span data-ttu-id="7eed1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7eed1-107">Members</span></span>                        | <span data-ttu-id="7eed1-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7eed1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7eed1-109">Completar</span><span class="sxs-lookup"><span data-stu-id="7eed1-109">Complete</span></span>](#complete) | <span data-ttu-id="7eed1-110">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="7eed1-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="7eed1-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="7eed1-111">Members</span></span>

#### <span data-ttu-id="7eed1-112">Completar</span><span class="sxs-lookup"><span data-stu-id="7eed1-112">Complete</span></span> 

<span data-ttu-id="7eed1-113">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="7eed1-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="7eed1-114">HRESULT público [completado](#complete)()</span><span class="sxs-lookup"><span data-stu-id="7eed1-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="7eed1-115">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="7eed1-115">Complete should only be called once for each deferral taken.</span></span>


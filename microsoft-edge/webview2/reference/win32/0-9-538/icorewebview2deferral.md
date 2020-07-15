---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2Deferral
ms.openlocfilehash: 85c8a795a79bae461ad958e6586b9bf1f6778075
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880125"
---
# <span data-ttu-id="e0ebf-104">interfaz ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="e0ebf-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="e0ebf-105">Esta interfaz se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="e0ebf-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="e0ebf-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e0ebf-106">Summary</span></span>

 <span data-ttu-id="e0ebf-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e0ebf-107">Members</span></span>                        | <span data-ttu-id="e0ebf-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e0ebf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e0ebf-109">Completar</span><span class="sxs-lookup"><span data-stu-id="e0ebf-109">Complete</span></span>](#complete) | <span data-ttu-id="e0ebf-110">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="e0ebf-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="e0ebf-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e0ebf-111">Members</span></span>

#### <span data-ttu-id="e0ebf-112">Completar</span><span class="sxs-lookup"><span data-stu-id="e0ebf-112">Complete</span></span> 

<span data-ttu-id="e0ebf-113">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="e0ebf-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="e0ebf-114">HRESULT público [completado](#complete)()</span><span class="sxs-lookup"><span data-stu-id="e0ebf-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="e0ebf-115">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="e0ebf-115">Complete should only be called once for each deferral taken.</span></span>


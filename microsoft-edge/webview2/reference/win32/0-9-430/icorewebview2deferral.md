---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: bf6ce187168223b7e108aff7abf1bee5adea05a6
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884270"
---
# <span data-ttu-id="ecd5e-104">0.9.430: ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="ecd5e-104">0.9.430 - interface ICoreWebView2Deferral</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="ecd5e-105">Esta interfaz se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="ecd5e-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="ecd5e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="ecd5e-106">Summary</span></span>

 <span data-ttu-id="ecd5e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ecd5e-107">Members</span></span>                        | <span data-ttu-id="ecd5e-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ecd5e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ecd5e-109">Completar</span><span class="sxs-lookup"><span data-stu-id="ecd5e-109">Complete</span></span>](#complete) | <span data-ttu-id="ecd5e-110">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="ecd5e-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="ecd5e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ecd5e-111">Members</span></span>

#### <span data-ttu-id="ecd5e-112">Completar</span><span class="sxs-lookup"><span data-stu-id="ecd5e-112">Complete</span></span> 

<span data-ttu-id="ecd5e-113">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="ecd5e-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="ecd5e-114">HRESULT público [completado](#complete)()</span><span class="sxs-lookup"><span data-stu-id="ecd5e-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="ecd5e-115">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="ecd5e-115">Complete should only be called once for each deferral taken.</span></span>


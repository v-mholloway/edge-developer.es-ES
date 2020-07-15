---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: f40d0baa415ccc76747993c4070bb05eaf76fe56
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878613"
---
# <span data-ttu-id="a8fa1-104">0.8.355: IWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="a8fa1-104">0.8.355 - interface IWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="a8fa1-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="a8fa1-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="a8fa1-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="a8fa1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="a8fa1-107">Esta interfaz se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="a8fa1-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="a8fa1-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="a8fa1-108">Summary</span></span>

 <span data-ttu-id="a8fa1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a8fa1-109">Members</span></span>                        | <span data-ttu-id="a8fa1-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a8fa1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a8fa1-111">Completar</span><span class="sxs-lookup"><span data-stu-id="a8fa1-111">Complete</span></span>](#complete) | <span data-ttu-id="a8fa1-112">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="a8fa1-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="a8fa1-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="a8fa1-113">Members</span></span>

#### <span data-ttu-id="a8fa1-114">Completar</span><span class="sxs-lookup"><span data-stu-id="a8fa1-114">Complete</span></span> 

<span data-ttu-id="a8fa1-115">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="a8fa1-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="a8fa1-116">HRESULT público [completado](#complete)()</span><span class="sxs-lookup"><span data-stu-id="a8fa1-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="a8fa1-117">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="a8fa1-117">Complete should only be called once for each deferral taken.</span></span>


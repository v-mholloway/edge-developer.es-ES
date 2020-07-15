---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: bd2ff8092ce0b8367ce4cc381e94dbd273ae1849
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880832"
---
# <span data-ttu-id="2dc4d-104">0.9.515: ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="2dc4d-104">0.9.515 - interface ICoreWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="2dc4d-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="2dc4d-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="2dc4d-107">Esta interfaz se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="2dc4d-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="2dc4d-108">Summary</span></span>

 <span data-ttu-id="2dc4d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2dc4d-109">Members</span></span>                        | <span data-ttu-id="2dc4d-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2dc4d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2dc4d-111">Completar</span><span class="sxs-lookup"><span data-stu-id="2dc4d-111">Complete</span></span>](#complete) | <span data-ttu-id="2dc4d-112">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="2dc4d-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="2dc4d-113">Members</span></span>

#### <span data-ttu-id="2dc4d-114">Completar</span><span class="sxs-lookup"><span data-stu-id="2dc4d-114">Complete</span></span> 

<span data-ttu-id="2dc4d-115">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="2dc4d-116">HRESULT público [completado](#complete)()</span><span class="sxs-lookup"><span data-stu-id="2dc4d-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="2dc4d-117">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-117">Complete should only be called once for each deferral taken.</span></span>


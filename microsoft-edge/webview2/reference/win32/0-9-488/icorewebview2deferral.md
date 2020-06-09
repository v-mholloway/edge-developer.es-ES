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
ms.openlocfilehash: 7d21db7c3f0a66f60f32e92b3951151b8d13a002
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698081"
---
# <span data-ttu-id="a7d98-104">interfaz ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="a7d98-104">interface ICoreWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="a7d98-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="a7d98-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a7d98-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="a7d98-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="a7d98-107">Esta interfaz se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="a7d98-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="a7d98-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="a7d98-108">Summary</span></span>

 <span data-ttu-id="a7d98-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a7d98-109">Members</span></span>                        | <span data-ttu-id="a7d98-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a7d98-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a7d98-111">Completar</span><span class="sxs-lookup"><span data-stu-id="a7d98-111">Complete</span></span>](#complete) | <span data-ttu-id="a7d98-112">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="a7d98-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="a7d98-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="a7d98-113">Members</span></span>

#### <span data-ttu-id="a7d98-114">Completar</span><span class="sxs-lookup"><span data-stu-id="a7d98-114">Complete</span></span> 

<span data-ttu-id="a7d98-115">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="a7d98-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="a7d98-116">HRESULT público [completado](#complete)()</span><span class="sxs-lookup"><span data-stu-id="a7d98-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="a7d98-117">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="a7d98-117">Complete should only be called once for each deferral taken.</span></span>


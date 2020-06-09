---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: b5fcd04d702483778ef31549c2e7d989ebfe3689
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699365"
---
# <span data-ttu-id="8f02a-104">interfaz ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="8f02a-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="8f02a-105">Esta interfaz se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="8f02a-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="8f02a-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="8f02a-106">Summary</span></span>

 <span data-ttu-id="8f02a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8f02a-107">Members</span></span>                        | <span data-ttu-id="8f02a-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8f02a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8f02a-109">Completar</span><span class="sxs-lookup"><span data-stu-id="8f02a-109">Complete</span></span>](#complete) | <span data-ttu-id="8f02a-110">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="8f02a-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="8f02a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="8f02a-111">Members</span></span>

#### <span data-ttu-id="8f02a-112">Completar</span><span class="sxs-lookup"><span data-stu-id="8f02a-112">Complete</span></span> 

<span data-ttu-id="8f02a-113">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="8f02a-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="8f02a-114">HRESULT público [completado](#complete)()</span><span class="sxs-lookup"><span data-stu-id="8f02a-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="8f02a-115">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="8f02a-115">Complete should only be called once for each deferral taken.</span></span>


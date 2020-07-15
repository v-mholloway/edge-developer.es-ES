---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 4df74c4a645b6bfa17228860f627910d374e19c4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878725"
---
# <span data-ttu-id="b11ab-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral (clase)</span><span class="sxs-lookup"><span data-stu-id="b11ab-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

> [!NOTE]
> <span data-ttu-id="b11ab-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="b11ab-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b11ab-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="b11ab-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="b11ab-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b11ab-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b11ab-108">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b11ab-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b11ab-109">Esta clase se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="b11ab-109">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="b11ab-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="b11ab-110">Summary</span></span>

 <span data-ttu-id="b11ab-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b11ab-111">Members</span></span>                        | <span data-ttu-id="b11ab-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b11ab-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b11ab-113">Completar</span><span class="sxs-lookup"><span data-stu-id="b11ab-113">Complete</span></span>](#complete) | <span data-ttu-id="b11ab-114">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="b11ab-114">Completes the associated deferred event.</span></span>

## <span data-ttu-id="b11ab-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="b11ab-115">Members</span></span>

#### <span data-ttu-id="b11ab-116">Completar</span><span class="sxs-lookup"><span data-stu-id="b11ab-116">Complete</span></span> 

<span data-ttu-id="b11ab-117">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="b11ab-117">Completes the associated deferred event.</span></span>

> <span data-ttu-id="b11ab-118">[finalización](#complete)de public void ()</span><span class="sxs-lookup"><span data-stu-id="b11ab-118">public void [Complete](#complete)()</span></span>

<span data-ttu-id="b11ab-119">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="b11ab-119">Complete should only be called once for each deferral taken.</span></span>


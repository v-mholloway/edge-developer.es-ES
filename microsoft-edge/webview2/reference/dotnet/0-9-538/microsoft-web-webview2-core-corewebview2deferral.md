---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Deferral
ms.openlocfilehash: 77a3540a64c9894f10cb0c03998dafda90e4f15b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878935"
---
# <span data-ttu-id="6c170-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="6c170-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="6c170-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6c170-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6c170-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="6c170-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6c170-107">Esta clase se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="6c170-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="6c170-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="6c170-108">Summary</span></span>

 <span data-ttu-id="6c170-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c170-109">Members</span></span>                        | <span data-ttu-id="6c170-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6c170-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c170-111">Completar</span><span class="sxs-lookup"><span data-stu-id="6c170-111">Complete</span></span>](#complete) | <span data-ttu-id="6c170-112">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="6c170-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="6c170-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c170-113">Members</span></span>

#### <span data-ttu-id="6c170-114">Completar</span><span class="sxs-lookup"><span data-stu-id="6c170-114">Complete</span></span> 

<span data-ttu-id="6c170-115">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="6c170-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="6c170-116">[finalización](#complete)de public void ()</span><span class="sxs-lookup"><span data-stu-id="6c170-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="6c170-117">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="6c170-117">Complete should only be called once for each deferral taken.</span></span>


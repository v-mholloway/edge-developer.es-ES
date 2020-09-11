---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Deferral
ms.openlocfilehash: 62cd86772d45e1bf9eee7d1821a90b723e1af7db
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011051"
---
# <span data-ttu-id="5e2d8-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Deferral (clase)</span><span class="sxs-lookup"><span data-stu-id="5e2d8-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="5e2d8-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="5e2d8-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="5e2d8-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="5e2d8-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="5e2d8-107">Esta clase se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="5e2d8-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="5e2d8-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="5e2d8-108">Summary</span></span>

 <span data-ttu-id="5e2d8-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e2d8-109">Members</span></span>                        | <span data-ttu-id="5e2d8-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="5e2d8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5e2d8-111">Completar</span><span class="sxs-lookup"><span data-stu-id="5e2d8-111">Complete</span></span>](#complete) | <span data-ttu-id="5e2d8-112">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="5e2d8-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="5e2d8-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e2d8-113">Members</span></span>

#### <span data-ttu-id="5e2d8-114">Completar</span><span class="sxs-lookup"><span data-stu-id="5e2d8-114">Complete</span></span> 

<span data-ttu-id="5e2d8-115">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="5e2d8-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="5e2d8-116">[finalización](#complete)de public void ()</span><span class="sxs-lookup"><span data-stu-id="5e2d8-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="5e2d8-117">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="5e2d8-117">Complete should only be called once for each deferral taken.</span></span>


---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Deferral
ms.openlocfilehash: dcefefd37167b6ff78f2d994f84af6c707423bb4
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012678"
---
# <span data-ttu-id="9ad29-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="9ad29-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="9ad29-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="9ad29-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="9ad29-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="9ad29-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="9ad29-107">Esta clase se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="9ad29-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="9ad29-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="9ad29-108">Summary</span></span>

 <span data-ttu-id="9ad29-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9ad29-109">Members</span></span>                        | <span data-ttu-id="9ad29-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9ad29-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9ad29-111">Completar</span><span class="sxs-lookup"><span data-stu-id="9ad29-111">Complete</span></span>](#complete) | <span data-ttu-id="9ad29-112">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="9ad29-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="9ad29-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="9ad29-113">Members</span></span>

#### <span data-ttu-id="9ad29-114">Completar</span><span class="sxs-lookup"><span data-stu-id="9ad29-114">Complete</span></span> 

<span data-ttu-id="9ad29-115">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="9ad29-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="9ad29-116">[finalización](#complete)de public void ()</span><span class="sxs-lookup"><span data-stu-id="9ad29-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="9ad29-117">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="9ad29-117">Complete should only be called once for each deferral taken.</span></span>


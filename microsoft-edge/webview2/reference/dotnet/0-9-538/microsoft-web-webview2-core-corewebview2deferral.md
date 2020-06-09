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
ms.openlocfilehash: 935e8edb4db54e7bbb707cb2dc704ba312ed3196
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699325"
---
# <span data-ttu-id="383c2-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="383c2-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="383c2-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="383c2-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="383c2-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="383c2-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="383c2-107">Esta clase se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="383c2-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="383c2-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="383c2-108">Summary</span></span>

 <span data-ttu-id="383c2-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="383c2-109">Members</span></span>                        | <span data-ttu-id="383c2-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="383c2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="383c2-111">Completar</span><span class="sxs-lookup"><span data-stu-id="383c2-111">Complete</span></span>](#complete) | <span data-ttu-id="383c2-112">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="383c2-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="383c2-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="383c2-113">Members</span></span>

#### <span data-ttu-id="383c2-114">Completar</span><span class="sxs-lookup"><span data-stu-id="383c2-114">Complete</span></span> 

<span data-ttu-id="383c2-115">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="383c2-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="383c2-116">[finalización](#complete)de public void ()</span><span class="sxs-lookup"><span data-stu-id="383c2-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="383c2-117">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="383c2-117">Complete should only be called once for each deferral taken.</span></span>


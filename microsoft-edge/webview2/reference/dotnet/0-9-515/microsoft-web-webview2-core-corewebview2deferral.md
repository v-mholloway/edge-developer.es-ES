---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 135289994bdfe5481018c479b7a1d9c372ecb256
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885112"
---
# <span data-ttu-id="05eb3-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral (clase)</span><span class="sxs-lookup"><span data-stu-id="05eb3-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="05eb3-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="05eb3-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="05eb3-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="05eb3-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="05eb3-107">Esta clase se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="05eb3-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="05eb3-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="05eb3-108">Summary</span></span>

 <span data-ttu-id="05eb3-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="05eb3-109">Members</span></span>                        | <span data-ttu-id="05eb3-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="05eb3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="05eb3-111">Completar</span><span class="sxs-lookup"><span data-stu-id="05eb3-111">Complete</span></span>](#complete) | <span data-ttu-id="05eb3-112">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="05eb3-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="05eb3-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="05eb3-113">Members</span></span>

#### <span data-ttu-id="05eb3-114">Completar</span><span class="sxs-lookup"><span data-stu-id="05eb3-114">Complete</span></span> 

<span data-ttu-id="05eb3-115">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="05eb3-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="05eb3-116">[finalización](#complete)de public void ()</span><span class="sxs-lookup"><span data-stu-id="05eb3-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="05eb3-117">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="05eb3-117">Complete should only be called once for each deferral taken.</span></span>


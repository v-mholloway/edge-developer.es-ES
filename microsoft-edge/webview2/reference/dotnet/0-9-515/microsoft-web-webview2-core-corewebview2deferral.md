---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: fec7fd7399222d8223d1022cd1e528bc9ed0d161
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655388"
---
# <span data-ttu-id="08f71-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="08f71-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="08f71-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="08f71-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="08f71-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="08f71-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="08f71-107">Esta clase se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="08f71-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="08f71-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="08f71-108">Summary</span></span>

 <span data-ttu-id="08f71-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="08f71-109">Members</span></span>                        | <span data-ttu-id="08f71-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="08f71-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="08f71-111">Completar</span><span class="sxs-lookup"><span data-stu-id="08f71-111">Complete</span></span>](#complete) | <span data-ttu-id="08f71-112">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="08f71-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="08f71-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="08f71-113">Members</span></span>

#### <span data-ttu-id="08f71-114">Completar</span><span class="sxs-lookup"><span data-stu-id="08f71-114">Complete</span></span> 

<span data-ttu-id="08f71-115">Completa el evento diferido asociado.</span><span class="sxs-lookup"><span data-stu-id="08f71-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="08f71-116">[finalización](#complete)de public void ()</span><span class="sxs-lookup"><span data-stu-id="08f71-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="08f71-117">Solo se debe llamar a complete una vez por cada aplazamiento tomado.</span><span class="sxs-lookup"><span data-stu-id="08f71-117">Complete should only be called once for each deferral taken.</span></span>


---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: aaaad1f622887ed1c941a9cf12ee4c753b352286
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878886"
---
# <span data-ttu-id="93550-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="93550-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

<span data-ttu-id="93550-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="93550-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="93550-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="93550-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="93550-107">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="93550-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="93550-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="93550-108">Summary</span></span>

 <span data-ttu-id="93550-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="93550-109">Members</span></span>                        | <span data-ttu-id="93550-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="93550-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="93550-111">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="93550-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="93550-112">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="93550-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="93550-113">NavigationId</span><span class="sxs-lookup"><span data-stu-id="93550-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="93550-114">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="93550-114">The ID of the navigation.</span></span>
[<span data-ttu-id="93550-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="93550-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="93550-116">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="93550-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="93550-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="93550-117">Members</span></span>

#### <span data-ttu-id="93550-118">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="93550-118">IsSuccess</span></span> 

<span data-ttu-id="93550-119">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="93550-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="93550-120">Public bool [IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="93550-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="93550-121">Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="93550-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="93550-122">NavigationId</span><span class="sxs-lookup"><span data-stu-id="93550-122">NavigationId</span></span> 

<span data-ttu-id="93550-123">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="93550-123">The ID of the navigation.</span></span>

> <span data-ttu-id="93550-124">ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="93550-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="93550-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="93550-125">WebErrorStatus</span></span> 

<span data-ttu-id="93550-126">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="93550-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="93550-127">CoreWebView2WebErrorStatus pública [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="93550-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>


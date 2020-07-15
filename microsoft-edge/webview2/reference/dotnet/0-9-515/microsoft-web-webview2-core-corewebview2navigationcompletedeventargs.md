---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 3a15232a7fe2ddf230d0463069052c55f7abc843
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879138"
---
# <span data-ttu-id="40a3d-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="40a3d-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="40a3d-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="40a3d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="40a3d-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="40a3d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="40a3d-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="40a3d-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="40a3d-108">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="40a3d-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="40a3d-109">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="40a3d-109">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="40a3d-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="40a3d-110">Summary</span></span>

 <span data-ttu-id="40a3d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="40a3d-111">Members</span></span>                        | <span data-ttu-id="40a3d-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="40a3d-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="40a3d-113">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="40a3d-113">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="40a3d-114">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="40a3d-114">True when the navigation is successful.</span></span>
[<span data-ttu-id="40a3d-115">NavigationId</span><span class="sxs-lookup"><span data-stu-id="40a3d-115">NavigationId</span></span>](#navigationid) | <span data-ttu-id="40a3d-116">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="40a3d-116">The ID of the navigation.</span></span>
[<span data-ttu-id="40a3d-117">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="40a3d-117">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="40a3d-118">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="40a3d-118">The error code if the navigation failed.</span></span>

## <span data-ttu-id="40a3d-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="40a3d-119">Members</span></span>

#### <span data-ttu-id="40a3d-120">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="40a3d-120">IsSuccess</span></span> 

<span data-ttu-id="40a3d-121">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="40a3d-121">True when the navigation is successful.</span></span>

> <span data-ttu-id="40a3d-122">Public bool [IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="40a3d-122">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="40a3d-123">Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="40a3d-123">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="40a3d-124">NavigationId</span><span class="sxs-lookup"><span data-stu-id="40a3d-124">NavigationId</span></span> 

<span data-ttu-id="40a3d-125">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="40a3d-125">The ID of the navigation.</span></span>

> <span data-ttu-id="40a3d-126">ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="40a3d-126">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="40a3d-127">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="40a3d-127">WebErrorStatus</span></span> 

<span data-ttu-id="40a3d-128">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="40a3d-128">The error code if the navigation failed.</span></span>

> <span data-ttu-id="40a3d-129">CoreWebView2WebErrorStatus pública [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="40a3d-129">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>


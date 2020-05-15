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
ms.openlocfilehash: 2a18fe9f8f79a109047d029affab8d84a6ef845c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655088"
---
# <span data-ttu-id="10516-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="10516-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

<span data-ttu-id="10516-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="10516-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="10516-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="10516-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="10516-107">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="10516-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="10516-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="10516-108">Summary</span></span>

 <span data-ttu-id="10516-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="10516-109">Members</span></span>                        | <span data-ttu-id="10516-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="10516-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10516-111">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="10516-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="10516-112">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="10516-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="10516-113">NavigationId</span><span class="sxs-lookup"><span data-stu-id="10516-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="10516-114">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="10516-114">The ID of the navigation.</span></span>
[<span data-ttu-id="10516-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="10516-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="10516-116">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="10516-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="10516-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="10516-117">Members</span></span>

#### <span data-ttu-id="10516-118">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="10516-118">IsSuccess</span></span> 

<span data-ttu-id="10516-119">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="10516-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="10516-120">Public bool [IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="10516-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="10516-121">Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="10516-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="10516-122">NavigationId</span><span class="sxs-lookup"><span data-stu-id="10516-122">NavigationId</span></span> 

<span data-ttu-id="10516-123">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="10516-123">The ID of the navigation.</span></span>

> <span data-ttu-id="10516-124">ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="10516-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="10516-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="10516-125">WebErrorStatus</span></span> 

<span data-ttu-id="10516-126">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="10516-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="10516-127">CoreWebView2WebErrorStatus pública [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="10516-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>


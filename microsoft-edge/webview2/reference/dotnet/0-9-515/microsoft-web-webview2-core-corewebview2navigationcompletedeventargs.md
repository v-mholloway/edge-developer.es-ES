---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: e2e973e2ee1817decd24bbc1d0dc3daa9709795c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885082"
---
# <span data-ttu-id="6525d-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="6525d-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="6525d-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6525d-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6525d-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="6525d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6525d-107">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="6525d-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="6525d-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="6525d-108">Summary</span></span>

 <span data-ttu-id="6525d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6525d-109">Members</span></span>                        | <span data-ttu-id="6525d-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6525d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6525d-111">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="6525d-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="6525d-112">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="6525d-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="6525d-113">NavigationId</span><span class="sxs-lookup"><span data-stu-id="6525d-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="6525d-114">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="6525d-114">The ID of the navigation.</span></span>
[<span data-ttu-id="6525d-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="6525d-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="6525d-116">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="6525d-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="6525d-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="6525d-117">Members</span></span>

#### <span data-ttu-id="6525d-118">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="6525d-118">IsSuccess</span></span> 

<span data-ttu-id="6525d-119">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="6525d-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="6525d-120">Public bool [IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="6525d-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="6525d-121">Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="6525d-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="6525d-122">NavigationId</span><span class="sxs-lookup"><span data-stu-id="6525d-122">NavigationId</span></span> 

<span data-ttu-id="6525d-123">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="6525d-123">The ID of the navigation.</span></span>

> <span data-ttu-id="6525d-124">ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="6525d-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="6525d-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="6525d-125">WebErrorStatus</span></span> 

<span data-ttu-id="6525d-126">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="6525d-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="6525d-127">CoreWebView2WebErrorStatus pública [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="6525d-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>


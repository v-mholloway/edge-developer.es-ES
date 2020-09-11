---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: 01102cc9aa9d6fbec7f4d223e1115892dabe2899
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010974"
---
# <span data-ttu-id="46565-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="46565-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="46565-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="46565-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="46565-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="46565-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="46565-107">Argumentos de evento para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="46565-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="46565-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="46565-108">Summary</span></span>

 <span data-ttu-id="46565-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="46565-109">Members</span></span>                        | <span data-ttu-id="46565-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="46565-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="46565-111">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="46565-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="46565-112">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="46565-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="46565-113">NavigationId</span><span class="sxs-lookup"><span data-stu-id="46565-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="46565-114">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="46565-114">The ID of the navigation.</span></span>
[<span data-ttu-id="46565-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="46565-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="46565-116">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="46565-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="46565-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="46565-117">Members</span></span>

#### <span data-ttu-id="46565-118">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="46565-118">IsSuccess</span></span> 

<span data-ttu-id="46565-119">Es verdadero cuando la navegación es correcta.</span><span class="sxs-lookup"><span data-stu-id="46565-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="46565-120">Public bool [IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="46565-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="46565-121">Esto es falso para una navegación que terminó en una página de error (errores debidos a ausencia de red, error de búsqueda DNS, el servidor HTTP responde con 4xx), pero también podría ser falso si se llamase a Window. STOP () en la página desplazada.</span><span class="sxs-lookup"><span data-stu-id="46565-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="46565-122">NavigationId</span><span class="sxs-lookup"><span data-stu-id="46565-122">NavigationId</span></span> 

<span data-ttu-id="46565-123">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="46565-123">The ID of the navigation.</span></span>

> <span data-ttu-id="46565-124">ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="46565-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="46565-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="46565-125">WebErrorStatus</span></span> 

<span data-ttu-id="46565-126">El código de error si se produjo un error en la navegación.</span><span class="sxs-lookup"><span data-stu-id="46565-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="46565-127">CoreWebView2WebErrorStatus pública [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="46565-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>


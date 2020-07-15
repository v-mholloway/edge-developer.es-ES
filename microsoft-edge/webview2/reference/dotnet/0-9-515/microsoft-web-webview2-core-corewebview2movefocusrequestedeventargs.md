---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 37d64a18589df936383efe05317c1a625b841a6e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877661"
---
# <span data-ttu-id="46c91-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="46c91-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="46c91-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="46c91-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="46c91-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="46c91-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="46c91-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="46c91-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="46c91-108">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="46c91-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="46c91-109">Argumentos de evento para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="46c91-109">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="46c91-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="46c91-110">Summary</span></span>

 <span data-ttu-id="46c91-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="46c91-111">Members</span></span>                        | <span data-ttu-id="46c91-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="46c91-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="46c91-113">Handled</span><span class="sxs-lookup"><span data-stu-id="46c91-113">Handled</span></span>](#handled) | <span data-ttu-id="46c91-114">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="46c91-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="46c91-115">Razón</span><span class="sxs-lookup"><span data-stu-id="46c91-115">Reason</span></span>](#reason) | <span data-ttu-id="46c91-116">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="46c91-116">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="46c91-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="46c91-117">Members</span></span>

#### <span data-ttu-id="46c91-118">Handled</span><span class="sxs-lookup"><span data-stu-id="46c91-118">Handled</span></span> 

<span data-ttu-id="46c91-119">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="46c91-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="46c91-120">bool público [Handled](#handled)</span><span class="sxs-lookup"><span data-stu-id="46c91-120">public bool [Handled](#handled)</span></span>

<span data-ttu-id="46c91-121">Si la aplicación ha movido el foco a la ubicación deseada, debe establecer la propiedad Handled en TRUE.</span><span class="sxs-lookup"><span data-stu-id="46c91-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="46c91-122">Cuando la propiedad Handled es false después de que el controlador de eventos devuelva, se realiza una acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="46c91-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="46c91-123">La acción predeterminada es intentar buscar la siguiente ventana secundaria de la pestaña detener en la aplicación e intentar mover el foco a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="46c91-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="46c91-124">Si no hay ninguna otra ventana de este tipo para mover el foco, el foco se reactivará dentro del contenido Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="46c91-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="46c91-125">Razón</span><span class="sxs-lookup"><span data-stu-id="46c91-125">Reason</span></span> 

<span data-ttu-id="46c91-126">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="46c91-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="46c91-127">[razón](#reason) de CoreWebView2MoveFocusReason pública</span><span class="sxs-lookup"><span data-stu-id="46c91-127">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

